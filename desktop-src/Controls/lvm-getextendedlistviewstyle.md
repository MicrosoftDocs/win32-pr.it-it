---
title: Messaggio LVM_GETEXTENDEDLISTVIEWSTYLE (COMmctrl. h)
description: Ottiene gli stili estesi attualmente in uso per un determinato controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro GetExtendedListViewStyle di ListView.
ms.assetid: 5cfccdb8-a81c-4fa9-a4fa-19cf49bd6ce0
keywords:
- Controlli di Windows Message LVM_GETEXTENDEDLISTVIEWSTYLE
topic_type:
- apiref
api_name:
- LVM_GETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 273da9e7eac85475b90ad05dc5fdd7f70d524562
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047859"
---
# <a name="lvm_getextendedlistviewstyle-message"></a><span data-ttu-id="103f7-105">\_Messaggio GETEXTENDEDLISTVIEWSTYLE LVM</span><span class="sxs-lookup"><span data-stu-id="103f7-105">LVM\_GETEXTENDEDLISTVIEWSTYLE message</span></span>

<span data-ttu-id="103f7-106">Ottiene gli stili estesi attualmente in uso per un determinato controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="103f7-106">Gets the extended styles that are currently in use for a given list-view control.</span></span> <span data-ttu-id="103f7-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ GetExtendedListViewStyle di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) .</span><span class="sxs-lookup"><span data-stu-id="103f7-107">You can send this message explicitly or use the [**ListView\_GetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getextendedlistviewstyle) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="103f7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="103f7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="103f7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="103f7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="103f7-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="103f7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="103f7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="103f7-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="103f7-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="103f7-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="103f7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="103f7-113">Return value</span></span>

<span data-ttu-id="103f7-114">Restituisce un **valore DWORD** che rappresenta gli stili attualmente in uso per un determinato controllo di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="103f7-114">Returns a **DWORD** that represents the styles currently in use for a given list-view control.</span></span> <span data-ttu-id="103f7-115">Questo valore può essere una combinazione di [stili di List-View estesa](extended-list-view-styles.md).</span><span class="sxs-lookup"><span data-stu-id="103f7-115">This value can be a combination of [Extended List-View Styles](extended-list-view-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="103f7-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="103f7-116">Requirements</span></span>



| <span data-ttu-id="103f7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="103f7-117">Requirement</span></span> | <span data-ttu-id="103f7-118">Valore</span><span class="sxs-lookup"><span data-stu-id="103f7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="103f7-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="103f7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="103f7-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="103f7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="103f7-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="103f7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="103f7-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="103f7-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="103f7-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="103f7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="103f7-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="103f7-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





