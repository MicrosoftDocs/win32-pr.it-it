---
description: Evento che si verifica quando viene connesso un nuovo dispositivo hardware Windows Image Acquisition (WIA).
ms.assetid: 327a29b8-581c-41b5-bea7-068bec95e653
title: Evento WIA. OnDeviceConnected
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnDeviceConnected
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 952b738e8afa0850bd67bab1206382e96419513c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231565"
---
# <a name="wiaondeviceconnected-event"></a><span data-ttu-id="74729-103">Evento WIA. OnDeviceConnected</span><span class="sxs-lookup"><span data-stu-id="74729-103">Wia.OnDeviceConnected event</span></span>

<span data-ttu-id="74729-104">Evento che si verifica quando viene connesso un nuovo dispositivo hardware Windows Image Acquisition (WIA).</span><span class="sxs-lookup"><span data-stu-id="74729-104">Event that occurs when a new Windows Image Acquisition (WIA) hardware device is connected.</span></span>

## <a name="syntax"></a><span data-ttu-id="74729-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74729-105">Syntax</span></span>


```JScript
Wia.OnDeviceConnected(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="74729-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="74729-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74729-107">*Id*</span><span class="sxs-lookup"><span data-stu-id="74729-107">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="74729-108">Stringa che contiene l'ID del dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="74729-108">A string that contains the ID of the connected device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74729-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74729-109">Return value</span></span>

<span data-ttu-id="74729-110">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="74729-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="74729-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="74729-111">Remarks</span></span>

<span data-ttu-id="74729-112">WIA notifica lo script o l'applicazione ogni volta che un nuovo dispositivo hardware è connesso al computer.</span><span class="sxs-lookup"><span data-stu-id="74729-112">WIA notifies the script or application whenever a new hardware device is connected to the computer.</span></span> <span data-ttu-id="74729-113">Implementare la subroutine **objWia** \_ **OnDeviceConnected ()** per consentire all'applicazione o allo script di rispondere alla connessione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74729-113">Implement the **objWia**\_**OnDeviceConnected()** subroutine to allow the script or application to respond to the device connection.</span></span>

<span data-ttu-id="74729-114">Ad esempio, potrebbe essere necessario uno script per aggiornare la raccolta di [**dispositivi**](-wia-iwia-devices.md) quando viene installato un nuovo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74729-114">For example, you might want a script to refresh the [**Devices**](-wia-iwia-devices.md) collection when a new device is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="74729-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74729-115">Requirements</span></span>



| <span data-ttu-id="74729-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="74729-116">Requirement</span></span> | <span data-ttu-id="74729-117">Valore</span><span class="sxs-lookup"><span data-stu-id="74729-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74729-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74729-118">Minimum supported client</span></span><br/> | <span data-ttu-id="74729-119">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="74729-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74729-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74729-120">Minimum supported server</span></span><br/> | <span data-ttu-id="74729-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="74729-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="74729-122">DLL</span><span class="sxs-lookup"><span data-stu-id="74729-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74729-123"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="74729-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




