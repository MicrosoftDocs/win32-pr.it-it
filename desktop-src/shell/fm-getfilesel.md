---
description: Inviato da un'estensione di File Manager per recuperare le informazioni su un file selezionato dalla finestra di Gestione file attiva (nella finestra della directory o nella finestra Risultati ricerca).
title: FM_GETFILESEL messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c2b4aac6-165b-4eba-b012-ee7a20481cd3
ms.openlocfilehash: 2da95a39f8e84215640e926ae21a043865223665
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841422"
---
# <a name="fm_getfilesel-message"></a><span data-ttu-id="cda1d-103">Messaggio \_ FM GETFILESEL</span><span class="sxs-lookup"><span data-stu-id="cda1d-103">FM\_GETFILESEL message</span></span>

<span data-ttu-id="cda1d-104">Inviato da un'estensione di File Manager per recuperare le informazioni su un file selezionato dalla finestra di Gestione file attiva (nella finestra della directory o nella finestra Risultati ricerca).</span><span class="sxs-lookup"><span data-stu-id="cda1d-104">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="cda1d-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="cda1d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cda1d-106">*index*</span><span class="sxs-lookup"><span data-stu-id="cda1d-106">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="cda1d-107">Indice in base zero del file selezionato da recuperare.</span><span class="sxs-lookup"><span data-stu-id="cda1d-107">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="cda1d-108">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="cda1d-108">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="cda1d-109">Indirizzo di una [**struttura \_ FMS GETFILESEL**](fms-getfilesel.md) che riceve informazioni sulla selezione.</span><span class="sxs-lookup"><span data-stu-id="cda1d-109">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cda1d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cda1d-110">Return value</span></span>

<span data-ttu-id="cda1d-111">Restituisce l'indice in base zero del file selezionato recuperato.</span><span class="sxs-lookup"><span data-stu-id="cda1d-111">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="cda1d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="cda1d-112">Remarks</span></span>

<span data-ttu-id="cda1d-113">Un'estensione può usare il [**messaggio FM \_ GETSELCOUNT**](fm-getselcount.md) per recuperare il conteggio dei file selezionati.</span><span class="sxs-lookup"><span data-stu-id="cda1d-113">An extension can use the [**FM\_GETSELCOUNT**](fm-getselcount.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="cda1d-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cda1d-114">Requirements</span></span>



| <span data-ttu-id="cda1d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cda1d-115">Requirement</span></span> | <span data-ttu-id="cda1d-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cda1d-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cda1d-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cda1d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cda1d-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cda1d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="cda1d-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cda1d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cda1d-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cda1d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="cda1d-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cda1d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cda1d-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="cda1d-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cda1d-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cda1d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda1d-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="cda1d-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="cda1d-125">**FM \_ GETFILESELLFN**</span><span class="sxs-lookup"><span data-stu-id="cda1d-125">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="cda1d-126">**FM \_ GETSELCOUNTLFN**</span><span class="sxs-lookup"><span data-stu-id="cda1d-126">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




