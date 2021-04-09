---
title: Messaggio MM_ACM_FILTERCHOOSE (Msacm. h)
description: Il \_ messaggio mm ACM \_ FILTERCHOOSE notifica a una funzione di hook della finestra di dialogo acmFilterChoose prima di aggiungere un elemento a una delle tre caselle di riepilogo a discesa.
ms.assetid: f3c68240-a9aa-4771-96b9-1cb3bb5ea906
keywords:
- MM_ACM_FILTERCHOOSE messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MM_ACM_FILTERCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df28ad7f950b8ce995fd308622db8c429393cb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119143"
---
# <a name="mm_acm_filterchoose-message"></a><span data-ttu-id="50804-104">MM \_ \_ FILTERCHOOSE del messaggio ACM</span><span class="sxs-lookup"><span data-stu-id="50804-104">MM\_ACM\_FILTERCHOOSE message</span></span>

<span data-ttu-id="50804-105">Il messaggio **mm \_ ACM \_ FILTERCHOOSE** notifica a una funzione di hook della finestra di dialogo [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) prima di aggiungere un elemento a una delle tre caselle di riepilogo a discesa.</span><span class="sxs-lookup"><span data-stu-id="50804-105">The **MM\_ACM\_FILTERCHOOSE** message notifies an [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) dialog box hook function before adding an element to one of the three drop-down list boxes.</span></span> <span data-ttu-id="50804-106">Questo messaggio consente a un'applicazione di personalizzare ulteriormente le selezioni disponibili tramite l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="50804-106">This message allows an application to further customize the selections available through the user interface.</span></span>


```C++
        MM_ACM_FILTERCHOOSE
        wParam = (WPARAM) wDropDown
        lParam = (LONG) lCustom
      
```



## <a name="parameters"></a><span data-ttu-id="50804-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="50804-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50804-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span><span class="sxs-lookup"><span data-stu-id="50804-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span></span>
</dt> <dd>

<span data-ttu-id="50804-109">Casella di riepilogo a discesa inizializzata e operazione di verifica o di aggiunta.</span><span class="sxs-lookup"><span data-stu-id="50804-109">Drop-down list box being initialized and a verify or add operation.</span></span>



| <span data-ttu-id="50804-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="50804-110">Requirement</span></span> | <span data-ttu-id="50804-111">Valore</span><span class="sxs-lookup"><span data-stu-id="50804-111">Value</span></span> |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50804-112">\_verifica personalizzata di FILTERCHOOSE \_</span><span class="sxs-lookup"><span data-stu-id="50804-112">FILTERCHOOSE\_CUSTOM\_VERIFY</span></span>    | <span data-ttu-id="50804-113">Il parametro *lParam* è un puntatore a una struttura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) da aggiungere alla casella di riepilogo a discesa nome personalizzato.</span><span class="sxs-lookup"><span data-stu-id="50804-113">The *lParam* parameter is a pointer to a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the custom Name drop-down list box.</span></span>                                                                                                   |
| <span data-ttu-id="50804-114">\_aggiunta filtro \_ FILTERCHOOSE</span><span class="sxs-lookup"><span data-stu-id="50804-114">FILTERCHOOSE\_FILTER\_ADD</span></span>       | <span data-ttu-id="50804-115">Il parametro *lParam* è un puntatore a un buffer che accetterà una struttura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) da aggiungere all'elenco a discesa del filtro.</span><span class="sxs-lookup"><span data-stu-id="50804-115">The *lParam* parameter is a pointer to a buffer that will accept a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the Filter drop-down list box.</span></span> <span data-ttu-id="50804-116">L'applicazione deve copiare la struttura del filtro da aggiungere in questo buffer.</span><span class="sxs-lookup"><span data-stu-id="50804-116">The application must copy the filter structure to be added into this buffer.</span></span> |
| <span data-ttu-id="50804-117">\_Verifica del filtro FILTERCHOOSE \_</span><span class="sxs-lookup"><span data-stu-id="50804-117">FILTERCHOOSE\_FILTER\_VERIFY</span></span>    | <span data-ttu-id="50804-118">Il parametro *lParam* è un puntatore a una struttura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) da aggiungere alla casella di riepilogo a discesa filtro.</span><span class="sxs-lookup"><span data-stu-id="50804-118">The *lParam* parameter is a pointer to a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the Filter drop-down list box.</span></span>                                                                                                        |
| <span data-ttu-id="50804-119">\_aggiunta FILTERCHOOSE FILTERTAG \_</span><span class="sxs-lookup"><span data-stu-id="50804-119">FILTERCHOOSE\_FILTERTAG\_ADD</span></span>    | <span data-ttu-id="50804-120">Il parametro *lParam* è un puntatore a un **valore DWORD** che accetterà un tag di filtro della forma d'onda-audio da aggiungere alla casella di riepilogo a discesa Tag filtro.</span><span class="sxs-lookup"><span data-stu-id="50804-120">The *lParam* parameter is a pointer to a **DWORD** that will accept a waveform-audio filter tag to be added to the Filter Tag drop-down list box.</span></span>                                                                                        |
| <span data-ttu-id="50804-121">\_Verifica FILTERTAG \_ FILTERCHOOSE</span><span class="sxs-lookup"><span data-stu-id="50804-121">FILTERCHOOSE\_FILTERTAG\_VERIFY</span></span> | <span data-ttu-id="50804-122">Il parametro *lParam* è un tag del filtro per la forma d'onda, che deve essere elencato nella casella di riepilogo a discesa Tag filtro.</span><span class="sxs-lookup"><span data-stu-id="50804-122">The *lParam* parameter is a waveform-audio filter tag to be listed in the Filter Tag drop-down list box.</span></span>                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="50804-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span><span class="sxs-lookup"><span data-stu-id="50804-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span></span>
</dt> <dd>

