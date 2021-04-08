---
title: Compilazione e registrazione di una DLL proxy
description: Se è stato scelto il marshalling del proxy/stub per l'applicazione, i file. c e. h generati da MIDL devono essere compilati e collegati per creare una DLL proxy e tale DLL deve essere inserita nel registro di sistema in modo che i client possano individuare le interfacce.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b0dcd28359172ff2f90391d44a66f8f51a4cbf
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730514"
---
# <a name="building-and-registering-a-proxy-dll"></a><span data-ttu-id="eb7f5-103">Compilazione e registrazione di una DLL proxy</span><span class="sxs-lookup"><span data-stu-id="eb7f5-103">Building and Registering a Proxy DLL</span></span>

<span data-ttu-id="eb7f5-104">Se è stato scelto il marshalling del proxy/stub per l'applicazione, i file. c e. h generati da MIDL devono essere compilati e collegati per creare una DLL proxy e tale DLL deve essere inserita nel registro di sistema in modo che i client possano individuare le interfacce.</span><span class="sxs-lookup"><span data-stu-id="eb7f5-104">If you chose proxy/stub marshaling for your application, the .c and .h files that MIDL generated must be compiled and linked to create a proxy DLL, and that DLL must be entered into the system registry so that clients can locate your interfaces.</span></span> <span data-ttu-id="eb7f5-105">Il file generato da MIDL dlldata. c contiene le routine e altre informazioni necessarie per compilare e registrare una DLL proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="eb7f5-105">The MIDL-generated file Dlldata.c contains the necessary routines and other information to build and register a proxy/stub DLL.</span></span>

<span data-ttu-id="eb7f5-106">Il primo passaggio nella creazione della DLL consiste nel scrivere un file di definizione del modulo per il linker, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="eb7f5-106">The first step in building the DLL is to write a module definition file for the linker, as shown in the following example:</span></span>

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

<span data-ttu-id="eb7f5-107">In alternativa, è possibile specificare queste funzioni esportate nella riga di comando del collegamento del makefile.</span><span class="sxs-lookup"><span data-stu-id="eb7f5-107">Alternatively, you can specify these exported functions on the LINK command line of your makefile.</span></span>

<span data-ttu-id="eb7f5-108">Le funzioni esportate sono dichiarate in Rpcproxy. h, che dlldata. c include e le implementazioni predefinite fanno parte della libreria di runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="eb7f5-108">The exported functions are declared in Rpcproxy.h, which Dlldata.c includes, and default implementations are part of the RPC run-time library.</span></span> <span data-ttu-id="eb7f5-109">COM utilizza queste funzioni per creare un class factory, scaricare le dll (dopo aver verificato che non esistano oggetti o blocchi), recuperare informazioni sulla DLL proxy e registrare e annullare la registrazione della DLL del proxy.</span><span class="sxs-lookup"><span data-stu-id="eb7f5-109">COM uses these functions to create a class factory, unload DLLs (after making sure that no objects or locks exist), retrieve information about the proxy DLL, and to self-register and unregister the proxy DLL.</span></span> <span data-ttu-id="eb7f5-110">Per sfruttare i vantaggi di queste funzioni predefinite, è necessario richiamare l'opzione Cpreprocessor/D (o-D) quando si compilano i file dlldata. c e \_ p. c di esempio, come illustrato nel makefile seguente:</span><span class="sxs-lookup"><span data-stu-id="eb7f5-110">To take advantage of these predefined functions, you need to invoke the Cpreprocessor /D (or -D) option when you compile the Dlldata.c and Example\_p.c files, as shown in the following makefile:</span></span>

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcndr.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(ORIXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

<span data-ttu-id="eb7f5-111">Se non si specificano queste definizioni per il preprocessore in fase di compilazione, queste funzioni non vengono definite automaticamente.</span><span class="sxs-lookup"><span data-stu-id="eb7f5-111">If you do not specify these preprocessor definitions at compile time, these functions are not automatically defined.</span></span> <span data-ttu-id="eb7f5-112">(Ovvero, le macro in Rpcproxy. c si espandono su Nothing). È necessario che siano stati definiti in modo esplicito in un altro file di origine, il cui modulo verrebbe incluso anche nel collegamento e nella compilazione finali nella riga di comando del compilatore C.</span><span class="sxs-lookup"><span data-stu-id="eb7f5-112">(That is, the macros in Rpcproxy.c expand to nothing.) You would have to have defined them explicitly in another source file, whose module would also be included in the final linking and compilation on the C compiler command line.</span></span>

<span data-ttu-id="eb7f5-113">Quando \_ \_ si definisce la dll del proxy di registrazione, Rpcproxy. h fornisce un ulteriore controllo di compilazione condizionale con proxy \_ CLSID =*GUID*, il \_ CLSID proxy \_ è =*valore esplicito GUID* e \_ prefisso voce =*stringa prefisso*.</span><span class="sxs-lookup"><span data-stu-id="eb7f5-113">When REGISTER\_PROXY\_DLL is defined, Rpcproxy.h provides for additional conditional compilation control with PROXY\_CLSID=*guid*, PROXY\_CLSID\_IS=*explicit value of guid*, and ENTRY\_PREFIX=*prefix string*.</span></span> <span data-ttu-id="eb7f5-114">Queste definizioni di macro sono descritte più dettagliatamente nelle [definizioni del compilatore C per proxy/stub](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) in MIDL Programmer ' s Guide.</span><span class="sxs-lookup"><span data-stu-id="eb7f5-114">These macro definitions are described in greater detail in [C-Compiler Definitions for Proxy/Stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) in the MIDL Programmer's Guide.</span></span>

## <a name="manually-registering-the-proxy-dll"></a><span data-ttu-id="eb7f5-115">Registrazione manuale della DLL proxy</span><span class="sxs-lookup"><span data-stu-id="eb7f5-115">Manually Registering the Proxy DLL</span></span>

<span data-ttu-id="eb7f5-116">Se per qualche motivo non è possibile usare le routine di registrazione stub proxy predefinite, è possibile registrare manualmente la DLL aggiungendo le voci seguenti al registro di sistema, usando Regedt32.exe.</span><span class="sxs-lookup"><span data-stu-id="eb7f5-116">If for some reason you cannot use the default proxy stub registration routines, you can manually register the DLL by adding the following entries to the system registry, using Regedt32.exe.</span></span>

```
HKEY_CLASSES_ROOT
   Interface
      iid
         (Default) = ICustomInterfaceName
         ProxyStubClsid32 = {clsid}
```

```
HKEY_CLASSES_ROOT
   CLSID
      clsid
         (Default) = ICustomInterfaceName_PSFactory
         InprocServer32 = proxstub.dll
```

## <a name="related-topics"></a><span data-ttu-id="eb7f5-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eb7f5-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb7f5-118">Definizioni del compilatore C per proxy/stub</span><span class="sxs-lookup"><span data-stu-id="eb7f5-118">C-Compiler Definitions for Proxy/Stubs</span></span>](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[<span data-ttu-id="eb7f5-119">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="eb7f5-119">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="eb7f5-120">Registrazione automatica</span><span class="sxs-lookup"><span data-stu-id="eb7f5-120">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 