---
title: Messaggio di EM_EXLINEFROMCHAR (RichEdit. h)
description: Determina quale riga contiene il carattere specificato in un controllo Rich Edit.
ms.assetid: 497482fb-9640-4063-a9f5-e0691b65225d
keywords:
- Controlli di Windows Message EM_EXLINEFROMCHAR
topic_type:
- apiref
api_name:
- EM_EXLINEFROMCHAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce904725c5dc63732bae07cfaa95b41558db11d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479465"
---
# <a name="em_exlinefromchar-message"></a><span data-ttu-id="b8a7a-104">\_Messaggio EXLINEFROMCHAR em</span><span class="sxs-lookup"><span data-stu-id="b8a7a-104">EM\_EXLINEFROMCHAR message</span></span>

<span data-ttu-id="b8a7a-105">Determina quale riga contiene il carattere specificato in un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="b8a7a-105">Determines which line contains the specified character in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8a7a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8a7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8a7a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b8a7a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8a7a-108">Questo parametro non viene utilizzato. deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b8a7a-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="b8a7a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b8a7a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b8a7a-110">Indice in base zero del carattere.</span><span class="sxs-lookup"><span data-stu-id="b8a7a-110">Zero-based index of the character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8a7a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b8a7a-111">Return value</span></span>

<span data-ttu-id="b8a7a-112">Questo messaggio restituisce l'indice in base zero della riga.</span><span class="sxs-lookup"><span data-stu-id="b8a7a-112">This message returns the zero-based index of the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8a7a-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8a7a-113">Requirements</span></span>



| <span data-ttu-id="b8a7a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8a7a-114">Requirement</span></span> | <span data-ttu-id="b8a7a-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b8a7a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a7a-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8a7a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b8a7a-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b8a7a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b8a7a-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8a7a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b8a7a-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b8a7a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b8a7a-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8a7a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8a7a-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8a7a-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





