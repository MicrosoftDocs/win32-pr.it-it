---
description: Contiene informazioni su un evento di sistema tablet.
ms.assetid: 725f4b43-0bcb-4452-a87f-b24a85de0049
title: Struttura SYSTEM_EVENT_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_EVENT_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5d77c78a78a6cecae0368e8d9192a0dc0efc10e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234077"
---
# <a name="system_event_data-structure"></a><span data-ttu-id="08bf5-103">\_ \_ Struttura dei dati degli eventi di sistema</span><span class="sxs-lookup"><span data-stu-id="08bf5-103">SYSTEM\_EVENT\_DATA structure</span></span>

<span data-ttu-id="08bf5-104">Contiene informazioni su un evento di sistema tablet.</span><span class="sxs-lookup"><span data-stu-id="08bf5-104">Contains information about a tablet system event.</span></span>

## <a name="syntax"></a><span data-ttu-id="08bf5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08bf5-105">Syntax</span></span>


```C++
typedef struct tagSYSTEM_EVENT_DATA {
  BYTE  bModifier;
  WCHAR wKey;
  LONG  xPos;
  LONG  yPos;
  BYTE  bCursorMode;
  DWORD dwButtonState;
} SYSTEM_EVENT_DATA;
```



## <a name="members"></a><span data-ttu-id="08bf5-106">Members</span><span class="sxs-lookup"><span data-stu-id="08bf5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="08bf5-107">**bModifier**</span><span class="sxs-lookup"><span data-stu-id="08bf5-107">**bModifier**</span></span>
</dt> <dd>

<span data-ttu-id="08bf5-108">Valori di bit per i modificatori.</span><span class="sxs-lookup"><span data-stu-id="08bf5-108">Bit values for the modifiers.</span></span> <span data-ttu-id="08bf5-109">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="08bf5-109">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="08bf5-110">**Tasto wsul**</span><span class="sxs-lookup"><span data-stu-id="08bf5-110">**wKey**</span></span>
</dt> <dd>

<span data-ttu-id="08bf5-111">Analizza il codice per il carattere della tastiera.</span><span class="sxs-lookup"><span data-stu-id="08bf5-111">Scan code for the keyboard character.</span></span>

</dd> <dt>

<span data-ttu-id="08bf5-112">**xPos**</span><span class="sxs-lookup"><span data-stu-id="08bf5-112">**xPos**</span></span>
</dt> <dd>

<span data-ttu-id="08bf5-113">Posizione X dell'evento.</span><span class="sxs-lookup"><span data-stu-id="08bf5-113">X position of the event.</span></span>

</dd> <dt>

<span data-ttu-id="08bf5-114">**yPos**</span><span class="sxs-lookup"><span data-stu-id="08bf5-114">**yPos**</span></span>
</dt> <dd>

<span data-ttu-id="08bf5-115">Posizione Y dell'evento.</span><span class="sxs-lookup"><span data-stu-id="08bf5-115">Y position of the event.</span></span>

</dd> <dt>

<span data-ttu-id="08bf5-116">**bCursorMode**</span><span class="sxs-lookup"><span data-stu-id="08bf5-116">**bCursorMode**</span></span>
</dt> <dd>

<span data-ttu-id="08bf5-117">Tipo di cursore che ha causato l'evento.</span><span class="sxs-lookup"><span data-stu-id="08bf5-117">The type of cursor that caused the event.</span></span> <span data-ttu-id="08bf5-118">Per ulteriori informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="08bf5-118">See the remarks section for more information.</span></span>

</dd> <dt>

<span data-ttu-id="08bf5-119">**dwButtonState**</span><span class="sxs-lookup"><span data-stu-id="08bf5-119">**dwButtonState**</span></span>
</dt> <dd>

<span data-ttu-id="08bf5-120">Stato dei pulsanti al momento dell'evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="08bf5-120">State of the buttons at the time of the system event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08bf5-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="08bf5-121">Remarks</span></span>

