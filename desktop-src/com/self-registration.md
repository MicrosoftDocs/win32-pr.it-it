---
title: Self-Registration
description: La registrazione automatica è il mezzo standard attraverso il quale un modulo server può creare un pacchetto delle proprie operazioni del registro di sistema, sia di registrazione che di annullamento della registrazione, nel modulo stesso.
ms.assetid: fb5dcb2b-b0e3-4f37-a8e7-b84b9a265227
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c95d422213b8e33ac89b89408ed95724f0769b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474355"
---
# <a name="self-registration"></a><span data-ttu-id="d9bb5-103">Self-Registration</span><span class="sxs-lookup"><span data-stu-id="d9bb5-103">Self-Registration</span></span>

<span data-ttu-id="d9bb5-104">Poiché il software dei componenti continua a crescere come mercato, saranno presenti più istanze in cui un utente ottiene un nuovo componente software come singolo modulo DLL o EXE, ad esempio quando Scarica un nuovo componente da un servizio online o ne riceve uno da un amico su un disco floppy.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-104">As component software continues to grow as a market, there will be more and more instances where a user obtains a new software component as a single DLL or EXE module, such as when downloading a new component from an on-line service or receiving one from a friend on a floppy disk.</span></span> <span data-ttu-id="d9bb5-105">In questi casi, non è pratico richiedere all'utente di eseguire una lunga procedura di installazione o programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-105">In these cases, it is not practical to require the user to go through a lengthy installation procedure or setup program.</span></span> <span data-ttu-id="d9bb5-106">Oltre ai problemi relativi alle licenze, che vengono gestiti tramite [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), una procedura di installazione crea in genere le voci del registro di sistema necessarie per l'esecuzione corretta di un componente nel contesto com e OLE.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-106">Besides the licensing issues, which are handled through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), an installation procedure typically creates the necessary registry entries for a component to run properly in the COM and OLE context.</span></span>

<span data-ttu-id="d9bb5-107">La registrazione automatica è il mezzo standard attraverso il quale un modulo server può creare un pacchetto delle proprie operazioni del registro di sistema, sia di registrazione che di annullamento della registrazione, nel modulo stesso.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-107">Self-registration is the standard means through which a server module can package its own registry operations, both registration and unregistration, into the module itself.</span></span> <span data-ttu-id="d9bb5-108">Quando viene usato con le licenze gestite tramite [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), un server può diventare un modulo completamente autonomo senza necessità di programmi di installazione esterni o file reg.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-108">When used with licensing handled through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2), a server can become an entirely self-contained module with no need for external installation programs or .reg files.</span></span>

<span data-ttu-id="d9bb5-109">Qualsiasi modulo di registrazione automatica, DLL o EXE, deve prima includere una stringa "OleSelfRegister" nella sezione [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) della relativa risorsa di informazioni sulla versione, come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-109">Any self-registering module, DLL or EXE, should first include an "OleSelfRegister" string in the [StringFileInfo](/windows/desktop/menurc/stringfileinfo-block) section of its version information resource, as shown here.</span></span>

``` syntax
VS_VERSION_INFO VERSIONINFO 
 
 ... 
 
 BEGIN 
   BLOCK "StringFileInfo" 
    BEGIN 
#ifdef UNICODE 
     BLOCK "040904B0" // Lang=US English, CharSet=Unicode 
#else 
     BLOCK "040904E4" // Lang=US English, CharSet=Windows Multilingual 
#endif 
      BEGIN 
       ... 
       VALUE "OLESelfRegister", "\0" 
      END 
 
   ... 
 
   END 
 
 ... 
 
 END 
 
```

<span data-ttu-id="d9bb5-110">L'esistenza di questi dati consente a qualsiasi parte interessata, ad esempio un'applicazione che desidera integrare questo nuovo componente, di determinare se il server supporta la registrazione automatica senza dover prima caricare la DLL o EXE.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-110">The existence of this data allows any interested party, such as an application that wishes to integrate this new component, to determine whether the server supports self-registration without having to load the DLL or EXE first.</span></span>

