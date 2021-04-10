---
description: Evento che si verifica quando un nuovo dispositivo hardware di acquisizione immagini Windows (WIA) viene disconnesso.
ms.assetid: 9c3ccdba-288c-4bdd-b257-b03999bc6fd9
title: Evento WIA. OnDeviceDisconnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceDisconnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 45652f3c447c1dd0f59b0470823782c6ba635cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231564"
---
# <a name="wiaondevicedisconnected-event"></a><span data-ttu-id="ae7dc-103">Evento WIA. OnDeviceDisconnected</span><span class="sxs-lookup"><span data-stu-id="ae7dc-103">Wia.OnDeviceDisconnected event</span></span>

<span data-ttu-id="ae7dc-104">Evento che si verifica quando un nuovo dispositivo hardware di acquisizione immagini Windows (WIA) viene disconnesso.</span><span class="sxs-lookup"><span data-stu-id="ae7dc-104">Event that occurs when a new Windows Image Acquisition (WIA) hardware device is disconnected.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae7dc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae7dc-105">Syntax</span></span>


```JScript
Wia.OnDeviceDisconnected(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="ae7dc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae7dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae7dc-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="ae7dc-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="ae7dc-108">Stringa che contiene l'ID del dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="ae7dc-108">A string that contains the ID of the connected device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae7dc-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae7dc-109">Return value</span></span>

<span data-ttu-id="ae7dc-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ae7dc-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae7dc-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae7dc-111">Remarks</span></span>

<span data-ttu-id="ae7dc-112">WIA notifica lo script o l'applicazione ogni volta che un dispositivo hardware è disconnesso dal computer.</span><span class="sxs-lookup"><span data-stu-id="ae7dc-112">WIA notifies the script or application whenever a hardware device is disconnected from the computer.</span></span> <span data-ttu-id="ae7dc-113">Implementare la subroutine **objWia** \_ **OnDeviceDisconnected ()** per consentire all'applicazione o allo script di rispondere alla disconnessione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ae7dc-113">Implement the **objWia**\_**OnDeviceDisconnected()** subroutine to allow the script or application to respond to the device disconnection.</span></span>

<span data-ttu-id="ae7dc-114">Ad esempio, potrebbe essere necessario uno script per aggiornare la raccolta di [**dispositivi**](-wia-iwia-devices.md) quando un dispositivo viene rimosso dal computer.</span><span class="sxs-lookup"><span data-stu-id="ae7dc-114">For example, you might want a script to refresh the [**Devices**](-wia-iwia-devices.md) collection when a device is removed from the computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae7dc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae7dc-115">Requirements</span></span>



| <span data-ttu-id="ae7dc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae7dc-116">Requirement</span></span> | <span data-ttu-id="ae7dc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="ae7dc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae7dc-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae7dc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ae7dc-119">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ae7dc-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae7dc-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae7dc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ae7dc-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ae7dc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ae7dc-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ae7dc-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae7dc-123"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="ae7dc-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




