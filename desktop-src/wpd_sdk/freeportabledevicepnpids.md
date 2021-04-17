---
description: 'Libera gli identificatori di Plug and Play (PnP) recuperati dai metodi IPortableDeviceManager:: GetDevices o IPortableDeviceServiceManager:: GetDeviceServices.'
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
title: Funzione FreePortableDevicePnPIDs (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePortableDevicePnPIDs
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 58bb5fa33007ed0e167226edf7078d08c2e5c3de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232703"
---
# <a name="freeportabledevicepnpids-function"></a><span data-ttu-id="07c9e-103">FreePortableDevicePnPIDs (funzione)</span><span class="sxs-lookup"><span data-stu-id="07c9e-103">FreePortableDevicePnPIDs function</span></span>

<span data-ttu-id="07c9e-104">La funzione helper **FreePortableDevicePnPIDs** libera gli identificatori plug and Play (PNP) recuperati dai metodi [**IPortableDeviceManager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) o [**IPortableDeviceServiceManager:: GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) .</span><span class="sxs-lookup"><span data-stu-id="07c9e-104">The **FreePortableDevicePnPIDs** helper function frees the Plug and Play (PnP) identifiers that are retrieved by the [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) or [**IPortableDeviceServiceManager::GetDeviceServices**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemanager-getdeviceservices) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="07c9e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07c9e-105">Syntax</span></span>


```C++
void FreePortableDevicePnPIDs(
   LPWSTR *pPnPIDs,
   DWORD  cPnPIDs
);
```



## <a name="parameters"></a><span data-ttu-id="07c9e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="07c9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07c9e-107">*pPnPIDs*</span><span class="sxs-lookup"><span data-stu-id="07c9e-107">*pPnPIDs*</span></span> 
</dt> <dd>

<span data-ttu-id="07c9e-108">Matrice di identificatori di Plug and Play (PnP) da liberare.</span><span class="sxs-lookup"><span data-stu-id="07c9e-108">The array of Plug and Play (PnP) identifiers to be freed.</span></span>

</dd> <dt>

<span data-ttu-id="07c9e-109">*cPnPIDs*</span><span class="sxs-lookup"><span data-stu-id="07c9e-109">*cPnPIDs*</span></span> 
</dt> <dd>

<span data-ttu-id="07c9e-110">Il numero di identificatori nella matrice specificata dal parametro *pPnPIDs* .</span><span class="sxs-lookup"><span data-stu-id="07c9e-110">The number of identifiers in the array specified by the *pPnPIDs* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07c9e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07c9e-111">Return value</span></span>

<span data-ttu-id="07c9e-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="07c9e-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07c9e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="07c9e-113">Remarks</span></span>

<span data-ttu-id="07c9e-114">L'applicazione è responsabile di liberare la matrice di puntatori che alloca.</span><span class="sxs-lookup"><span data-stu-id="07c9e-114">The application is responsible for freeing the array of pointers that it allocates.</span></span>

## <a name="examples"></a><span data-ttu-id="07c9e-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="07c9e-115">Examples</span></span>


```C++
// Allocate an array of LPWSTR pointers.
    LPWSTR* pPnpDeviceIDs = new LPWSTR[cPnpDeviceIDs];
if (pPnpDeviceIDs != NULL)
{
    hr = pPortableDeviceManager->;GetDevices(pPnpDeviceIDs, &cPnpDeviceIDs);
    if (SUCCEEDED(hr))
    {
        // Free all returned PnPDeviceID strings allocated by IPortableDeviceManager::GetDevices.
     FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);
     // Application is responsible for deleting the array of LPWSTR pointers.
     delete [] pPnpDeviceIDs;
     pPnpDeviceIDs = NULL;      
 }
} 
```



## <a name="requirements"></a><span data-ttu-id="07c9e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07c9e-116">Requirements</span></span>



| <span data-ttu-id="07c9e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="07c9e-117">Requirement</span></span> | <span data-ttu-id="07c9e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="07c9e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="07c9e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07c9e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="07c9e-120">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="07c9e-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                           |
| <span data-ttu-id="07c9e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07c9e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="07c9e-122">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="07c9e-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="07c9e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07c9e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="07c9e-124"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="07c9e-124"><dt>PortableDevice.h</dt></span></span> </dl> |



 

 