<span data-ttu-id="50804-124">Valore definito dalla casella di riepilogo specificata nel parametro **wParam** .</span><span class="sxs-lookup"><span data-stu-id="50804-124">Value defined by the list box specified in the **wParam** parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50804-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50804-125">Return Value</span></span>

<span data-ttu-id="50804-126">Restituisce **true** se un'applicazione gestisce questo messaggio o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="50804-126">Returns **TRUE** if an application handles this message or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="50804-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="50804-127">Remarks</span></span>

<span data-ttu-id="50804-128">Se l'applicazione elabora l' \_ \_ operazione di aggiunta del filtro FILTERCHOOSE, le dimensioni del buffer di memoria fornito in *lParam* verranno determinate dalla funzione [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .</span><span class="sxs-lookup"><span data-stu-id="50804-128">If the application processes the FILTERCHOOSE\_FILTER\_ADD operation, the size of the memory buffer supplied in *lParam* will be determined from the [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) function.</span></span>

<span data-ttu-id="50804-129">Se l'applicazione elabora un'operazione di verifica, l'applicazione deve precedere il valore restituito con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long) **false**) per impedire che la finestra di dialogo elenchi questa selezione o con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**true**) per consentire alla finestra di dialogo di elencare questa selezione.</span><span class="sxs-lookup"><span data-stu-id="50804-129">If the application processes a verify operation, the application must precede the return value with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG) **FALSE**) to prevent the dialog box from listing this selection or with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**TRUE**) to allow the dialog box to list this selection.</span></span> <span data-ttu-id="50804-130">Se si elabora un'operazione di aggiunta, l'applicazione deve precedere la restituzione con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**false**) per indicare che non sono necessarie altre aggiunte o con **SetWindowLong** (HWND, DWL \_ MSGRESULT, (Long)**true**) se sono necessarie altre aggiunte.</span><span class="sxs-lookup"><span data-stu-id="50804-130">If processing an add operation, the application must precede the return with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**FALSE**) to indicate that no more additions are required or with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**TRUE**) if more additions are required.</span></span>

## <a name="requirements"></a><span data-ttu-id="50804-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50804-131">Requirements</span></span>



| <span data-ttu-id="50804-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="50804-132">Requirement</span></span> | <span data-ttu-id="50804-133">Valore</span><span class="sxs-lookup"><span data-stu-id="50804-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50804-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50804-134">Minimum supported client</span></span><br/> | <span data-ttu-id="50804-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="50804-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="50804-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="50804-136">Minimum supported server</span></span><br/> | <span data-ttu-id="50804-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="50804-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="50804-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50804-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="50804-139"><dt>Msacm. h</dt></span><span class="sxs-lookup"><span data-stu-id="50804-139"><dt>Msacm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50804-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50804-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50804-141">Gestione compressione audio</span><span class="sxs-lookup"><span data-stu-id="50804-141">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="50804-142">Messaggi di compressione audio</span><span class="sxs-lookup"><span data-stu-id="50804-142">Audio Compression Messages</span></span>](audio-compression-messages.md)
</dt> </dl>

 

 





