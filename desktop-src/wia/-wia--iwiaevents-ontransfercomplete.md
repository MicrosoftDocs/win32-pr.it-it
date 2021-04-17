---
description: Evento che si verifica quando un trasferimento dei dati viene completato correttamente.
ms.assetid: 6110867b-21e2-48ab-97ad-0e084a0ccf07
title: Evento WIA. OnTransferComplete
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia.OnTransferComplete
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: d33685e0e8fe233f96e9841359e56f759032d17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231563"
---
# <a name="wiaontransfercomplete-event"></a><span data-ttu-id="ebc70-103">Evento WIA. OnTransferComplete</span><span class="sxs-lookup"><span data-stu-id="ebc70-103">Wia.OnTransferComplete event</span></span>

<span data-ttu-id="ebc70-104">Evento che si verifica quando un trasferimento dei dati viene completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="ebc70-104">Event that occurs when a data transfer is completed successfully.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebc70-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ebc70-105">Syntax</span></span>


```JScript
Wia.OnTransferComplete(
  Item,
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="ebc70-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ebc70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebc70-107">*Item*</span><span class="sxs-lookup"><span data-stu-id="ebc70-107">*Item*</span></span> 
</dt> <dd>

<span data-ttu-id="ebc70-108">Oggetto [**elemento**](-wia-item.md) trasferito.</span><span class="sxs-lookup"><span data-stu-id="ebc70-108">The [**Item**](-wia-item.md) object transferred.</span></span>

</dd> <dt>

<span data-ttu-id="ebc70-109">*Percorso*</span><span class="sxs-lookup"><span data-stu-id="ebc70-109">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="ebc70-110">Il percorso e il nome file dell'immagine trasferita.</span><span class="sxs-lookup"><span data-stu-id="ebc70-110">The path and file name of the transferred image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebc70-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ebc70-111">Return value</span></span>

<span data-ttu-id="ebc70-112">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ebc70-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebc70-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ebc70-113">Remarks</span></span>

<span data-ttu-id="ebc70-114">WIA notifica allo script o all'applicazione quando un trasferimento dati, un'immagine o un suono viene completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="ebc70-114">WIA notifies the script or application when a data transfer, image or sound, completes successfully.</span></span> <span data-ttu-id="ebc70-115">Implementare la subroutine **objWia** \_ **OnTransferComplete ()** per consentire all'applicazione o allo script di rispondere al completamento del trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="ebc70-115">Implement the **objWia**\_**OnTransferComplete()** subroutine to allow your script or application to respond to the completion of the data transfer.</span></span>

<span data-ttu-id="ebc70-116">Ad esempio, potrebbe essere necessario che uno script visualizzi un'immagine dopo che è stata trasferita.</span><span class="sxs-lookup"><span data-stu-id="ebc70-116">For example, you might want a script to display an image after it is transferred.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebc70-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ebc70-117">Requirements</span></span>



| <span data-ttu-id="ebc70-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebc70-118">Requirement</span></span> | <span data-ttu-id="ebc70-119">Valore</span><span class="sxs-lookup"><span data-stu-id="ebc70-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc70-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebc70-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ebc70-121">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ebc70-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ebc70-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ebc70-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ebc70-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ebc70-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ebc70-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ebc70-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ebc70-125"><dt>Wiascr.dll (versione 4,90 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="ebc70-125"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