<span data-ttu-id="08bf5-122">Gli eventi di sistema seguenti vengono definiti per l'utilizzo nel membro **bModifier** .</span><span class="sxs-lookup"><span data-stu-id="08bf5-122">The following system events are defined for use in the **bModifier** member.</span></span>



| <span data-ttu-id="08bf5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="08bf5-123">Value</span></span>               | <span data-ttu-id="08bf5-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08bf5-124">Description</span></span>                  |
|---------------------|------------------------------|
| <span data-ttu-id="08bf5-125">\_modificatore se \_ CTRL</span><span class="sxs-lookup"><span data-stu-id="08bf5-125">SE\_MODIFIER\_CTRL</span></span>  | <span data-ttu-id="08bf5-126">È stato premuto il tasto CTRL.</span><span class="sxs-lookup"><span data-stu-id="08bf5-126">The Control key was pressed.</span></span> |
| <span data-ttu-id="08bf5-127">\_ALT modificatore se \_</span><span class="sxs-lookup"><span data-stu-id="08bf5-127">SE\_MODIFIER\_ALT</span></span>   | <span data-ttu-id="08bf5-128">È stato premuto il tasto ALT.</span><span class="sxs-lookup"><span data-stu-id="08bf5-128">The Alt key was pressed.</span></span>     |
| <span data-ttu-id="08bf5-129">\_MAIUSC se modificatore \_</span><span class="sxs-lookup"><span data-stu-id="08bf5-129">SE\_MODIFIER\_SHIFT</span></span> | <span data-ttu-id="08bf5-130">Il tasto MAIUSC è stato premuto.</span><span class="sxs-lookup"><span data-stu-id="08bf5-130">The Shift key was pressed.</span></span>   |



 

<span data-ttu-id="08bf5-131">Gli eventi di sistema seguenti vengono definiti per l'utilizzo nel membro **bCursorMode** .</span><span class="sxs-lookup"><span data-stu-id="08bf5-131">The following system events are defined for use in the **bCursorMode** member.</span></span>



| <span data-ttu-id="08bf5-132">Valore</span><span class="sxs-lookup"><span data-stu-id="08bf5-132">Value</span></span>              | <span data-ttu-id="08bf5-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08bf5-133">Description</span></span>               |
|--------------------|---------------------------|
| <span data-ttu-id="08bf5-134">\_cursore normale \_ se</span><span class="sxs-lookup"><span data-stu-id="08bf5-134">SE\_NORMAL\_CURSOR</span></span> | <span data-ttu-id="08bf5-135">Indica il suggerimento della penna.</span><span class="sxs-lookup"><span data-stu-id="08bf5-135">Indicates the pen tip.</span></span>    |
| <span data-ttu-id="08bf5-136">\_cursore gomma se \_</span><span class="sxs-lookup"><span data-stu-id="08bf5-136">SE\_ERASER\_CURSOR</span></span> | <span data-ttu-id="08bf5-137">Indica la gomma della penna.</span><span class="sxs-lookup"><span data-stu-id="08bf5-137">Indicates the pen eraser.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="08bf5-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08bf5-138">Requirements</span></span>



| <span data-ttu-id="08bf5-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="08bf5-139">Requirement</span></span> | <span data-ttu-id="08bf5-140">Valore</span><span class="sxs-lookup"><span data-stu-id="08bf5-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="08bf5-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08bf5-141">Minimum supported client</span></span><br/> | <span data-ttu-id="08bf5-142">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="08bf5-142">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="08bf5-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08bf5-143">Minimum supported server</span></span><br/> | <span data-ttu-id="08bf5-144">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="08bf5-144">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="08bf5-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08bf5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08bf5-146">**Metodo IStylusPlugin:: SystemEvent**</span><span class="sxs-lookup"><span data-stu-id="08bf5-146">**IStylusPlugin::SystemEvent Method**</span></span>](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-systemevent)
</dt> <dt>

[<span data-ttu-id="08bf5-147">**Metodo ITabletEventSink:: SystemEvent**</span><span class="sxs-lookup"><span data-stu-id="08bf5-147">**ITabletEventSink::SystemEvent Method**</span></span>](itableteventsink-systemevent.md)
</dt> </dl>

 

 




