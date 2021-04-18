---
description: Utilizzo di oggetti di enumerazione
ms.assetid: cb99e9fd-613c-4e38-9e0f-e1a23b72aa07
title: Utilizzo di oggetti di enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0df90548ef060d537faff206e45e0cf74630cdfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313239"
---
# <a name="working-with-enumeration-objects"></a>Utilizzo di oggetti di enumerazione

\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Nell'esempio di codice seguente viene illustrato il funzionamento di un chiamante con gli oggetti di enumerazione utilizzando l'interfaccia [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) . Si noti che le informazioni restituite da un oggetto di enumerazione sono statiche. Per visualizzare le nuove modifiche alla configurazione, è necessario eseguire di nuovo l'oggetto.

La funzione **GetControllerById** accetta un'interfaccia [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem) , specificata dal parametro *pSubsystem* e query per i controller nel sottosistema, quindi scorre l'enumerazione restituita cercando un controller con un GUID corrispondente al GUID specificato dal parametro *pControllerId* . Se viene trovato un controller corrispondente, questo viene restituito dal parametro *ppController* insieme a un valore \_ **HRESULT** S OK.


```C++
//
// Simple macro to release non-null interfaces.
//
#include <windows.h>
#include "vds.h"
#include <stdio.h>

#define _SafeRelease(x) {if (NULL != x) { x->Release(); x = NULL; } }

HRESULT GetControllerById(
         IN IVdsSubSystem       *pSubsystem,
         IN CONST VDS_OBJECT_ID *pControllerId,
         OUT IVdsController     **ppController)
{
    VDS_CONTROLLER_PROP vdsControllerProperties;
    IEnumVdsObject      *pEnumController = NULL;
    IVdsController      *pController     = NULL;
    IUnknown            *pUnknown        = NULL;
    HRESULT             hResult          = S_OK;
    ULONG               ulFetched        = 0;
    BOOL                bDone            = FALSE;

    ZeroMemory(&vdsControllerProperties, sizeof(VDS_CONTROLLER_PROP));

    // Query for the enumeration of controllers belonging
    // to the given subsystem.
    hResult = pSubsystem->QueryControllers(&pEnumController);

    if (SUCCEEDED(hResult) && (!pEnumController)) 
    {
        hResult = E_UNEXPECTED; // Errant provider, 
        // returned S_OK 
        // with a NULL pointer.
    }

    if (SUCCEEDED(hResult)) 
    {
        // Enumerate through all the controllers this subsystem 
        // contains to find the controller of interest.
        while (!bDone) 
        {
            ulFetched = 0;
            hResult = pEnumController->Next(1, &pUnknown, &ulFetched);

            if (hResult == S_FALSE) 
            {
                hResult = E_INVALIDARG;
                break;
            }

            if (SUCCEEDED(hResult) && (!pUnknown)) 
            {
                hResult = E_UNEXPECTED; // Errant provider, 
                // returned S_OK with
                // a NULL pointer 
            }

            // Use an IVdsController interface to get the controller 
            // properties and check for the desired GUID.
            if (SUCCEEDED(hResult)) 
            {
                hResult = pUnknown->QueryInterface(IID_IVdsController,  
                    (void **) &pController);
            }

            if (SUCCEEDED(hResult) && (!pController)) 
            {
                hResult = E_UNEXPECTED; // Errant provider, 
                // returned S_OK 
                // with a NULL pointer
            }

            if (SUCCEEDED(hResult)) 
            {
                hResult = pController->  
                GetProperties( &vdsControllerProperties);
            }

            if (SUCCEEDED(hResult) 
                && IsEqualGUID(*pControllerId, vdsControllerProperties.id)) 
            {
                bDone = TRUE;
            } 
            else 
            {
                _SafeRelease(pController);
            }

            _SafeRelease(pUnknown);

            //Free the strings in the properties structure.
            if (NULL != vdsControllerProperties.pwszIdentification) 
            {
                CoTaskMemFree(vdsControllerProperties.pwszIdentification);
            }

            ZeroMemory(&vdsControllerProperties, sizeof(VDS_CONTROLLER_PROP));
        }
    }

    if (SUCCEEDED(hResult)) 
    {
        *ppController = pController;
    }

    _SafeRelease(pEnumController);
    return hResult;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di VDS](using-vds.md)
</dt> <dt>

[Oggetti helper](helper-objects.md)
</dt> <dt>

[**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject)
</dt> <dt>

[**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem)
</dt> </dl>

 

 
