---
description: Inviato da un'estensione di File Manager per recuperare informazioni su un file selezionato dalla finestra di Gestione file attiva (la finestra della directory o la finestra Risultati ricerca). Il file selezionato può avere un nome file lungo.
title: FM_GETFILESELLFN messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESELLFN
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 461fd171-d47f-41d6-953e-8e497e023ab1
ms.openlocfilehash: e991d2705f74aa8822dcef89878e9762f22b08dc
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842392"
---
# <a name="fm_getfilesellfn-message"></a><span data-ttu-id="0befd-104">Messaggio \_ FM GETFILESELLFN</span><span class="sxs-lookup"><span data-stu-id="0befd-104">FM\_GETFILESELLFN message</span></span>

<span data-ttu-id="0befd-105">Inviato da un'estensione di File Manager per recuperare informazioni su un file selezionato dalla finestra di Gestione file attiva (la finestra della directory o la finestra Risultati ricerca).</span><span class="sxs-lookup"><span data-stu-id="0befd-105">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="0befd-106">Il file selezionato può avere un nome file lungo.</span><span class="sxs-lookup"><span data-stu-id="0befd-106">The selected file can have a long file name.</span></span>

## <a name="parameters"></a><span data-ttu-id="0befd-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0befd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0befd-108">*index*</span><span class="sxs-lookup"><span data-stu-id="0befd-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="0befd-109">Indice in base zero del file selezionato da recuperare.</span><span class="sxs-lookup"><span data-stu-id="0befd-109">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="0befd-110">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="0befd-110">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="0befd-111">Indirizzo di una [**struttura \_ FMS GETFILESEL**](fms-getfilesel.md) che riceve informazioni sulla selezione.</span><span class="sxs-lookup"><span data-stu-id="0befd-111">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0befd-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0befd-112">Return value</span></span>

<span data-ttu-id="0befd-113">Restituisce l'indice in base zero del file selezionato recuperato.</span><span class="sxs-lookup"><span data-stu-id="0befd-113">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="0befd-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="0befd-114">Remarks</span></span>

<span data-ttu-id="0befd-115">Solo le estensioni che supportano nomi di file lunghi ( ad esempio, estensioni che supportano la rete) devono usare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="0befd-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

<span data-ttu-id="0befd-116">Un'estensione può usare [**il messaggio FM \_ GETSELCOUNTLFN**](fm-getselcountlfn.md) per recuperare il conteggio dei file selezionati.</span><span class="sxs-lookup"><span data-stu-id="0befd-116">An extension can use the [**FM\_GETSELCOUNTLFN**](fm-getselcountlfn.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="0befd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0befd-117">Requirements</span></span>



| <span data-ttu-id="0befd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0befd-118">Requirement</span></span> | <span data-ttu-id="0befd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="0befd-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0befd-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0befd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0befd-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0befd-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="0befd-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0befd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0befd-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0befd-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0befd-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0befd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0befd-125"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="0befd-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0befd-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0befd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0befd-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="0befd-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="0befd-128">**FM \_ GETFILESEL**</span><span class="sxs-lookup"><span data-stu-id="0befd-128">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="0befd-129">**FM \_ GETSELCOUNT**</span><span class="sxs-lookup"><span data-stu-id="0befd-129">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




