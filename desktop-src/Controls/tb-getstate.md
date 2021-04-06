---
title: Messaggio TB_GETSTATE (COMmctrl. h)
description: Recupera le informazioni sullo stato del pulsante specificato in una barra degli strumenti, ad esempio se è abilitato, premuto o selezionato.
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- Controlli di Windows Message TB_GETSTATE
topic_type:
- apiref
api_name:
- TB_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3b5c50978da78218be7f3d47208c0ea430ff36c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873474"
---
# <a name="tb_getstate-message"></a><span data-ttu-id="76375-104">TB- \_ messaggio di stato</span><span class="sxs-lookup"><span data-stu-id="76375-104">TB\_GETSTATE message</span></span>

<span data-ttu-id="76375-105">Recupera le informazioni sullo stato del pulsante specificato in una barra degli strumenti, ad esempio se è abilitato, premuto o selezionato.</span><span class="sxs-lookup"><span data-stu-id="76375-105">Retrieves information about the state of the specified button in a toolbar, such as whether it is enabled, pressed, or checked.</span></span>

## <a name="parameters"></a><span data-ttu-id="76375-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="76375-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76375-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76375-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76375-108">Identificatore di comando del pulsante per il quale recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="76375-108">Command identifier of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="76375-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76375-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="76375-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="76375-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76375-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76375-111">Return value</span></span>

<span data-ttu-id="76375-112">Restituisce le informazioni sullo stato del pulsante in caso di esito positivo o-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="76375-112">Returns the button state information if successful, or -1 otherwise.</span></span> <span data-ttu-id="76375-113">Le informazioni sullo stato del pulsante possono essere una combinazione dei valori elencati negli [**stati dei pulsanti della barra degli strumenti**](toolbar-button-states.md).</span><span class="sxs-lookup"><span data-stu-id="76375-113">The button state information can be a combination of the values listed in [**Toolbar Button States**](toolbar-button-states.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="76375-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76375-114">Requirements</span></span>



| <span data-ttu-id="76375-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="76375-115">Requirement</span></span> | <span data-ttu-id="76375-116">Valore</span><span class="sxs-lookup"><span data-stu-id="76375-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76375-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76375-117">Minimum supported client</span></span><br/> | <span data-ttu-id="76375-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76375-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76375-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76375-119">Minimum supported server</span></span><br/> | <span data-ttu-id="76375-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="76375-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76375-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="76375-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="76375-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="76375-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





