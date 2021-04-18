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
# <a name="working-with-enumeration-objects"></a><span data-ttu-id="ef3b3-103">Utilizzo di oggetti di enumerazione</span><span class="sxs-lookup"><span data-stu-id="ef3b3-103">Working with Enumeration Objects</span></span>

<span data-ttu-id="ef3b3-104">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ef3b3-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="ef3b3-105">Nell'esempio di codice seguente viene illustrato il funzionamento di un chiamante con gli oggetti di enumerazione utilizzando l'interfaccia [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) .</span><span class="sxs-lookup"><span data-stu-id="ef3b3-105">The code example that follows demonstrates how a caller works with enumeration objects using the [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) interface.</span></span> <span data-ttu-id="ef3b3-106">Si noti che le informazioni restituite da un oggetto di enumerazione sono statiche.</span><span class="sxs-lookup"><span data-stu-id="ef3b3-106">Note that the information that is returned by a enumeration object is static.</span></span> <span data-ttu-id="ef3b3-107">Per visualizzare le nuove modifiche alla configurazione, è necessario eseguire di nuovo l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="ef3b3-107">You must query the object again to see new configuration changes.</span></span>

<span data-ttu-id="ef3b3-108">La funzione **GetControllerById** accetta un'interfaccia [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem) , specificata dal parametro *pSubsystem* e query per i controller nel sottosistema, quindi scorre l'enumerazione restituita cercando un controller con un GUID corrispondente al GUID specificato dal parametro *pControllerId* .</span><span class="sxs-lookup"><span data-stu-id="ef3b3-108">The **GetControllerById** function takes an [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem) interface, specified by the *pSubsystem* parameter, and queries for the controllers in the subsystem, then iterates through the returned enumeration searching for a controller with a GUID that matches the GUID that is specified by the *pControllerId* parameter.</span></span> <span data-ttu-id="ef3b3-109">Se viene trovato un controller corrispondente, questo viene restituito dal parametro *ppController* insieme a un valore \_ **HRESULT** S OK.</span><span class="sxs-lookup"><span data-stu-id="ef3b3-109">If a matching controller is found, it is returned by the *ppController* parameter along with an S\_OK **HRESULT**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ef3b3-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ef3b3-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef3b3-111">Uso di VDS</span><span class="sxs-lookup"><span data-stu-id="ef3b3-111">Using VDS</span></span>](using-vds.md)
</dt> <dt>

[<span data-ttu-id="ef3b3-112">Oggetti helper</span><span class="sxs-lookup"><span data-stu-id="ef3b3-112">Helper Objects</span></span>](helper-objects.md)
</dt> <dt>

[<span data-ttu-id="ef3b3-113">**IEnumVdsObject**</span><span class="sxs-lookup"><span data-stu-id="ef3b3-113">**IEnumVdsObject**</span></span>](/windows/desktop/api/Vds/nn-vds-ienumvdsobject)
</dt> <dt>

[<span data-ttu-id="ef3b3-114">**IVdsSubSystem**</span><span class="sxs-lookup"><span data-stu-id="ef3b3-114">**IVdsSubSystem**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdssubsystem)
</dt> </dl>

 

 
