---
title: Messaggio RB_HITTEST (COMmctrl. h)
description: Determina quale parte di una banda Rebar si trova in un determinato punto sullo schermo, se in quel punto esiste una banda del controllo Rebar.
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- Controlli di Windows Message RB_HITTEST
topic_type:
- apiref
api_name:
- RB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17283bfce255672391ba9d8b6acd60fe41045b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047921"
---
# <a name="rb_hittest-message"></a><span data-ttu-id="457c3-104">Messaggio di RB \_ HITTEST</span><span class="sxs-lookup"><span data-stu-id="457c3-104">RB\_HITTEST message</span></span>

<span data-ttu-id="457c3-105">Determina quale parte di una banda Rebar si trova in un determinato punto sullo schermo, se in quel punto esiste una banda del controllo Rebar.</span><span class="sxs-lookup"><span data-stu-id="457c3-105">Determines which portion of a rebar band is at a given point on the screen, if a rebar band exists at that point.</span></span>

## <a name="parameters"></a><span data-ttu-id="457c3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="457c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="457c3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="457c3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="457c3-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="457c3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="457c3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="457c3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="457c3-110">Puntatore a una struttura [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) .</span><span class="sxs-lookup"><span data-stu-id="457c3-110">Pointer to an [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) structure.</span></span> <span data-ttu-id="457c3-111">Prima di inviare il messaggio, è necessario inizializzare il membro **PT** di questa struttura sul punto che verrà sottoposto a hit testing, nelle coordinate del client.</span><span class="sxs-lookup"><span data-stu-id="457c3-111">Before sending the message, the **pt** member of this structure must be initialized to the point that will be hit tested, in client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="457c3-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="457c3-112">Return value</span></span>

<span data-ttu-id="457c3-113">Restituisce l'indice in base zero della banda nel punto specificato oppure-1 se non è presente alcuna banda del controllo Rebar nel punto.</span><span class="sxs-lookup"><span data-stu-id="457c3-113">Returns the zero-based index of the band at the given point, or -1 if no rebar band was at the point.</span></span>

## <a name="requirements"></a><span data-ttu-id="457c3-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="457c3-114">Requirements</span></span>



| <span data-ttu-id="457c3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="457c3-115">Requirement</span></span> | <span data-ttu-id="457c3-116">Valore</span><span class="sxs-lookup"><span data-stu-id="457c3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="457c3-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="457c3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="457c3-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="457c3-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="457c3-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="457c3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="457c3-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="457c3-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="457c3-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="457c3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="457c3-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="457c3-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





