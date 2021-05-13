---
description: Inviato da un'estensione di File Manager per recuperare le informazioni sull'unità dalla finestra di Gestione file attiva.
title: FM_GETDRIVEINFO messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_GETDRIVEINFO
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 142fff71-3a1b-4197-8c06-2e981cce4e4f
ms.openlocfilehash: 0abac794ed23eca30676a839a6eb5ad7c1079c3c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842412"
---
# <a name="fm_getdriveinfo-message"></a><span data-ttu-id="6463f-103">Messaggio \_ FM GETDRIVEINFO</span><span class="sxs-lookup"><span data-stu-id="6463f-103">FM\_GETDRIVEINFO message</span></span>

<span data-ttu-id="6463f-104">Inviato da un'estensione di File Manager per recuperare le informazioni sull'unità dalla finestra di Gestione file attiva.</span><span class="sxs-lookup"><span data-stu-id="6463f-104">Sent by a File Manager extension to retrieve drive information from the active File Manager window.</span></span>

## <a name="parameters"></a><span data-ttu-id="6463f-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="6463f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6463f-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6463f-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6463f-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="6463f-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6463f-108">*lpfmsgdi*</span><span class="sxs-lookup"><span data-stu-id="6463f-108">*lpfmsgdi*</span></span> 
</dt> <dd>

<span data-ttu-id="6463f-109">Indirizzo di una [**struttura FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) che riceve le informazioni sull'unità.</span><span class="sxs-lookup"><span data-stu-id="6463f-109">The address of an [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure that receives drive information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6463f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6463f-110">Return value</span></span>

<span data-ttu-id="6463f-111">Restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="6463f-111">Returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="6463f-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6463f-112">Remarks</span></span>

<span data-ttu-id="6463f-113">Se 0xFFFFFFFF viene restituito nel membro **dwTotalSpace** o **dwFreeSpace** della struttura [**FMS \_ GETDRIVEINFO,**](fms-getdriveinfo.md) la libreria di estensioni deve calcolare il valore o i valori.</span><span class="sxs-lookup"><span data-stu-id="6463f-113">If 0xFFFFFFFF is returned in the **dwTotalSpace** or **dwFreeSpace** member of the [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure, the extension library must compute the value or values.</span></span>

## <a name="requirements"></a><span data-ttu-id="6463f-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6463f-114">Requirements</span></span>



| <span data-ttu-id="6463f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6463f-115">Requirement</span></span> | <span data-ttu-id="6463f-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6463f-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6463f-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6463f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6463f-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6463f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="6463f-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6463f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6463f-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6463f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6463f-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6463f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6463f-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="6463f-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6463f-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6463f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6463f-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="6463f-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




