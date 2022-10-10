# architectural-studies

Laravel w/ Clean Arch

    public function controllerMethod(Request $request): Response
    {
    
        $adapter = new Adapter($request);
        
        if ($adapter->validContract) {
        
            $interactor = new Interactor($adapter->inputContract);
            
            $adapter->setResponse($interactor->interactorContract);
            
        }

        $adapter->setResponse();

        return $adapter->response;
        
    }
