---
title: Richiamo di creazioni guidate dall'applicazione
description: Un'applicazione o un componente può utilizzare le stesse procedure guidate di creazione di oggetti del servizio directory utilizzate dal Active Directory snap-in MMC amministrativi. Questa operazione viene eseguita con l'interfaccia IDsAdminCreateObj.
ms.assetid: be4b6101-f795-403b-b93e-960759ac4f14
ms.tgt_platform: multiple
keywords:
- Richiamo di creazioni guidate dall'applicazione AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa523d3b861d1d4a7588455b04c1a9633734253a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472523"
---
# <a name="invoking-creation-wizards-from-your-application"></a><span data-ttu-id="6c8ac-104">Richiamo di creazioni guidate dall'applicazione</span><span class="sxs-lookup"><span data-stu-id="6c8ac-104">Invoking Creation Wizards from Your Application</span></span>

<span data-ttu-id="6c8ac-105">Un'applicazione o un componente può utilizzare le stesse procedure guidate di creazione di oggetti del servizio directory utilizzate dal Active Directory snap-in MMC amministrativi. Questa operazione viene eseguita con l'interfaccia [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) .</span><span class="sxs-lookup"><span data-stu-id="6c8ac-105">An application or component can use the same directory service object creation wizards used by the Active Directory administrative MMC snap-ins. This is accomplished with the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface.</span></span>

## <a name="using-the-idsadmincreateobj-interface"></a><span data-ttu-id="6c8ac-106">Uso dell'interfaccia IDsAdminCreateObj</span><span class="sxs-lookup"><span data-stu-id="6c8ac-106">Using the IDsAdminCreateObj Interface</span></span>

<span data-ttu-id="6c8ac-107">Un'applicazione o un componente (client) crea un'istanza dell'interfaccia [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con l'identificatore di classe **CLSID \_ DsAdminCreateObj** .</span><span class="sxs-lookup"><span data-stu-id="6c8ac-107">An application or component (client) creates an instance of the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the **CLSID\_DsAdminCreateObj** class identifier.</span></span> <span data-ttu-id="6c8ac-108">È necessario inizializzare COM chiamando [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) prima della chiamata a **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="6c8ac-108">COM must be initialized by calling [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) before **CoCreateInstance** is called.</span></span>

<span data-ttu-id="6c8ac-109">Il client chiama quindi [**IDsAdminCreateObj:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) per inizializzare l'oggetto [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) .</span><span class="sxs-lookup"><span data-stu-id="6c8ac-109">The client then calls [**IDsAdminCreateObj::Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) to initialize the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) object.</span></span> <span data-ttu-id="6c8ac-110">**IDsAdminCreateObj:: Initialize** accetta un puntatore all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) che rappresenta il contenitore in cui deve essere creato l'oggetto e il nome della classe dell'oggetto da creare.</span><span class="sxs-lookup"><span data-stu-id="6c8ac-110">**IDsAdminCreateObj::Initialize** accepts an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface pointer that represents the container that the object should be created in, and the class name of the object to be created.</span></span> <span data-ttu-id="6c8ac-111">Quando si creano oggetti utente, è anche possibile specificare un oggetto esistente che verrà copiato nel nuovo oggetto.</span><span class="sxs-lookup"><span data-stu-id="6c8ac-111">When creating user objects, it is also possible to specify an existing object that will be copied to the new object.</span></span>

<span data-ttu-id="6c8ac-112">Quando l'oggetto [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) è stato inizializzato, il client chiama [**IDsAdminCreateObj:: CreateModal**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) per visualizzare la creazione guidata di oggetti.</span><span class="sxs-lookup"><span data-stu-id="6c8ac-112">When the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) object has been initialized, the client calls [**IDsAdminCreateObj::CreateModal**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) to display the object creation wizard.</span></span>

