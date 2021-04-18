---
description: Si verifica quando è disponibile un evento di sistema.
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: 'Metodo ITabletEventSink:: SystemEvent'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.SystemEvent
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 71b5882fd9e19df43581e00cce55c2af5faa432b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314912"
---
# <a name="itableteventsinksystemevent-method"></a><span data-ttu-id="65f23-103">Metodo ITabletEventSink:: SystemEvent</span><span class="sxs-lookup"><span data-stu-id="65f23-103">ITabletEventSink::SystemEvent method</span></span>

<span data-ttu-id="65f23-104">Si verifica quando è disponibile un evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="65f23-104">Occurs when a system event is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="65f23-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65f23-105">Syntax</span></span>


```C++
HRESULT SystemEvent(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] SYSTEM_EVENT      event,
  [in] SYSTEM_EVENT_DATA eventdata
);
```



## <a name="parameters"></a><span data-ttu-id="65f23-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="65f23-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65f23-107">*TCID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65f23-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f23-108">Identificatore del tablet.</span><span class="sxs-lookup"><span data-stu-id="65f23-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="65f23-109">*CID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65f23-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f23-110">Identificatore dello stilo.</span><span class="sxs-lookup"><span data-stu-id="65f23-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="65f23-111">*evento* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65f23-111">*event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f23-112">Codice dell'evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="65f23-112">The system event code.</span></span>

</dd> <dt>

<span data-ttu-id="65f23-113">*EventData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="65f23-113">*eventdata* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65f23-114">Dati dell'evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="65f23-114">The system event data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65f23-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65f23-115">Return value</span></span>

<span data-ttu-id="65f23-116">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="65f23-116">This method can return one of these values.</span></span>



| <span data-ttu-id="65f23-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="65f23-117">Return code</span></span>                                                                            | <span data-ttu-id="65f23-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65f23-118">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="65f23-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="65f23-119"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="65f23-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="65f23-120">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="65f23-121"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="65f23-121"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="65f23-122">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="65f23-122">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="65f23-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="65f23-123">Remarks</span></span>

<span data-ttu-id="65f23-124">Nell'elenco seguente sono riportati i valori validi per il parametro dell'evento.</span><span class="sxs-lookup"><span data-stu-id="65f23-124">The following list contains the valid values for the event parameter.</span></span>

-   <span data-ttu-id="65f23-125">\_tocco se</span><span class="sxs-lookup"><span data-stu-id="65f23-125">SE\_TAP</span></span>
-   <span data-ttu-id="65f23-126">SE \_ \_ tocco doppia</span><span class="sxs-lookup"><span data-stu-id="65f23-126">SE\_DBL\_TAP</span></span>
-   <span data-ttu-id="65f23-127">SE \_ \_ tocco destro</span><span class="sxs-lookup"><span data-stu-id="65f23-127">SE\_RIGHT\_TAP</span></span>
-   <span data-ttu-id="65f23-128">\_trascina se</span><span class="sxs-lookup"><span data-stu-id="65f23-128">SE\_DRAG</span></span>
-   <span data-ttu-id="65f23-129">trascina SE a \_ destra \_</span><span class="sxs-lookup"><span data-stu-id="65f23-129">SE\_RIGHT\_DRAG</span></span>
-   <span data-ttu-id="65f23-130">SE è in \_ attesa di \_ INVIO</span><span class="sxs-lookup"><span data-stu-id="65f23-130">SE\_HOLD\_ENTER</span></span>
-   <span data-ttu-id="65f23-131">\_Mantieni \_ uscita</span><span class="sxs-lookup"><span data-stu-id="65f23-131">SE\_HOLD\_LEAVE</span></span>
-   <span data-ttu-id="65f23-132">SE al \_ passaggio del mouse \_ immettere</span><span class="sxs-lookup"><span data-stu-id="65f23-132">SE\_HOVER\_ENTER</span></span>
-   <span data-ttu-id="65f23-133">SE il \_ passaggio del mouse viene \_ lasciato</span><span class="sxs-lookup"><span data-stu-id="65f23-133">SE\_HOVER\_LEAVE</span></span>
-   <span data-ttu-id="65f23-134">SE al \_ centro \_ fare clic</span><span class="sxs-lookup"><span data-stu-id="65f23-134">SE\_MIDDLE\_CLICK</span></span>
-   <span data-ttu-id="65f23-135">\_chiave se</span><span class="sxs-lookup"><span data-stu-id="65f23-135">SE\_KEY</span></span>
-   <span data-ttu-id="65f23-136">\_tasto di modifica se \_</span><span class="sxs-lookup"><span data-stu-id="65f23-136">SE\_MODIFIER\_KEY</span></span>
-   <span data-ttu-id="65f23-137">\_modalità movimento \_ se</span><span class="sxs-lookup"><span data-stu-id="65f23-137">SE\_GESTURE\_MODE</span></span>
-   <span data-ttu-id="65f23-138">\_cursore se</span><span class="sxs-lookup"><span data-stu-id="65f23-138">SE\_CURSOR</span></span>

## <a name="requirements"></a><span data-ttu-id="65f23-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65f23-139">Requirements</span></span>



| <span data-ttu-id="65f23-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="65f23-140">Requirement</span></span> | <span data-ttu-id="65f23-141">Valore</span><span class="sxs-lookup"><span data-stu-id="65f23-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65f23-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65f23-142">Minimum supported client</span></span><br/> | <span data-ttu-id="65f23-143">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="65f23-143">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="65f23-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65f23-144">Minimum supported server</span></span><br/> | <span data-ttu-id="65f23-145">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="65f23-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="65f23-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="65f23-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="65f23-147"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="65f23-147"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65f23-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65f23-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65f23-149">**Interfaccia ITabletEventSink**</span><span class="sxs-lookup"><span data-stu-id="65f23-149">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




