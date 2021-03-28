---
description: Inviato da un'estensione di file Manager per recuperare le informazioni relative a un file selezionato dalla finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca). Il file selezionato può avere un nome di file lungo.
title: Messaggio FM_GETFILESELLFN (Wfext. h)
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
ms.openlocfilehash: 847100f494772b3c59ad719d03d7bc2dbe28cc29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484045"
---
# <a name="fm_getfilesellfn-message"></a><span data-ttu-id="9e48a-104">\_Messaggio GETFILESELLFN FM</span><span class="sxs-lookup"><span data-stu-id="9e48a-104">FM\_GETFILESELLFN message</span></span>

<span data-ttu-id="9e48a-105">Inviato da un'estensione di file Manager per recuperare le informazioni relative a un file selezionato dalla finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).</span><span class="sxs-lookup"><span data-stu-id="9e48a-105">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span> <span data-ttu-id="9e48a-106">Il file selezionato può avere un nome di file lungo.</span><span class="sxs-lookup"><span data-stu-id="9e48a-106">The selected file can have a long file name.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e48a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e48a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e48a-108">*index*</span><span class="sxs-lookup"><span data-stu-id="9e48a-108">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="9e48a-109">Indice in base zero del file selezionato da recuperare.</span><span class="sxs-lookup"><span data-stu-id="9e48a-109">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="9e48a-110">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="9e48a-110">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="9e48a-111">Indirizzo di una struttura [**FMS \_ GETFILESEL**](fms-getfilesel.md) che riceve informazioni sulla selezione.</span><span class="sxs-lookup"><span data-stu-id="9e48a-111">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e48a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e48a-112">Return value</span></span>

<span data-ttu-id="9e48a-113">Restituisce l'indice in base zero del file selezionato recuperato.</span><span class="sxs-lookup"><span data-stu-id="9e48a-113">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e48a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e48a-114">Remarks</span></span>

<span data-ttu-id="9e48a-115">Questo messaggio deve essere utilizzato solo dalle estensioni che supportano nomi di file lunghi (ad esempio, le estensioni che supportano la rete).</span><span class="sxs-lookup"><span data-stu-id="9e48a-115">Only extensions that support long file names (for example, network-aware extensions) should use this message.</span></span>

<span data-ttu-id="9e48a-116">Un'estensione può usare il messaggio [**FM \_ GETSELCOUNTLFN**](fm-getselcountlfn.md) per recuperare il numero di file selezionati.</span><span class="sxs-lookup"><span data-stu-id="9e48a-116">An extension can use the [**FM\_GETSELCOUNTLFN**](fm-getselcountlfn.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e48a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e48a-117">Requirements</span></span>



| <span data-ttu-id="9e48a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e48a-118">Requirement</span></span> | <span data-ttu-id="9e48a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="9e48a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9e48a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e48a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9e48a-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9e48a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="9e48a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9e48a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9e48a-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9e48a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9e48a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e48a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e48a-125"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e48a-125"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e48a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e48a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e48a-127">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="9e48a-127">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="9e48a-128">**\_GETFILESEL FM**</span><span class="sxs-lookup"><span data-stu-id="9e48a-128">**FM\_GETFILESEL**</span></span>](fm-getfilesel.md)
</dt> <dt>

[<span data-ttu-id="9e48a-129">**\_GETSELCOUNT FM**</span><span class="sxs-lookup"><span data-stu-id="9e48a-129">**FM\_GETSELCOUNT**</span></span>](fm-getselcount.md)
</dt> </dl>

 

 




