---
description: Inviato da un'estensione di file Manager per recuperare le informazioni sull'unità dalla finestra di gestione file attiva.
title: Messaggio FM_GETDRIVEINFO (Wfext. h)
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
ms.openlocfilehash: 7accd78b36e82abbf56b02b133c79e92dd40d37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993704"
---
# <a name="fm_getdriveinfo-message"></a><span data-ttu-id="f06cc-103">\_Messaggio GETDRIVEINFO FM</span><span class="sxs-lookup"><span data-stu-id="f06cc-103">FM\_GETDRIVEINFO message</span></span>

<span data-ttu-id="f06cc-104">Inviato da un'estensione di file Manager per recuperare le informazioni sull'unità dalla finestra di gestione file attiva.</span><span class="sxs-lookup"><span data-stu-id="f06cc-104">Sent by a File Manager extension to retrieve drive information from the active File Manager window.</span></span>

## <a name="parameters"></a><span data-ttu-id="f06cc-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="f06cc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f06cc-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f06cc-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="f06cc-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f06cc-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="f06cc-108">*lpfmsgdi*</span><span class="sxs-lookup"><span data-stu-id="f06cc-108">*lpfmsgdi*</span></span> 
</dt> <dd>

<span data-ttu-id="f06cc-109">Indirizzo di una struttura [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) che riceve informazioni sull'unità.</span><span class="sxs-lookup"><span data-stu-id="f06cc-109">The address of an [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure that receives drive information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f06cc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f06cc-110">Return value</span></span>

<span data-ttu-id="f06cc-111">Restituisce un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="f06cc-111">Returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="f06cc-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="f06cc-112">Remarks</span></span>

<span data-ttu-id="f06cc-113">Se 0xFFFFFFFF viene restituito nel membro **dwTotalSpace** o **DwFreeSpace** della struttura [**FMS \_ GETDRIVEINFO**](fms-getdriveinfo.md) , la libreria di estensioni deve calcolare il valore o i valori.</span><span class="sxs-lookup"><span data-stu-id="f06cc-113">If 0xFFFFFFFF is returned in the **dwTotalSpace** or **dwFreeSpace** member of the [**FMS\_GETDRIVEINFO**](fms-getdriveinfo.md) structure, the extension library must compute the value or values.</span></span>

## <a name="requirements"></a><span data-ttu-id="f06cc-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f06cc-114">Requirements</span></span>



| <span data-ttu-id="f06cc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f06cc-115">Requirement</span></span> | <span data-ttu-id="f06cc-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f06cc-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f06cc-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f06cc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f06cc-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f06cc-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f06cc-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f06cc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f06cc-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f06cc-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f06cc-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f06cc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f06cc-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="f06cc-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f06cc-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f06cc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f06cc-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="f06cc-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




