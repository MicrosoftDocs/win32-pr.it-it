---
title: Binding con GetObject e ADsGetObject
description: Le funzioni GetObject e ADsGetObject vengono utilizzate per l'associazione agli oggetti del servizio directory senza autenticazione.
ms.assetid: 15d8116a-8ec1-48b5-bf62-411fdff7c8b8
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, uso, associazione con GetObject e ADsGetObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f61d5aba2c2c49e97ddcfc0f727d0cd4c17a164
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963444"
---
# <a name="binding-with-getobject-and-adsgetobject"></a><span data-ttu-id="46e8e-104">Binding con GetObject e ADsGetObject</span><span class="sxs-lookup"><span data-stu-id="46e8e-104">Binding With GetObject and ADsGetObject</span></span>

<span data-ttu-id="46e8e-105">Le funzioni **GetObject** e [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) vengono utilizzate per l'associazione agli oggetti del servizio directory senza autenticazione.</span><span class="sxs-lookup"><span data-stu-id="46e8e-105">The **GetObject** and [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) functions are used to bind to directory service objects with no authentication.</span></span> <span data-ttu-id="46e8e-106">L'applicazione non deve fornire le credenziali per l'accesso ai dati del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="46e8e-106">The application is not required to provide credentials when accessing directory service data.</span></span> <span data-ttu-id="46e8e-107">ADSI usa il contesto di sicurezza del thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="46e8e-107">ADSI uses the security context of the calling thread.</span></span> <span data-ttu-id="46e8e-108">Tuttavia, se l'autenticazione protetta non riesce, ADSI tenta di eseguire un'associazione semplice con un nome utente e una password null null.</span><span class="sxs-lookup"><span data-stu-id="46e8e-108">However, if secure authentication fails, ADSI attempts to perform a simple bind with a null user name and null password.</span></span> <span data-ttu-id="46e8e-109">Se l'associazione semplice ha esito positivo, il contesto utente per l'associazione è Guest.</span><span class="sxs-lookup"><span data-stu-id="46e8e-109">If the simple bind succeeds, the user context for the binding is Guest.</span></span> <span data-ttu-id="46e8e-110">Un'associazione semplice usa l'autenticazione in testo non crittografato.</span><span class="sxs-lookup"><span data-stu-id="46e8e-110">A simple bind uses plaintext authentication.</span></span> <span data-ttu-id="46e8e-111">Poiché il nome utente o la password non vengono trasmessi in rete, questo non è un problema di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="46e8e-111">Because no user name or password is transmitted over the network, this is not a security issue.</span></span>

<span data-ttu-id="46e8e-112">La funzione **GetObject** viene utilizzata per l'associazione agli oggetti servizio directory in linguaggi che supportano l'automazione, ad esempio Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="46e8e-112">The **GetObject** function is used to bind to directory service objects in languages that support automation, such as Visual Basic.</span></span> <span data-ttu-id="46e8e-113">La funzione **GetObject** richiede una stringa del moniker.</span><span class="sxs-lookup"><span data-stu-id="46e8e-113">The **GetObject** function requires a moniker string.</span></span> <span data-ttu-id="46e8e-114">In ADSI la stringa di associazione è la stringa del moniker.</span><span class="sxs-lookup"><span data-stu-id="46e8e-114">In ADSI, the binding string is the moniker string.</span></span>

<span data-ttu-id="46e8e-115">In linguaggi che non supportano direttamente l'automazione, ad esempio C o C++, ADSI fornisce la funzione [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) per l'associazione agli oggetti del servizio directory.</span><span class="sxs-lookup"><span data-stu-id="46e8e-115">In languages that do not directly support automation, such as C or C++, ADSI provides the [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function to bind to directory service objects.</span></span> <span data-ttu-id="46e8e-116">In alternativa, è possibile usare le funzioni [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) e [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) per ottenere lo stesso risultato di **GetObject**.</span><span class="sxs-lookup"><span data-stu-id="46e8e-116">Alternatively, the [**MkParseDisplayName**](/windows/win32/api/objbase/nf-objbase-mkparsedisplayname) and [**MkParseDisplayNameEx**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) functions can be used to achieve the same result as **GetObject**.</span></span>

<span data-ttu-id="46e8e-117">Per un servizio in esecuzione con l'account LocalSystem, il contesto di sicurezza utilizzato da **GetObject** e [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) dipende dal computer in cui è in esecuzione il servizio.</span><span class="sxs-lookup"><span data-stu-id="46e8e-117">For a service running under the LocalSystem account, the security context used by **GetObject** and [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) depends on the computer on which the service is running.</span></span> <span data-ttu-id="46e8e-118">Se il servizio è in esecuzione come LocalSystem in un controller di dominio, il servizio dispone di accesso completo a livello di sistema per Active Directory.</span><span class="sxs-lookup"><span data-stu-id="46e8e-118">If the service is running as LocalSystem on a domain controller, the service has full system-level access to Active Directory.</span></span> <span data-ttu-id="46e8e-119">Se il servizio non è in esecuzione in un controller di dominio, il servizio dispone dei diritti di accesso e dei privilegi concessi all'account computer per il computer in cui è in esecuzione il servizio. Questo è significativamente meno potente dell'accesso a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="46e8e-119">If the service is not running on a DC, the service has the access rights and privileges granted to the computer account for the computer on which the service is running; this is significantly less powerful than system-level access.</span></span>

## <a name="examples"></a><span data-ttu-id="46e8e-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="46e8e-120">Examples</span></span>

<span data-ttu-id="46e8e-121">Nell'esempio di codice Visual Basic riportato di seguito viene illustrato come utilizzare la funzione **GetObject** per eseguire l'associazione a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="46e8e-121">The following Visual Basic code example shows how to use the **GetObject** function to bind to an object.</span></span>


```VB
Dim myUser as IADs
Set myUser = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com")
```



<span data-ttu-id="46e8e-122">Nell'esempio di codice C++ riportato di seguito viene illustrato come utilizzare la funzione [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) per eseguire l'associazione a un oggetto.</span><span class="sxs-lookup"><span data-stu-id="46e8e-122">The following C++ code example shows how to use the [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) function to bind to an object.</span></span>


```C++
IADs *pObject;
HRESULT hr;

// Initialize COM.
CoInitialize(NULL);

hr = ADsGetObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com", 
        IID_IADs,
        (void**) &pObject);

if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}

// Uninitialize COM.
CoUninitialize();
```



 

 