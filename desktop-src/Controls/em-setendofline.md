---
title: Messaggio EM_SETENDOFLINE (CommCtrl. h)
description: Imposta il carattere di fine riga utilizzato quando viene inserito un LineBreak.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- Controlli di Windows Message EM_SETENDOFLINE
topic_type:
- apiref
api_name:
- EM_SETENDOFLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 5ee7c500ba3818cad0f5ee74e9994ed8af049ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478569"
---
# <a name="em_setendofline-message"></a><span data-ttu-id="1f7f5-104">\_Messaggio SETENDOFLINE em</span><span class="sxs-lookup"><span data-stu-id="1f7f5-104">EM\_SETENDOFLINE message</span></span>

<span data-ttu-id="1f7f5-105">Imposta il carattere di fine riga utilizzato quando viene inserito un LineBreak.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-105">Sets the end-of-line character used when a linebreak is inserted.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f7f5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f7f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f7f5-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f7f5-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f7f5-108">Specifica il carattere di fine riga utilizzato quando viene inserito un LineBreak.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-108">Specifies the end-of-line character used when a linebreak is inserted.</span></span> <span data-ttu-id="1f7f5-109">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-109">This can be one of the following values.</span></span>


| <span data-ttu-id="1f7f5-110">Valore</span><span class="sxs-lookup"><span data-stu-id="1f7f5-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="1f7f5-111">Significato</span><span class="sxs-lookup"><span data-stu-id="1f7f5-111">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <span data-ttu-id="1f7f5-112"><dt>**EC \_ ENDOFLINE \_ DETECTFROMCONTENT**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-112"><dt>**EC\_ENDOFLINE\_DETECTFROMCONTENT**</dt></span></span> </dl> | <span data-ttu-id="1f7f5-113">Imposta il carattere di fine riga utilizzato per il nuovo interruzioni sul carattere utilizzato dal documento corrente.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-113">Sets the end-of-line character used for new linebreaks to the character used by the current document.</span></span><br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <span data-ttu-id="1f7f5-114"><dt>**EC \_ ENDOFLINE \_ CRLF**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-114"><dt>**EC\_ENDOFLINE\_CRLF**</dt></span></span> </dl>                                        | <span data-ttu-id="1f7f5-115">Imposta il carattere di fine riga utilizzato per il nuovo interruzioni per il ritorno a capo seguito da avanzamento riga (CRLF).</span><span class="sxs-lookup"><span data-stu-id="1f7f5-115">Sets the end-of-line character used for new linebreaks to carriage return followed by linefeed (CRLF).</span></span><br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <span data-ttu-id="1f7f5-116"><dt>**EC \_ ENDOFLINE \_ CR**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-116"><dt>**EC\_ENDOFLINE\_CR**</dt></span></span> </dl>                                              | <span data-ttu-id="1f7f5-117">Imposta il carattere di fine riga utilizzato per il nuovo interruzioni per il ritorno a capo (CR).</span><span class="sxs-lookup"><span data-stu-id="1f7f5-117">Sets the end-of-line character used for new linebreaks to carriage return (CR).</span></span><br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <span data-ttu-id="1f7f5-118"><dt>**EC \_ ENDOFLINE \_ LF**</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-118"><dt>**EC\_ENDOFLINE\_LF**</dt></span></span> </dl>                                              | <span data-ttu-id="1f7f5-119">Imposta il carattere di fine riga utilizzato per il nuovo interruzioni di avanzamento riga (LF).</span><span class="sxs-lookup"><span data-stu-id="1f7f5-119">Sets the end-of-line character used for new linebreaks to linefeed (LF).</span></span><br/>                               |

</dd> <dt>

<span data-ttu-id="1f7f5-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f7f5-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f7f5-121">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-121">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f7f5-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1f7f5-122">Return value</span></span>

<span data-ttu-id="1f7f5-123">Se l'operazione ha esito positivo, il valore restituito è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-123">If the operation succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="1f7f5-124">Se l'operazione ha esito negativo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="1f7f5-124">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f7f5-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="1f7f5-125">Remarks</span></span>

<span data-ttu-id="1f7f5-126">Quando il set di caratteri di fine riga è **EC \_ ENDOFLINE \_ DETECTFROMCONTENT**, il controllo di modifica rileverà solo i caratteri di fine riga supportati in base allo stile della finestra estesa, vedere Modificare gli [stili estesi del controllo](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="1f7f5-126">When the end-of-line character set is **EC\_ENDOFLINE\_DETECTFROMCONTENT**, the edit control will only detect end-of-line characters supported according to its extended window style, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f7f5-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f7f5-127">Requirements</span></span>



| <span data-ttu-id="1f7f5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f7f5-128">Requirement</span></span> | <span data-ttu-id="1f7f5-129">Valore</span><span class="sxs-lookup"><span data-stu-id="1f7f5-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f7f5-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f7f5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1f7f5-131">Solo app desktop Windows 10, 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="1f7f5-131">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1f7f5-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f7f5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1f7f5-133">\[Solo app desktop Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="1f7f5-133">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1f7f5-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f7f5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f7f5-135"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f7f5-135"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f7f5-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1f7f5-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f7f5-137">\**\_GETENDOFLINE em*</span><span class="sxs-lookup"><span data-stu-id="1f7f5-137">\**EM\_GETENDOFLINE*</span></span>](em-getendofline.md)
</dt> </dl>

 

 





