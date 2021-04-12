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
# <a name="invoking-creation-wizards-from-your-application"></a>Richiamo di creazioni guidate dall'applicazione

Un'applicazione o un componente può utilizzare le stesse procedure guidate di creazione di oggetti del servizio directory utilizzate dal Active Directory snap-in MMC amministrativi. Questa operazione viene eseguita con l'interfaccia [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) .

## <a name="using-the-idsadmincreateobj-interface"></a>Uso dell'interfaccia IDsAdminCreateObj

Un'applicazione o un componente (client) crea un'istanza dell'interfaccia [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) chiamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con l'identificatore di classe **CLSID \_ DsAdminCreateObj** . È necessario inizializzare COM chiamando [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) prima della chiamata a **CoCreateInstance** .

Il client chiama quindi [**IDsAdminCreateObj:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-initialize) per inizializzare l'oggetto [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) . **IDsAdminCreateObj:: Initialize** accetta un puntatore all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) che rappresenta il contenitore in cui deve essere creato l'oggetto e il nome della classe dell'oggetto da creare. Quando si creano oggetti utente, è anche possibile specificare un oggetto esistente che verrà copiato nel nuovo oggetto.

Quando l'oggetto [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) è stato inizializzato, il client chiama [**IDsAdminCreateObj:: CreateModal**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadmincreateobj-createmodal) per visualizzare la creazione guidata di oggetti.

A differenza della maggior parte degli identificatori di interfaccia e di classe, **CLSID \_ DsAdminCreateObj** e **IID \_ ADsAdminCreateObj** non sono definiti in un file di libreria. Ciò significa che è necessario definire lo spazio di archiviazione per questi identificatori all'interno dell'applicazione. A tale scopo, è necessario includere il file Initguid. h immediatamente prima di includere DSAdmin. h. Il file Initguid. h deve essere incluso una sola volta in un'applicazione. Nell'esempio di codice seguente viene illustrato come includere questi file.


```C++
#include <initguid.h>
#include <dsadmin.h>
```



Nell'esempio di codice seguente viene illustrato come creare e utilizzare l'interfaccia [**IDsAdminCreateObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadmincreateobj) per avviare la creazione guidata oggetto per un oggetto utente.


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



 

 