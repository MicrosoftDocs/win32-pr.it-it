---
title: Messaggio LVM_GETCOLUMNWIDTH (COMmctrl. h)
description: Ottiene la larghezza di una colonna in un report o in una visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetColumnWidth di ListView.
ms.assetid: 06e8ec36-3bc5-4516-ac29-17c36fb6d962
keywords:
- Controlli di Windows Message LVM_GETCOLUMNWIDTH
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0577e7cb2a589c432d4b5ca62f640de61d67dc75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119006"
---
# <a name="lvm_getcolumnwidth-message"></a><span data-ttu-id="d2abe-105">\_Messaggio GETCOLUMNWIDTH LVM</span><span class="sxs-lookup"><span data-stu-id="d2abe-105">LVM\_GETCOLUMNWIDTH message</span></span>

<span data-ttu-id="d2abe-106">Ottiene la larghezza di una colonna in un report o in una visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="d2abe-106">Gets the width of a column in report or list view.</span></span> <span data-ttu-id="d2abe-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetColumnWidth di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) .</span><span class="sxs-lookup"><span data-stu-id="d2abe-107">You can send this message explicitly or by using the [**ListView\_GetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d2abe-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d2abe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2abe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2abe-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2abe-110">Indice della colonna.</span><span class="sxs-lookup"><span data-stu-id="d2abe-110">The index of the column.</span></span> <span data-ttu-id="d2abe-111">Questo parametro viene ignorato in visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="d2abe-111">This parameter is ignored in list view.</span></span>

</dd> <dt>

<span data-ttu-id="d2abe-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2abe-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d2abe-113">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d2abe-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2abe-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d2abe-114">Return value</span></span>

<span data-ttu-id="d2abe-115">Restituisce la larghezza della colonna in caso di esito positivo; in caso contrario, zero.</span><span class="sxs-lookup"><span data-stu-id="d2abe-115">Returns the column width if successful, or zero otherwise.</span></span> <span data-ttu-id="d2abe-116">Se questo messaggio viene inviato a un controllo di visualizzazione elenco con lo stile del [**\_ report LVS**](list-view-window-styles.md) e la colonna specificata non esiste, il valore restituito non è definito.</span><span class="sxs-lookup"><span data-stu-id="d2abe-116">If this message is sent to a list-view control with the [**LVS\_REPORT**](list-view-window-styles.md) style and the specified column does not exist, the return value is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2abe-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d2abe-117">Requirements</span></span>



| <span data-ttu-id="d2abe-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2abe-118">Requirement</span></span> | <span data-ttu-id="d2abe-119">Valore</span><span class="sxs-lookup"><span data-stu-id="d2abe-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2abe-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2abe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d2abe-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d2abe-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d2abe-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d2abe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d2abe-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d2abe-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2abe-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d2abe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2abe-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2abe-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





