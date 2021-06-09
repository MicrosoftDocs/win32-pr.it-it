---
title: Compilazione e registrazione di una DLL proxy
description: Se si sceglie il marshalling proxy/stub per l'applicazione, i file con estensione c e h generati da MIDL devono essere compilati e collegati per creare una DLL proxy e tale DLL deve essere immessa nel Registro di sistema in modo che i client possano individuare le interfacce.
ms.assetid: 939e6eed-2a2d-4d90-8fbb-c07142e7ba70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d4cafbe2be56d9e9a02a451e3daf905496c424
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826806"
---
# <a name="building-and-registering-a-proxy-dll"></a><span data-ttu-id="9f5cf-103">Compilazione e registrazione di una DLL proxy</span><span class="sxs-lookup"><span data-stu-id="9f5cf-103">Building and Registering a Proxy DLL</span></span>

<span data-ttu-id="9f5cf-104">Se si sceglie il marshalling proxy/stub per l'applicazione, i file con estensione c e h generati da MIDL devono essere compilati e collegati per creare una DLL proxy e tale DLL deve essere immessa nel Registro di sistema in modo che i client possano individuare le interfacce.</span><span class="sxs-lookup"><span data-stu-id="9f5cf-104">If you chose proxy/stub marshaling for your application, the .c and .h files that MIDL generated must be compiled and linked to create a proxy DLL, and that DLL must be entered into the system registry so that clients can locate your interfaces.</span></span> <span data-ttu-id="9f5cf-105">Il file dlldata.c generato da MIDL contiene le routine necessarie e altre informazioni per compilare e registrare una DLL proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="9f5cf-105">The MIDL-generated file Dlldata.c contains the necessary routines and other information to build and register a proxy/stub DLL.</span></span>

<span data-ttu-id="9f5cf-106">Il primo passaggio per la compilazione della DLL consiste nello scrivere un file di definizione del modulo per il linker, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="9f5cf-106">The first step in building the DLL is to write a module definition file for the linker, as shown in the following example:</span></span>

``` syntax
LIBRARY        example.dll
DESCRIPTION    'generic proxy/stub DLL'
EXPORTS        DllGetClassObject      @1 PRIVATE
               DllCanUnloadNow        @2 PRIVATE
               DllRegisterServer      @4 PRIVATE
               DllUnregisterServer    @5 PRIVATE
 
```

<span data-ttu-id="9f5cf-107">In alternativa, è possibile specificare queste funzioni esportate nella riga di comando LINK del makefile.</span><span class="sxs-lookup"><span data-stu-id="9f5cf-107">Alternatively, you can specify these exported functions on the LINK command line of your makefile.</span></span>

<span data-ttu-id="9f5cf-108">Le funzioni esportate vengono dichiarate in Rpcproxy.h, incluso in Dlldata.c, e le implementazioni predefinite fanno parte della libreria di runtime RPC.</span><span class="sxs-lookup"><span data-stu-id="9f5cf-108">The exported functions are declared in Rpcproxy.h, which Dlldata.c includes, and default implementations are part of the RPC run-time library.</span></span> <span data-ttu-id="9f5cf-109">COM usa queste funzioni per creare un class factory, scaricare le DLL (dopo aver verificato che non esistano oggetti o blocchi), recuperare informazioni sulla DLL proxy e per autoregistrare e annullare la registrazione della DLL proxy.</span><span class="sxs-lookup"><span data-stu-id="9f5cf-109">COM uses these functions to create a class factory, unload DLLs (after making sure that no objects or locks exist), retrieve information about the proxy DLL, and to self-register and unregister the proxy DLL.</span></span> <span data-ttu-id="9f5cf-110">Per sfruttare queste funzioni predefinite, è necessario richiamare l'opzione Cpreprocessor /D (o -D) quando si compilano i file Dlldata.c e Example p.c, come illustrato nel \_ makefile seguente:</span><span class="sxs-lookup"><span data-stu-id="9f5cf-110">To take advantage of these predefined functions, you need to invoke the Cpreprocessor /D (or -D) option when you compile the Dlldata.c and Example\_p.c files, as shown in the following makefile:</span></span>

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
proxy.dll : $(PROXYSTUBOBJS) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
 
```

<span data-ttu-id="9f5cf-111">Se non si specificano queste definizioni del preprocessore in fase di compilazione, queste funzioni non vengono definite automaticamente.</span><span class="sxs-lookup"><span data-stu-id="9f5cf-111">If you do not specify these preprocessor definitions at compile time, these functions are not automatically defined.</span></span> <span data-ttu-id="9f5cf-112">Ovvero, le macro in Rpcproxy.c non si espandono fino a nulla. È necessario averle definite in modo esplicito in un altro file di origine, il cui modulo sarebbe stato incluso anche nel collegamento e nella compilazione finali nella riga di comando del compilatore C.</span><span class="sxs-lookup"><span data-stu-id="9f5cf-112">(That is, the macros in Rpcproxy.c expand to nothing.) You would have to have defined them explicitly in another source file, whose module would also be included in the final linking and compilation on the C compiler command line.</span></span>

<span data-ttu-id="9f5cf-113">Quando viene definita la DLL REGISTER PROXY, Rpcproxy.h fornisce un controllo di compilazione condizionale aggiuntivo con \_ \_ \_ CLSID PROXY=*guid,* \_ CLSID PROXY IS= \_ valore \_ esplicito di guid e ENTRY PREFIX= stringa di prefisso .</span><span class="sxs-lookup"><span data-stu-id="9f5cf-113">When REGISTER\_PROXY\_DLL is defined, Rpcproxy.h provides for additional conditional compilation control with PROXY\_CLSID=*guid*, PROXY\_CLSID\_IS=*explicit value of guid*, and ENTRY\_PREFIX=*prefix string*.</span></span> <span data-ttu-id="9f5cf-114">Queste definizioni di macro sono descritte in modo più dettagliato in Definizioni del compilatore [C per proxy/stub](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) nella Guida per programmatori MIDL.</span><span class="sxs-lookup"><span data-stu-id="9f5cf-114">These macro definitions are described in greater detail in [C-Compiler Definitions for Proxy/Stubs](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs) in the MIDL Programmer's Guide.</span></span>

## <a name="manually-registering-the-proxy-dll"></a><span data-ttu-id="9f5cf-115">Registrazione manuale della DLL del proxy</span><span class="sxs-lookup"><span data-stu-id="9f5cf-115">Manually Registering the Proxy DLL</span></span>

<span data-ttu-id="9f5cf-116">Se per qualche motivo non è possibile usare le routine di registrazione predefinite dello stub proxy, è possibile registrare manualmente la DLL aggiungendo le voci seguenti al Registro di sistema usando Regedt32.exe.</span><span class="sxs-lookup"><span data-stu-id="9f5cf-116">If for some reason you cannot use the default proxy stub registration routines, you can manually register the DLL by adding the following entries to the system registry, using Regedt32.exe.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="9f5cf-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9f5cf-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f5cf-118">Definizioni del compilatore C per proxy/stub</span><span class="sxs-lookup"><span data-stu-id="9f5cf-118">C-Compiler Definitions for Proxy/Stubs</span></span>](/windows/desktop/Midl/c-compiler-definitions-for-proxy-stubs)
</dt> <dt>

[<span data-ttu-id="9f5cf-119">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="9f5cf-119">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="9f5cf-120">Registrazione automatica</span><span class="sxs-lookup"><span data-stu-id="9f5cf-120">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 
