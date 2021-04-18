---
title: Messaggio TB_SETCMDID (COMmctrl. h)
description: Imposta l'identificatore del comando di un pulsante della barra degli strumenti.
ms.assetid: 0674c905-2d9d-45d3-b565-2f3bcd7d6383
keywords:
- Controlli di Windows Message TB_SETCMDID
topic_type:
- apiref
api_name:
- TB_SETCMDID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f91cc4fd4d70e912bed3163cdf783e8e17ab463
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301668"
---
# <a name="tb_setcmdid-message"></a><span data-ttu-id="2a1d3-104">TB \_ SETCMDID messaggio</span><span class="sxs-lookup"><span data-stu-id="2a1d3-104">TB\_SETCMDID message</span></span>

<span data-ttu-id="2a1d3-105">Imposta l'identificatore del comando di un pulsante della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-105">Sets the command identifier of a toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a1d3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2a1d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a1d3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a1d3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a1d3-108">Indice in base zero del pulsante di cui è necessario impostare l'identificatore di comando.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-108">Zero-based index of the button whose command identifier is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="2a1d3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a1d3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a1d3-110">Identificatore del comando.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-110">Command identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a1d3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2a1d3-111">Return value</span></span>

<span data-ttu-id="2a1d3-112">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a1d3-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2a1d3-113">Requirements</span></span>



| <span data-ttu-id="2a1d3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a1d3-114">Requirement</span></span> | <span data-ttu-id="2a1d3-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2a1d3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a1d3-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a1d3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2a1d3-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2a1d3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2a1d3-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2a1d3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2a1d3-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2a1d3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2a1d3-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2a1d3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a1d3-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a1d3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





