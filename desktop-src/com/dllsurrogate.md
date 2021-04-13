---
title: DllSurrogate
description: Consente l'esecuzione di server DLL in un processo surrogato. Se viene specificata una stringa vuota, viene utilizzato il surrogato fornito dal sistema; in caso contrario, il valore specifica il percorso del surrogato da usare.
ms.assetid: ae02d828-9cdb-4faa-8fa9-971da97e27b1
keywords:
- Valore DllSurrogate del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9854f3c4e4390d64d97c8ab829ac2e7fe34488e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399770"
---
# <a name="dllsurrogate"></a><span data-ttu-id="1ee64-105">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="1ee64-105">DllSurrogate</span></span>

<span data-ttu-id="1ee64-106">Consente l'esecuzione di server DLL in un processo surrogato.</span><span class="sxs-lookup"><span data-stu-id="1ee64-106">Enables DLL servers to run in a surrogate process.</span></span> <span data-ttu-id="1ee64-107">Se viene specificata una stringa vuota, viene utilizzato il surrogato fornito dal sistema; in caso contrario, il valore specifica il percorso del surrogato da usare.</span><span class="sxs-lookup"><span data-stu-id="1ee64-107">If an empty string is specified, the system-supplied surrogate is used; otherwise, the value specifies the path of the surrogate to be used.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="1ee64-108">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="1ee64-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogate = path
```

## <a name="remarks"></a><span data-ttu-id="1ee64-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ee64-109">Remarks</span></span>

<span data-ttu-id="1ee64-110">Si tratta di un valore **reg \_ SZ** che specifica che la classe è una dll che deve essere attivata in un processo surrogato e il processo surrogato da usare.</span><span class="sxs-lookup"><span data-stu-id="1ee64-110">This is a **REG\_SZ** value that specifies that the class is a DLL that is to be activated in a surrogate process, and the surrogate process to be used.</span></span> <span data-ttu-id="1ee64-111">Per usare il processo surrogato generico fornito dal sistema, impostare il *percorso* su una stringa vuota o su **null**.</span><span class="sxs-lookup"><span data-stu-id="1ee64-111">To use the system-supplied generic surrogate process, set *path* to an empty string or **NULL**.</span></span> <span data-ttu-id="1ee64-112">Per specificare un altro processo surrogato, impostare *path* sul percorso del surrogato.</span><span class="sxs-lookup"><span data-stu-id="1ee64-112">To specify another surrogate process, set *path* to the path of the surrogate.</span></span> <span data-ttu-id="1ee64-113">Come nella specifica del percorso di un server sotto la chiave [**LocalServer32**](localserver32.md) , non è necessario specificare un percorso completo.</span><span class="sxs-lookup"><span data-stu-id="1ee64-113">As in the specification of the path of a server under the [**LocalServer32**](localserver32.md) key, a full path specification is not necessary.</span></span> <span data-ttu-id="1ee64-114">È necessario scrivere il surrogato per comunicare correttamente con il servizio DCOM come descritto in [scrittura di un surrogato personalizzato](writing-a-custom-surrogate.md).</span><span class="sxs-lookup"><span data-stu-id="1ee64-114">The surrogate must be written to properly communicate with the DCOM service as described in [Writing a Custom Surrogate](writing-a-custom-surrogate.md).</span></span>

<span data-ttu-id="1ee64-115">Il valore **DllSurrogate** deve essere presente affinché un server DLL venga attivato in un surrogato.</span><span class="sxs-lookup"><span data-stu-id="1ee64-115">The **DllSurrogate** value must be present for a DLL server to be activated in a surrogate.</span></span> <span data-ttu-id="1ee64-116">L'attivazione fa riferimento a una chiamata a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **CoCreateInstanceEx**, [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)o [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span><span class="sxs-lookup"><span data-stu-id="1ee64-116">Activation refers to a call to [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex), **CoCreateInstanceEx**, [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile), [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage), or [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject).</span></span> <span data-ttu-id="1ee64-117">L'esecuzione di dll in un processo surrogato offre i vantaggi di un'implementazione eseguibile, tra cui l'isolamento degli errori, la possibilità di gestire più client simultaneamente e consente al server di fornire servizi ai client remoti in un ambiente distribuito.</span><span class="sxs-lookup"><span data-stu-id="1ee64-117">Running DLLs in a surrogate process provides the benefits of an executable implementation, including fault isolation, the ability to serve multiple clients simultaneously, and allowing the server to provide services to remote clients in a distributed environment.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ee64-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1ee64-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ee64-119">**CoRegisterSurrogate**</span><span class="sxs-lookup"><span data-stu-id="1ee64-119">**CoRegisterSurrogate**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[<span data-ttu-id="1ee64-120">Surrogati DLL</span><span class="sxs-lookup"><span data-stu-id="1ee64-120">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> <dt>

[<span data-ttu-id="1ee64-121">**DllSurrogateExecutable**</span><span class="sxs-lookup"><span data-stu-id="1ee64-121">**DllSurrogateExecutable**</span></span>](dllsurrogateexecutable.md)
</dt> <dt>

[<span data-ttu-id="1ee64-122">**ISurrogate**</span><span class="sxs-lookup"><span data-stu-id="1ee64-122">**ISurrogate**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 