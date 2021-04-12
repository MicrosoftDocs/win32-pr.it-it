---
title: Messaggio di EM_SETAUTOCORRECTPROC (RichEdit. h)
description: Definisce la procedura di callback di correzione automatica corrente.
ms.assetid: 2FA48CFC-0D7C-41EF-8207-5EDC644FF3BC
keywords:
- Controlli di Windows Message EM_SETAUTOCORRECTPROC
topic_type:
- apiref
api_name:
- EM_SETAUTOCORRECTPROC
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7359c86c3fdabe4c410f600d0af3100dde4c4ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478592"
---
# <a name="em_setautocorrectproc-message"></a><span data-ttu-id="cc59e-104">\_Messaggio SETAUTOCORRECTPROC em</span><span class="sxs-lookup"><span data-stu-id="cc59e-104">EM\_SETAUTOCORRECTPROC message</span></span>

<span data-ttu-id="cc59e-105">Definisce la procedura di callback di correzione automatica corrente.</span><span class="sxs-lookup"><span data-stu-id="cc59e-105">Defines the current autocorrect callback procedure.</span></span>


```C++
#define EM_SETAUTOCORRECTPROC       (WM_USER + 234)
```



## <a name="parameters"></a><span data-ttu-id="cc59e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc59e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc59e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cc59e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc59e-108">Funzione di callback [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) .</span><span class="sxs-lookup"><span data-stu-id="cc59e-108">The [*AutoCorrectProc*](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc) callback function.</span></span>

</dd> <dt>

<span data-ttu-id="cc59e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cc59e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cc59e-110">Non utilizzato; deve essere zero</span><span class="sxs-lookup"><span data-stu-id="cc59e-110">Not used; must be zero</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc59e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc59e-111">Return value</span></span>

<span data-ttu-id="cc59e-112">Se l'operazione ha esito positivo, il valore restituito è zero.</span><span class="sxs-lookup"><span data-stu-id="cc59e-112">If the operation succeeds, the return value is zero.</span></span> <span data-ttu-id="cc59e-113">Se l'operazione ha esito negativo, il valore restituito è un valore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="cc59e-113">If the operation fails, the return value is a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc59e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc59e-114">Requirements</span></span>



| <span data-ttu-id="cc59e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc59e-115">Requirement</span></span> | <span data-ttu-id="cc59e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cc59e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc59e-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc59e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cc59e-118">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cc59e-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cc59e-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc59e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cc59e-120">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cc59e-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cc59e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc59e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc59e-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc59e-122"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc59e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc59e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc59e-124">*AutoCorrectProc*</span><span class="sxs-lookup"><span data-stu-id="cc59e-124">*AutoCorrectProc*</span></span>](/windows/desktop/api/Richedit/nc-richedit-autocorrectproc)
</dt> <dt>

[<span data-ttu-id="cc59e-125">**\_CALLAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="cc59e-125">**EM\_CALLAUTOCORRECTPROC**</span></span>](em-callautocorrectproc.md)
</dt> <dt>

[<span data-ttu-id="cc59e-126">**\_GETAUTOCORRECTPROC em**</span><span class="sxs-lookup"><span data-stu-id="cc59e-126">**EM\_GETAUTOCORRECTPROC**</span></span>](em-getautocorrectproc.md)
</dt> </dl>

 

 





