---
title: Messaggio MM_ACM_FORMATCHOOSE (Msacm. h)
description: Il \_ messaggio mm ACM \_ FORMATCHOOSE notifica a una funzione hook della finestra di dialogo acmFormatChoose prima di aggiungere un elemento a una delle tre caselle di riepilogo a discesa.
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- MM_ACM_FORMATCHOOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_ACM_FORMATCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35808e06521cbd83d07f8d6c799779a16f50236b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743922"
---
# <a name="mm_acm_formatchoose-message"></a><span data-ttu-id="bff0a-104">MM \_ \_ FORMATCHOOSE del messaggio ACM</span><span class="sxs-lookup"><span data-stu-id="bff0a-104">MM\_ACM\_FORMATCHOOSE message</span></span>

<span data-ttu-id="bff0a-105">Il messaggio **mm \_ ACM \_ FORMATCHOOSE** notifica a una funzione hook della finestra di dialogo [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) prima di aggiungere un elemento a una delle tre caselle di riepilogo a discesa.</span><span class="sxs-lookup"><span data-stu-id="bff0a-105">The **MM\_ACM\_FORMATCHOOSE** message notifies an [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) dialog hook function before adding an element to one of the three drop-down list boxes.</span></span> <span data-ttu-id="bff0a-106">Questo messaggio consente a un'applicazione di personalizzare ulteriormente le selezioni disponibili tramite l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="bff0a-106">This message allows an application to further customize the selections available through the user interface.</span></span>


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a><span data-ttu-id="bff0a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bff0a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bff0a-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span><span class="sxs-lookup"><span data-stu-id="bff0a-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span></span>
</dt> <dd>

<span data-ttu-id="bff0a-109">Casella di riepilogo a discesa inizializzata e operazione di verifica o di aggiunta.</span><span class="sxs-lookup"><span data-stu-id="bff0a-109">Drop-down list box being initialized and a verify or add operation.</span></span>



| <span data-ttu-id="bff0a-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="bff0a-110">Requirement</span></span> | <span data-ttu-id="bff0a-111">Valore</span><span class="sxs-lookup"><span data-stu-id="bff0a-111">Value</span></span> |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bff0a-112">\_verifica personalizzata di FORMATCHOOSE \_</span><span class="sxs-lookup"><span data-stu-id="bff0a-112">FORMATCHOOSE\_CUSTOM\_VERIFY</span></span>    | <span data-ttu-id="bff0a-113">Il parametro *lParam* è un puntatore a una struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) da aggiungere alla casella di riepilogo a discesa nome personalizzato.</span><span class="sxs-lookup"><span data-stu-id="bff0a-113">The *lParam* parameter is a pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the custom Name drop-down list box.</span></span>                                                                                                   |
| <span data-ttu-id="bff0a-114">\_aggiunta formato \_ FORMATCHOOSE</span><span class="sxs-lookup"><span data-stu-id="bff0a-114">FORMATCHOOSE\_FORMAT\_ADD</span></span>       | <span data-ttu-id="bff0a-115">Il parametro *lParam* è un puntatore a un buffer che accetterà una struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) da aggiungere alla casella di riepilogo a discesa formato.</span><span class="sxs-lookup"><span data-stu-id="bff0a-115">The *lParam* parameter is a pointer to a buffer that will accept a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the Format drop-down list box.</span></span> <span data-ttu-id="bff0a-116">L'applicazione deve copiare la struttura del formato da aggiungere in questo buffer.</span><span class="sxs-lookup"><span data-stu-id="bff0a-116">The application must copy the format structure to be added into this buffer.</span></span> |
| <span data-ttu-id="bff0a-117">\_verifica formato \_ FORMATCHOOSE</span><span class="sxs-lookup"><span data-stu-id="bff0a-117">FORMATCHOOSE\_FORMAT\_VERIFY</span></span>    | <span data-ttu-id="bff0a-118">Il parametro *lParam* è un puntatore a una struttura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) da aggiungere alla casella di riepilogo a discesa formato.</span><span class="sxs-lookup"><span data-stu-id="bff0a-118">The *lParam* parameter is a pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the Format drop-down list box.</span></span>                                                                                                        |
| <span data-ttu-id="bff0a-119">\_aggiunta FORMATCHOOSE FORMATTAG \_</span><span class="sxs-lookup"><span data-stu-id="bff0a-119">FORMATCHOOSE\_FORMATTAG\_ADD</span></span>    | <span data-ttu-id="bff0a-120">Il parametro *lParam* è un puntatore a una variabile che accetterà un tag di formato Waveform-Audio da aggiungere alla casella di riepilogo a discesa Tag di formato.</span><span class="sxs-lookup"><span data-stu-id="bff0a-120">The *lParam* parameter is a pointer to a variable that will accept a waveform-audio format tag to be added to the Format Tag drop-down list box.</span></span>                                                                                             |
| <span data-ttu-id="bff0a-121">\_Verifica FORMATTAG \_ FORMATCHOOSE</span><span class="sxs-lookup"><span data-stu-id="bff0a-121">FORMATCHOOSE\_FORMATTAG\_VERIFY</span></span> | <span data-ttu-id="bff0a-122">Il parametro *lParam* è un tag di formato della forma d'onda-audio da elencare nell'elenco a discesa Tag di formato.</span><span class="sxs-lookup"><span data-stu-id="bff0a-122">The *lParam* parameter is a waveform-audio format tag to be listed in the Format Tag drop-down list box.</span></span>                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="bff0a-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span><span class="sxs-lookup"><span data-stu-id="bff0a-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span></span>
</dt> <dd>

