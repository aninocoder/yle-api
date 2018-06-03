# yle-api

This is a simple project where I play around with MVVC concepts in Unity and create a simple client-to-backend interface that handles connections and web requests to the public YLE Api (which is basically a public media content information repository).

I tried implementing the MVVC concept via the following main classes/components:

- `ProgramsModel`: implements and serves data-related information
- `ProgramsViewController`: interface between data and UI, handles model changes as well as serves UI-related requests.

And then create my own simple client-to-backend API specific to the use of the public YLE Api via the following concepts and solutions:
- Creating a simple YLE SDK for Unity which I can then (theoretically) re-use across different projects. I try to keep this sort of mentality when creating solutions for meta-features and/or 3rd-party functionality that need to be integrated into Unity.
- Creating a generic web request builder that makes use of the `UnityWebRequest` object. This enables me to send and process web requests and responses faster and more convenient since I can offload much of the processing of the raw response to this builder.
- I try to demonstrate the benefits of extending built-in data structure interfaces (via adding general-use convenience functions to `IDictionary`). 

### Important Note
The project is meant to be viewed on a 16:10 aspect ratio, and has been tested only on Android devices.