<span data-ttu-id="6c8ac-113">A differenza della maggior parte degli identificatori di interfaccia e di classe, **CLSID \_ DsAdminCreateObj** e **IID \_ ADsAdminCreateObj** non sono definiti in un file di libreria.</span><span class="sxs-lookup"><span data-stu-id="6c8ac-113">Unlike most class and interface identifiers, **CLSID\_DsAdminCreateObj** and **IID\_ADsAdminCreateObj** are not defined in a library file.</span></span> <span data-ttu-id="6c8ac-114">Ciò significa che è necessario definire lo spazio di archiviazione per questi identificatori all'interno dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c8ac-114">This means you must define the storage for these identifiers within your application.</span></span> <span data-ttu-id="6c8ac-115">A tale scopo, è necessario includere il file Initguid. h immediatamente prima di includere DSAdmin. h.</span><span class="sxs-lookup"><span data-stu-id="6c8ac-115">To do this, you must include the file initguid.h immediately before including dsadmin.h.</span></span> <span data-ttu-id="6c8ac-116">Il file Initguid. h deve essere incluso una sola volta in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6c8ac-116">The initguid.h file must only be included once in an application.</span></span> <span data-ttu-id="6c8ac-117">Nell'esempio di codice seguente viene illustrato come includere questi file.</span><span class="sxs-lookup"><span data-stu-id="6c8ac-117">The following code example shows how to include these files.</span></span>


```C++
#include <initguid.h>
#include <dsadmin.h>
```



<span data-ttu-id="6c8ac-118">Nell'esempio di codice seguente viene illustrato come creare e utilizzare l'interfaccia [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) per avviare la creazione guidata oggetto per un oggetto utente.</span><span class="sxs-lookup"><span data-stu-id="6c8ac-118">The following code example shows how the [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) interface can be created and used to start the object creation wizard for a user object.</span></span>


```C++
//  Add activeds.lib to your project
//  Add adsiid.lib to your project

#include "stdafx.h"
#include <atlbase.h>
#include <atlstr.h>
#include "activeds.h"
#include <initguid.h> // Only include this in one source file
#include <dsadmin.h>

//  GetUserContainer() function binds to the user container
IADsContainer* GetUserContainer(void)
{
    IADsContainer *pUsers = NULL;
    HRESULT hr;
    IADs *pRoot;

    //  Bind to the rootDSE.
    hr = ADsGetObject(L"LDAP://rootDSE", IID_IADs, (LPVOID*)&pRoot);

    if(SUCCEEDED(hr))
    {
        VARIANT var;
        VariantInit(&var);
        CComBSTR sbstr(L"defaultNamingContext");

        //  Get the default naming context (domain) DN.
        hr = pRoot->Get(sbstr, &var);
        if(SUCCEEDED(hr) && (VT_BSTR == var.vt))
        {
            CStringW sstr(L"LDAP://CN=Users,");
            sstr += var.bstrVal;

            //  Bind to the User container.
            hr = ADsGetObject(sstr, IID_IADsContainer, (LPVOID*)&pUsers);

            VariantClear(&var);
        }
    }

    return pUsers;
}


//  The LaunchNewUserWizard() function launches the user wizard.
HRESULT LaunchNewUserWizard(IADs** ppAdsOut)
{
    if(NULL == ppAdsOut)
    {
        return E_INVALIDARG;
    }

    HRESULT hr;
    IDsAdminCreateObj* pCreateObj = NULL;

    hr = ::CoCreateInstance(CLSID_DsAdminCreateObj,
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_IDsAdminCreateObj,
                            (void**)&pCreateObj);

    if(SUCCEEDED(hr))
    {
        IADsContainer *pContainer;

        pContainer = GetUserContainer();

        if(pContainer)
        {
            hr = pCreateObj->Initialize(pContainer, NULL, L"user");
            if(SUCCEEDED(hr))
            {
                HWND    hwndParent;

                hwndParent = GetDesktopWindow();

                hr = pCreateObj->CreateModal(hwndParent, ppAdsOut);
            }

            pContainer->Release();
        }

        pCreateObj->Release();
    }

    return hr;    
}

//  Entry point to the application
int main(void)
{
    HRESULT hr;
    IADs *pAds = NULL;

    CoInitialize(NULL);

    hr = LaunchNewUserWizard(&pAds);
    if((S_OK == hr) && (NULL != pAds))
    {
        pAds->Release();
    }

    CoUninitialize();

    return 0;
}
```



 

 