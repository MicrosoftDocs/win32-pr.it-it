---
title: Messaggio CBEM_GETEDITCONTROL (COMmctrl. h)
description: Ottiene l'handle per la parte del controllo di modifica di un controllo ComboBoxEx. Un controllo ComboBoxEx usa una casella di modifica quando è impostata sullo stile a \_ discesa CBS.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- Controlli di Windows Message CBEM_GETEDITCONTROL
topic_type:
- apiref
api_name:
- CBEM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412d1183b29c8c89b5977d5f7f2a1b962d54dc01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121050"
---
# <a name="cbem_geteditcontrol-message"></a><span data-ttu-id="3899c-105">\_Messaggio CBEM GETEDITCONTROL</span><span class="sxs-lookup"><span data-stu-id="3899c-105">CBEM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="3899c-106">Ottiene l'handle per la parte del controllo di modifica di un controllo ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="3899c-106">Gets the handle to the edit control portion of a ComboBoxEx control.</span></span> <span data-ttu-id="3899c-107">Un controllo ComboBoxEx usa una casella di modifica quando è impostata sullo stile [**a \_ discesa CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="3899c-107">A ComboBoxEx control uses an edit box when it is set to the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="3899c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3899c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3899c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3899c-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3899c-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3899c-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3899c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3899c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3899c-112">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3899c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3899c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3899c-113">Return value</span></span>

<span data-ttu-id="3899c-114">Restituisce l'handle per il controllo di modifica all'interno del controllo ComboBoxEx se usa lo stile a [**\_ discesa CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="3899c-114">Returns the handle to the edit control within the ComboBoxEx control if it uses the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span> <span data-ttu-id="3899c-115">In caso contrario, il messaggio restituisce **null**.</span><span class="sxs-lookup"><span data-stu-id="3899c-115">Otherwise, the message returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3899c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3899c-116">Requirements</span></span>



| <span data-ttu-id="3899c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3899c-117">Requirement</span></span> | <span data-ttu-id="3899c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3899c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3899c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3899c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3899c-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3899c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3899c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3899c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3899c-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3899c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3899c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3899c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3899c-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3899c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





