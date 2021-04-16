---
title: Messaggio di EM_GETIMECOMPMODE (RichEdit. h)
description: Recupera la modalità IME (Input Method Editor) corrente per un controllo Rich Edit.
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- Controlli di Windows Message EM_GETIMECOMPMODE
topic_type:
- apiref
api_name:
- EM_GETIMECOMPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feb2f5f31831e0e292bf002f24ca4978f25753a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477914"
---
# <a name="em_getimecompmode-message"></a><span data-ttu-id="95cae-104">\_Messaggio GETIMECOMPMODE em</span><span class="sxs-lookup"><span data-stu-id="95cae-104">EM\_GETIMECOMPMODE message</span></span>

<span data-ttu-id="95cae-105">Recupera la modalità IME (Input Method Editor) corrente per un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="95cae-105">Retrieves the current Input Method Editor (IME) mode for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="95cae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="95cae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95cae-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="95cae-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95cae-108">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="95cae-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="95cae-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="95cae-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="95cae-110">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="95cae-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95cae-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95cae-111">Return value</span></span>

<span data-ttu-id="95cae-112">Il valore restituito è uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="95cae-112">The return value is one of the following values.</span></span>



| <span data-ttu-id="95cae-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="95cae-113">Return code</span></span>                                                                                     | <span data-ttu-id="95cae-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95cae-114">Description</span></span>                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="95cae-115"><dt>**\_NOTOPEN ICM**</dt></span><span class="sxs-lookup"><span data-stu-id="95cae-115"><dt>**ICM\_NOTOPEN**</dt></span></span> </dl>     | <span data-ttu-id="95cae-116">IME non è aperto.</span><span class="sxs-lookup"><span data-stu-id="95cae-116">IME is not open.</span></span><br/>  |
| <dl> <span data-ttu-id="95cae-117"><dt>**\_Level3 ICM**</dt></span><span class="sxs-lookup"><span data-stu-id="95cae-117"><dt>**ICM\_LEVEL3**</dt></span></span> </dl>      | <span data-ttu-id="95cae-118">Modalità in linea true.</span><span class="sxs-lookup"><span data-stu-id="95cae-118">True inline mode.</span></span><br/> |
| <dl> <span data-ttu-id="95cae-119"><dt>**\_Level2 ICM**</dt></span><span class="sxs-lookup"><span data-stu-id="95cae-119"><dt>**ICM\_LEVEL2**</dt></span></span> </dl>      | <span data-ttu-id="95cae-120">Livello 2.</span><span class="sxs-lookup"><span data-stu-id="95cae-120">Level 2.</span></span><br/>          |
| <dl> <span data-ttu-id="95cae-121"><dt>**ICM \_ Level2 \_ 5**</dt></span><span class="sxs-lookup"><span data-stu-id="95cae-121"><dt>**ICM\_LEVEL2\_5**</dt></span></span> </dl>   | <span data-ttu-id="95cae-122">Livello 2,5</span><span class="sxs-lookup"><span data-stu-id="95cae-122">Level 2.5</span></span><br/>         |
| <dl> <span data-ttu-id="95cae-123"><dt>**ICM \_ Level2 \_ sui**</dt></span><span class="sxs-lookup"><span data-stu-id="95cae-123"><dt>**ICM\_LEVEL2\_SUI**</dt></span></span> </dl> | <span data-ttu-id="95cae-124">Interfaccia utente speciale.</span><span class="sxs-lookup"><span data-stu-id="95cae-124">Special UI.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="95cae-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95cae-125">Requirements</span></span>



| <span data-ttu-id="95cae-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="95cae-126">Requirement</span></span> | <span data-ttu-id="95cae-127">Valore</span><span class="sxs-lookup"><span data-stu-id="95cae-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95cae-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95cae-128">Minimum supported client</span></span><br/> | <span data-ttu-id="95cae-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95cae-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="95cae-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="95cae-130">Minimum supported server</span></span><br/> | <span data-ttu-id="95cae-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="95cae-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95cae-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="95cae-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="95cae-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="95cae-133"><dt>Richedit.h</dt></span></span> </dl> |



 

 





