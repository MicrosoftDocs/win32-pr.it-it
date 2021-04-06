---
title: Messaggio TB_GETBUTTON (COMmctrl. h)
description: Recupera le informazioni sul pulsante specificato in una barra degli strumenti.
ms.assetid: d90d053c-0daf-4a5a-b7ca-b9b4472c65a3
keywords:
- Controlli di Windows Message TB_GETBUTTON
topic_type:
- apiref
api_name:
- TB_GETBUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2080a6c984bb2384f68a1388bd46fe598f5087
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743962"
---
# <a name="tb_getbutton-message"></a><span data-ttu-id="91179-104">\_Messaggio GETBUTTON TB</span><span class="sxs-lookup"><span data-stu-id="91179-104">TB\_GETBUTTON message</span></span>

<span data-ttu-id="91179-105">Recupera le informazioni sul pulsante specificato in una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="91179-105">Retrieves information about the specified button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="91179-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="91179-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91179-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91179-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91179-108">Indice in base zero del pulsante per il quale recuperare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="91179-108">Zero-based index of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="91179-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91179-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91179-110">Puntatore alla struttura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) che riceve le informazioni sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="91179-110">Pointer to the [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure that receives the button information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91179-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91179-111">Return value</span></span>

<span data-ttu-id="91179-112">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="91179-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="91179-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91179-113">Requirements</span></span>



| <span data-ttu-id="91179-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="91179-114">Requirement</span></span> | <span data-ttu-id="91179-115">Valore</span><span class="sxs-lookup"><span data-stu-id="91179-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91179-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91179-116">Minimum supported client</span></span><br/> | <span data-ttu-id="91179-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="91179-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91179-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91179-118">Minimum supported server</span></span><br/> | <span data-ttu-id="91179-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="91179-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91179-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91179-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="91179-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="91179-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