<span data-ttu-id="bff0a-124">Valore definito dalla casella di riepilogo specificata nel parametro **wParam** .</span><span class="sxs-lookup"><span data-stu-id="bff0a-124">Value defined by the listbox specified in the **wParam** parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bff0a-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bff0a-125">Return Value</span></span>

<span data-ttu-id="bff0a-126">Restituisce **true** se un'applicazione gestisce questo messaggio o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bff0a-126">Returns **TRUE** if an application handles this message or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bff0a-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="bff0a-127">Remarks</span></span>

<span data-ttu-id="bff0a-128">Se l'applicazione elabora l' \_ \_ operazione di aggiunta del formato FILTERCHOOSE, le dimensioni del buffer di memoria fornito in *lParam* verranno determinate dalla funzione [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .</span><span class="sxs-lookup"><span data-stu-id="bff0a-128">If the application processes the FILTERCHOOSE\_FORMAT\_ADD operation, the size of the memory buffer supplied in *lParam* will be determined from the [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) function.</span></span>

<span data-ttu-id="bff0a-129">Se l'applicazione sta elaborando un'operazione di verifica, può impedire alla finestra di dialogo di elencare questa selezione chiamando la funzione **SetWindowLong** con *NINDEX* impostato su DWL \_ MSGRESULT e *lNewLong* impostato su **false** (eseguito il cast a un tipo di dati **Long** ).</span><span class="sxs-lookup"><span data-stu-id="bff0a-129">If your application is processing a verify operation, it can prevent the dialog box from listing this selection by calling the **SetWindowLong** function with *nIndex* set to DWL\_MSGRESULT and *lNewLong* set to **FALSE** (cast to a **LONG** data type).</span></span> <span data-ttu-id="bff0a-130">Per consentire alla finestra di dialogo di elencare questa selezione, chiamare questa funzione con *lNewLong* impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="bff0a-130">To allow the dialog box to list this selection, call this function with *lNewLong* set to **TRUE**.</span></span>

<span data-ttu-id="bff0a-131">Se l'applicazione sta elaborando un'operazione di aggiunta, può indicare che non sono necessarie altre aggiunte chiamando la funzione **SetWindowLong** con *NINDEX* impostato su DWL \_ MSGRESULT e *lNewLong* impostato su **false** (eseguito il cast a un tipo di dati **Long** ).</span><span class="sxs-lookup"><span data-stu-id="bff0a-131">If your application is processing an add operation, it can indicate that no more additions are required by calling the **SetWindowLong** function with *nIndex* set to DWL\_MSGRESULT and *lNewLong* set to **FALSE** (cast to a **LONG** data type).</span></span> <span data-ttu-id="bff0a-132">Per indicare che sono necessarie altre aggiunte, chiamare questa funzione con *lNewLong* impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="bff0a-132">To indicate more additions are required, call this function with *lNewLong* set to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bff0a-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bff0a-133">Requirements</span></span>



| <span data-ttu-id="bff0a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="bff0a-134">Requirement</span></span> | <span data-ttu-id="bff0a-135">Valore</span><span class="sxs-lookup"><span data-stu-id="bff0a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bff0a-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bff0a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="bff0a-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bff0a-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bff0a-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bff0a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="bff0a-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bff0a-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bff0a-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bff0a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="bff0a-141"><dt>Msacm. h</dt></span><span class="sxs-lookup"><span data-stu-id="bff0a-141"><dt>Msacm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bff0a-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bff0a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bff0a-143">Gestione compressione audio</span><span class="sxs-lookup"><span data-stu-id="bff0a-143">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="bff0a-144">Messaggi di compressione audio</span><span class="sxs-lookup"><span data-stu-id="bff0a-144">Audio Compression Messages</span></span>](audio-compression-messages.md)
</dt> </dl>

 

