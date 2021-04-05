---
title: Definizioni del compilatore C per proxy/stub
description: Il file di intestazione Rpcproxy. h include le definizioni di macro seguenti, ognuna delle quali può risultare utile quando si compila un'applicazione COM distribuita. Queste macro vengono richiamate con l'opzione del preprocessore/D (o-D) in fase di compilazione C.
ms.assetid: 697f0b63-76ae-410d-8bbf-bb95295ffba9
keywords:
- MIDL compilatore MIDL, compilatore C, definizioni per proxy/stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1504c600c3f86a934ab3daa132b041c7310af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045110"
---
# <a name="c-compiler-definitions-for-proxystubs"></a><span data-ttu-id="c7e61-105">Definizioni del compilatore C per proxy/stub</span><span class="sxs-lookup"><span data-stu-id="c7e61-105">C-Compiler Definitions for Proxy/Stubs</span></span>

<span data-ttu-id="c7e61-106">Il file di intestazione Rpcproxy. h include le definizioni di macro seguenti, ognuna delle quali può risultare utile quando si compila un'applicazione COM distribuita.</span><span class="sxs-lookup"><span data-stu-id="c7e61-106">The header file Rpcproxy.h includes the following macro definitions, each of which may be convenient when building distributed COM application.</span></span> <span data-ttu-id="c7e61-107">Queste macro vengono richiamate con l'opzione del preprocessore [**/d**](-d.md) (o-D) in fase di compilazione C.</span><span class="sxs-lookup"><span data-stu-id="c7e61-107">These macros are invoked with the [**/D**](-d.md) (or -D) preprocessor switch at the C-compile time.</span></span>



| <span data-ttu-id="c7e61-108">MACRO</span><span class="sxs-lookup"><span data-stu-id="c7e61-108">MACRO</span></span>                                                                                                                                                                                           | <span data-ttu-id="c7e61-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7e61-109">Description</span></span>                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e61-110">Registra \_ \_ dll proxy</span><span class="sxs-lookup"><span data-stu-id="c7e61-110">REGISTER\_PROXY\_DLL</span></span>                                                                                                                                                                            | <span data-ttu-id="c7e61-111">Genera funzioni **DllMain**, **DllRegisterServer** e **DllUnregisterServer** per la registrazione automatica di una DLL proxy.</span><span class="sxs-lookup"><span data-stu-id="c7e61-111">Generates **DllMain**, **DllRegisterServer**, and **DllUnregisterServer** functions for automatically registering a proxy DLL.</span></span>                                                                                       |
| <span data-ttu-id="c7e61-112">\_CLSID proxy =<clsid></span><span class="sxs-lookup"><span data-stu-id="c7e61-112">PROXY\_CLSID=<clsid></span></span>                                                                                                                                                                      | <span data-ttu-id="c7e61-113">Specifica un identificatore di classe per il server.</span><span class="sxs-lookup"><span data-stu-id="c7e61-113">Specifies a class identifier for the server.</span></span> <span data-ttu-id="c7e61-114">Se questa macro non è definita, il CLSID predefinito è il primo identificatore di interfaccia rilevato dal compilatore MIDL nella specifica IDL per il server proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="c7e61-114">If this macro is not defined, the default CLSID is the first interface identifier that the MIDL compiler encounters in the IDL specification for the Proxy/Stub server.</span></span> |
| <span data-ttu-id="c7e61-115">Il \_ CLSID \_ proxy è = {*0x 8hexdigits*, 0x *4hexdigits*, 0x *4hexdigits*, {0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x *2hexdigits*, 0x 2hexdigits, 0x 2hexdigits, 0x 2hexdigits, 0x *2hexdigits*,}}</span><span class="sxs-lookup"><span data-stu-id="c7e61-115">PROXY\_CLSID\_IS={0x *8hexdigits*, 0x *4hexdigits*,0x *4hexdigits*, {0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*, 0x *2hexdigits*,0x *2hexdigits*,}}</span></span> | <span data-ttu-id="c7e61-116">Specifica il valore dell'identificatore di classe del server in formato esadecimale binario.</span><span class="sxs-lookup"><span data-stu-id="c7e61-116">Specifies the value of the server's class identifier in binary hex format.</span></span>                                                                                                                                           |



 

<span data-ttu-id="c7e61-117">Definendo la macro **Register \_ proxy \_ dll** quando si compila dlldata. c, la dll di marshalling del proxy/stub includerà automaticamente le definizioni predefinite per le funzioni **DllMain**, **DllRegisterServer** e **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="c7e61-117">By defining the **REGISTER\_PROXY\_DLL** macro when compiling Dlldata.c, your proxy/stub marshaling DLL will automatically include default definitions for the **DllMain**, **DllRegisterServer**, and **DllUnregisterServer** functions.</span></span> <span data-ttu-id="c7e61-118">È possibile usare queste funzioni per registrare autonomamente la DLL del proxy nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c7e61-118">You can use these functions to self-register your proxy DLL in the system registry.</span></span>

