---
description: Inviato da un'estensione di file Manager per recuperare le informazioni relative a un file selezionato dalla finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).
title: Messaggio FM_GETFILESEL (Wfext. h)
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
ms.openlocfilehash: ec7d221e0c352c4b9284ae5fe2d6f80e50da85ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881590"
---
# <a name="fm_getfilesel-message"></a><span data-ttu-id="651d5-103">\_Messaggio GETFILESEL FM</span><span class="sxs-lookup"><span data-stu-id="651d5-103">FM\_GETFILESEL message</span></span>

<span data-ttu-id="651d5-104">Inviato da un'estensione di file Manager per recuperare le informazioni relative a un file selezionato dalla finestra Active File Manager (la finestra Directory o la finestra dei risultati della ricerca).</span><span class="sxs-lookup"><span data-stu-id="651d5-104">Sent by a File Manager extension to retrieve information about a selected file from the active File Manager window (either the directory window or the Search Results window).</span></span>

## <a name="parameters"></a><span data-ttu-id="651d5-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="651d5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="651d5-106">*index*</span><span class="sxs-lookup"><span data-stu-id="651d5-106">*index*</span></span> 
</dt> <dd>

<span data-ttu-id="651d5-107">Indice in base zero del file selezionato da recuperare.</span><span class="sxs-lookup"><span data-stu-id="651d5-107">The zero-based index of the selected file to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="651d5-108">*lpfmsgfs*</span><span class="sxs-lookup"><span data-stu-id="651d5-108">*lpfmsgfs*</span></span> 
</dt> <dd>

<span data-ttu-id="651d5-109">Indirizzo di una struttura [**FMS \_ GETFILESEL**](fms-getfilesel.md) che riceve informazioni sulla selezione.</span><span class="sxs-lookup"><span data-stu-id="651d5-109">The address of an [**FMS\_GETFILESEL**](fms-getfilesel.md) structure that receives information about the selection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="651d5-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="651d5-110">Return value</span></span>

<span data-ttu-id="651d5-111">Restituisce l'indice in base zero del file selezionato recuperato.</span><span class="sxs-lookup"><span data-stu-id="651d5-111">Returns the zero-based index of the selected file that was retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="651d5-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="651d5-112">Remarks</span></span>

<span data-ttu-id="651d5-113">Un'estensione può usare il messaggio [**FM \_ GETSELCOUNT**](fm-getselcount.md) per recuperare il numero di file selezionati.</span><span class="sxs-lookup"><span data-stu-id="651d5-113">An extension can use the [**FM\_GETSELCOUNT**](fm-getselcount.md) message to retrieve the count of selected files.</span></span>

## <a name="requirements"></a><span data-ttu-id="651d5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="651d5-114">Requirements</span></span>



| <span data-ttu-id="651d5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="651d5-115">Requirement</span></span> | <span data-ttu-id="651d5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="651d5-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="651d5-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="651d5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="651d5-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="651d5-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="651d5-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="651d5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="651d5-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="651d5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="651d5-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="651d5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="651d5-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="651d5-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="651d5-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="651d5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="651d5-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="651d5-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="651d5-125">**\_GETFILESELLFN FM**</span><span class="sxs-lookup"><span data-stu-id="651d5-125">**FM\_GETFILESELLFN**</span></span>](fm-getfilesellfn.md)
</dt> <dt>

[<span data-ttu-id="651d5-126">**\_GETSELCOUNTLFN FM**</span><span class="sxs-lookup"><span data-stu-id="651d5-126">**FM\_GETSELCOUNTLFN**</span></span>](fm-getselcountlfn.md)
</dt> </dl>

 

 




