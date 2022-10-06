# architectural-studies

Laravel w/ Clean Arch

    controllerMethod(LaravelRequest) {

        Adapter(LaravelRequest)->RequestContract

        if (Adapter->validContract === true) {

            Adapter->InteractorContract = Interactor(RequestContract)->InteractorContract

        }

        return Adapter()->LaravelJsonResponse
    }