<span data-ttu-id="d9bb5-111">Se il server è incluso in un modulo DLL, è necessario che la DLL esporti le funzioni [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span><span class="sxs-lookup"><span data-stu-id="d9bb5-111">If the server is packaged in a DLL module, the DLL must export the functions [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver) and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="d9bb5-112">Qualsiasi applicazione che desidera indicare al server di registrarsi, ovvero tutti i relativi CLSID e ID della libreria dei tipi, può ottenere un puntatore a **DllRegisterServer** tramite la funzione [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="d9bb5-112">Any application that wishes to instruct the server to register itself (that is, all its CLSIDs and type library IDs) can obtain a pointer to **DllRegisterServer** through the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function.</span></span> <span data-ttu-id="d9bb5-113">In **DllRegisterServer**, la dll crea tutte le voci del registro di sistema necessarie, archiviando il percorso corretto della dll per tutte le voci [InprocServer32](inprocserver32.md) o [InprocHandler32](inprochandler32.md) .</span><span class="sxs-lookup"><span data-stu-id="d9bb5-113">Within **DllRegisterServer**, the DLL creates all its necessary registry entries, storing the correct path to the DLL for all [InprocServer32](inprocserver32.md) or [InprocHandler32](inprochandler32.md) entries.</span></span>

<span data-ttu-id="d9bb5-114">Quando un'applicazione desidera rimuovere il componente dal sistema, è necessario annullare la registrazione del componente chiamando [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span><span class="sxs-lookup"><span data-stu-id="d9bb5-114">When an application wishes to remove the component from the system, it should unregister that component by calling [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver).</span></span> <span data-ttu-id="d9bb5-115">All'interno di questa chiamata, il server rimuove esattamente le voci create in precedenza in [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span><span class="sxs-lookup"><span data-stu-id="d9bb5-115">Within this call, the server removes exactly those entries it previously created in [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver).</span></span> <span data-ttu-id="d9bb5-116">Il server non deve rimuovere in modo cieco tutte le voci per le relative classi perché altri software potrebbero avere archiviato voci aggiuntive, ad esempio una chiave [Treats](treatas.md) .</span><span class="sxs-lookup"><span data-stu-id="d9bb5-116">The server should not blindly remove all entries for its classes because other software may have stored additional entries, such as a [TreatAs](treatas.md) key.</span></span>

<span data-ttu-id="d9bb5-117">Se il server è incluso in un modulo EXE, l'applicazione che vuole registrare il server avvia il server EXE con l'argomento della riga di comando **/regserver** o **-regserver** (senza distinzione tra maiuscole e minuscole).</span><span class="sxs-lookup"><span data-stu-id="d9bb5-117">If the server is packaged in an EXE module, the application wishing to register the server launches the EXE server with the command-line argument **/RegServer** or **-RegServer** (case-insensitive).</span></span> <span data-ttu-id="d9bb5-118">Se l'applicazione vuole annullare la registrazione del server, avvia il file EXE con l'argomento della riga di comando **l'opzione/unregserver** o **-unregserver**.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-118">If the application wishes to unregister the server, it launches the EXE with the command-line argument **/UnregServer** or **-UnregServer**.</span></span> <span data-ttu-id="d9bb5-119">Il file EXE con registrazione automatica rileva questi argomenti della riga di comando e richiama le stesse operazioni di una DLL all'interno di [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)e [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver), rispettivamente, registrando il percorso del modulo in [LocalServer32](localserver32.md) anziché **InprocServer32** o **InprocHandler32**.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-119">The self-registering EXE detects these command-line arguments and invokes the same operations as a DLL would within [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)and [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver), respectively, registering its module path under [LocalServer32](localserver32.md) instead of **InprocServer32** or **InprocHandler32**.</span></span>

<span data-ttu-id="d9bb5-120">Il server deve registrare il percorso completo del percorso di installazione del modulo DLL o EXE per le rispettive chiavi **InprocServer32**, **InprocHandler32** e **LocalServer32** nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d9bb5-120">The server must register the full path to the installation location of the DLL or EXE module for their respective **InprocServer32**, **InprocHandler32**, and **LocalServer32** keys in the registry.</span></span> <span data-ttu-id="d9bb5-121">Il percorso del modulo è facilmente ottenibile tramite la funzione [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .</span><span class="sxs-lookup"><span data-stu-id="d9bb5-121">The module path is easily obtained through the [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9bb5-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9bb5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9bb5-123">Installazione come applicazione di servizio</span><span class="sxs-lookup"><span data-stu-id="d9bb5-123">Installing as a Service Application</span></span>](installing-as-a-service-application.md)
</dt> <dt>

[<span data-ttu-id="d9bb5-124">Registrazione di una classe durante l'installazione</span><span class="sxs-lookup"><span data-stu-id="d9bb5-124">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="d9bb5-125">Registrazione di un server EXE in esecuzione</span><span class="sxs-lookup"><span data-stu-id="d9bb5-125">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
</dt> <dt>

[<span data-ttu-id="d9bb5-126">Registrazione di oggetti nella tabella ROT</span><span class="sxs-lookup"><span data-stu-id="d9bb5-126">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> </dl>

 

 