<span data-ttu-id="c7e61-119">Questo codice di registrazione predefinito usa il GUID della prima interfaccia rilevata come CLSID per la registrazione dell'intero server DLL proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="c7e61-119">This default registration code uses the GUID of the first interface encountered as the CLSID for registering the entire proxy/stub DLL server.</span></span> <span data-ttu-id="c7e61-120">COM in un secondo momento utilizza questo CLSID per individuare e caricare il server proxy/stub compilato per il marshalling di qualsiasi interfaccia registrata dal server per la gestione.</span><span class="sxs-lookup"><span data-stu-id="c7e61-120">COM later uses this CLSID to locate and load the compiled proxy/stub server for the marshaling of any of the interfaces the server is registered to handle.</span></span> <span data-ttu-id="c7e61-121">Quando un'applicazione esegue una chiamata al metodo di interfaccia che supera i limiti dei thread, dei processi o dei computer, COM utilizza la voce del registro di sistema Identifier per individuare la voce del registro di sistema CLSID per il server di marshalling del proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="c7e61-121">When an application makes an interface method call that crosses thread, process, or computer boundaries, COM uses the interface identifier registry entry to locate the CLSID registry entry for the proxy/stub marshaling server.</span></span> <span data-ttu-id="c7e61-122">USA quindi questo CLSID per caricare il server, se non è già caricato, in modo che sia possibile effettuare il marshalling della chiamata di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="c7e61-122">It then uses this CLSID to load the server (if it isn't already loaded) so that the interface call can then be marshaled.</span></span>

<span data-ttu-id="c7e61-123">Utilizzare la macro **proxy \_ CLSID** = <clsid> quando si desidera specificare in modo esplicito il CLSID del server proxy/stub anziché basarsi sul CLSID predefinito.</span><span class="sxs-lookup"><span data-stu-id="c7e61-123">Use the **PROXY\_CLSID**=<clsid> macro when you want to explicitly specify the proxy/stub server's CLSID rather than rely on the default CLSID.</span></span> <span data-ttu-id="c7e61-124">Se, ad esempio, si compila una DLL di marshalling standard come server COM in-process, oppure se è necessario definire una proprietà **DllMain** personalizzata per gestire la \_ connessione al processo dll \_ .</span><span class="sxs-lookup"><span data-stu-id="c7e61-124">For example, if you are building a standard marshaling DLL as your own in-process COM server, or if you need to define your own **DllMain** to handle DLL\_PROCESS\_ATTACH.</span></span>

<span data-ttu-id="c7e61-125">Use **proxy \_ CLSID \_ is**= macro anziché **proxy \_ CLSID** per definire il valore del CLSID nel formato esadecimale binario utilizzato dalla macro del **\_ GUID define** .</span><span class="sxs-lookup"><span data-stu-id="c7e61-125">Use **PROXY\_CLSID\_IS**= macro instead of **PROXY\_CLSID** to define the value of the CLSID in the binary hexadecimal format that the **DEFINE\_GUID** macro uses.</span></span>

<span data-ttu-id="c7e61-126">Si noti inoltre che quando viene eseguita la funzione **DllRegisterServer** predefinita, viene registrato il server con ThreadingModel = both.</span><span class="sxs-lookup"><span data-stu-id="c7e61-126">Also note that when the default **DllRegisterServer** function runs, it registers the server with ThreadingModel=Both.</span></span>

<span data-ttu-id="c7e61-127">Nell'esempio di makefile seguente vengono usate le macro **Register \_ proxy \_ dll** e **proxy \_ CLSID**= Macros:</span><span class="sxs-lookup"><span data-stu-id="c7e61-127">The following makefile example uses the **REGISTER\_PROXY\_DLL** and **PROXY\_CLSID**= macros:</span></span>

``` syntax
example.h example.tlb example_p.c example_i.c dlldata.c : example.idl
    midl example.idl
dlldata.obj : dlldata.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL dlldata.c
example.obj : example_p.c
    CL /c /DWIN32 /DREGISTER_PROXY_DLL \
    /DPROXY_CLSID=7a98c250-6808-11cf-b73b-00aa00b677a7
example_p.c
iids.obj : example_i.c
PROXYSTUBOBJS = dlldata.obj example.obj iids.obj
PROXYSTUBLIBS = kernel32.lib rpcns4.lib rpcrt4.lib uuid.lib
proxy.dll : $(PROXYSTUBOBJX) example.def
    link /dll /out:proxy.dll /def:example.def
        $(PROXYSTUBOBJS) $(PROXYSTUBLIBS)
    regsvr32 /s proxy.dll
```

<span data-ttu-id="c7e61-128">Per ulteriori informazioni sull'opzione [**/d**](-d.md) preprocessore, vedere la documentazione del compilatore C.</span><span class="sxs-lookup"><span data-stu-id="c7e61-128">For more information on the [**/D**](-d.md) preprocessor option, see your C compiler documentation.</span></span>

 

 




