---
title: Messaggio TB_SETHOTITEM (COMmctrl. h)
description: Imposta l'elemento attivo in una barra degli strumenti.
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- Controlli di Windows Message TB_SETHOTITEM
topic_type:
- apiref
api_name:
- TB_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c477a445cb6aae78dd5d31e8d23b8ec3be8c61ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874209"
---
# <a name="tb_sethotitem-message"></a><span data-ttu-id="4e95d-104">TB \_ SETHOTITEM messaggio</span><span class="sxs-lookup"><span data-stu-id="4e95d-104">TB\_SETHOTITEM message</span></span>

<span data-ttu-id="4e95d-105">Imposta l'elemento attivo in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="4e95d-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e95d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4e95d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e95d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e95d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e95d-108">Indice dell'elemento che verrà reso attivo.</span><span class="sxs-lookup"><span data-stu-id="4e95d-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="4e95d-109">Se questo valore è-1, nessuno degli elementi sarà attivo.</span><span class="sxs-lookup"><span data-stu-id="4e95d-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="4e95d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e95d-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4e95d-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="4e95d-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e95d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4e95d-112">Return value</span></span>

<span data-ttu-id="4e95d-113">Restituisce l'indice dell'elemento attivo precedente oppure-1 se non è presente alcun elemento attivo.</span><span class="sxs-lookup"><span data-stu-id="4e95d-113">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e95d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e95d-114">Remarks</span></span>

<span data-ttu-id="4e95d-115">Il comportamento di questo messaggio non è definito per le barre degli strumenti che non hanno lo stile [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="4e95d-115">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e95d-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e95d-116">Requirements</span></span>



| <span data-ttu-id="4e95d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e95d-117">Requirement</span></span> | <span data-ttu-id="4e95d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4e95d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4e95d-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e95d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4e95d-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e95d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4e95d-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e95d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4e95d-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4e95d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4e95d-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4e95d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e95d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e95d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





