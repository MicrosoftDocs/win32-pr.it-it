---
title: TB_SETHOTITEM messaggio (Commctrl.h)
description: "TB_SETHOTITEM messaggio: imposta l'elemento di accesso rapido in una barra degli strumenti."
ms.assetid: 15005741-29d2-48c6-b5f0-15178a49b917
keywords:
- TB_SETHOTITEM messaggio Controlli Windows
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
ms.openlocfilehash: a90e5b38675d33a361857c4303fa2a89f22cff29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104179"
---
# <a name="tb_sethotitem-message"></a><span data-ttu-id="ec0fe-104">TB \_ SETHOTITEM message</span><span class="sxs-lookup"><span data-stu-id="ec0fe-104">TB\_SETHOTITEM message</span></span>

<span data-ttu-id="ec0fe-105">Imposta l'elemento di accesso rapido in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="ec0fe-105">Sets the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="ec0fe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ec0fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec0fe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ec0fe-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ec0fe-108">Indice dell'elemento che verrà reso a caldo.</span><span class="sxs-lookup"><span data-stu-id="ec0fe-108">Index of the item that will be made hot.</span></span> <span data-ttu-id="ec0fe-109">Se questo valore è -1, nessuno degli elementi sarà a caldo.</span><span class="sxs-lookup"><span data-stu-id="ec0fe-109">If this value is -1, none of the items will be hot.</span></span>

</dd> <dt>

<span data-ttu-id="ec0fe-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ec0fe-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ec0fe-111">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="ec0fe-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec0fe-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ec0fe-112">Return value</span></span>

<span data-ttu-id="ec0fe-113">Restituisce l'indice dell'elemento a caldo precedente oppure -1 se non è presente alcun elemento a caldo.</span><span class="sxs-lookup"><span data-stu-id="ec0fe-113">Returns the index of the previous hot item, or -1 if there was no hot item.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec0fe-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ec0fe-114">Remarks</span></span>

<span data-ttu-id="ec0fe-115">Il comportamento di questo messaggio non è definito per le barre degli strumenti che non hanno lo [**stile TBSTYLE \_ FLAT.**](toolbar-control-and-button-styles.md)</span><span class="sxs-lookup"><span data-stu-id="ec0fe-115">The behavior of this message is not defined for toolbars that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec0fe-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ec0fe-116">Requirements</span></span>



| <span data-ttu-id="ec0fe-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec0fe-117">Requirement</span></span> | <span data-ttu-id="ec0fe-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ec0fe-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec0fe-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec0fe-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ec0fe-120">Solo app desktop di Windows \[ Vista\]</span><span class="sxs-lookup"><span data-stu-id="ec0fe-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec0fe-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ec0fe-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ec0fe-122">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ec0fe-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ec0fe-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ec0fe-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec0fe-124"><dt>Commctrl.h</dt></span><span class="sxs-lookup"><span data-stu-id="ec0fe-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





