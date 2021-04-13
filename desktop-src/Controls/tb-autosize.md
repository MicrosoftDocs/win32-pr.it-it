---
title: Messaggio TB_AUTOSIZE (COMmctrl. h)
description: Determina il ridimensionamento di una barra degli strumenti.
ms.assetid: 11aff184-6f18-43a2-9bdc-462fc5ba1680
keywords:
- Controlli di Windows Message TB_AUTOSIZE
topic_type:
- apiref
api_name:
- TB_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5f901463888338fd9cadf67472232efe9a25f29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519310"
---
# <a name="tb_autosize-message"></a><span data-ttu-id="91d1d-104">\_Messaggio AUTOSIZE TB</span><span class="sxs-lookup"><span data-stu-id="91d1d-104">TB\_AUTOSIZE message</span></span>

<span data-ttu-id="91d1d-105">Determina il ridimensionamento di una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="91d1d-105">Causes a toolbar to be resized.</span></span>

## <a name="parameters"></a><span data-ttu-id="91d1d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="91d1d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91d1d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91d1d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="91d1d-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="91d1d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="91d1d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91d1d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="91d1d-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="91d1d-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91d1d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="91d1d-111">Return value</span></span>

<span data-ttu-id="91d1d-112">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="91d1d-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="91d1d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="91d1d-113">Remarks</span></span>

<span data-ttu-id="91d1d-114">Un'applicazione invia il messaggio di **\_ ridimensionamento automatico TB** dopo aver causato la modifica delle dimensioni di una barra degli strumenti impostando le dimensioni del pulsante o della bitmap oppure aggiungendo stringhe per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="91d1d-114">An application sends the **TB\_AUTOSIZE** message after causing the size of a toolbar to change either by setting the button or bitmap size or by adding strings for the first time.</span></span>

## <a name="requirements"></a><span data-ttu-id="91d1d-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91d1d-115">Requirements</span></span>



| <span data-ttu-id="91d1d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="91d1d-116">Requirement</span></span> | <span data-ttu-id="91d1d-117">Valore</span><span class="sxs-lookup"><span data-stu-id="91d1d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91d1d-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91d1d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="91d1d-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="91d1d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91d1d-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91d1d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="91d1d-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="91d1d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91d1d-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="91d1d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="91d1d-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="91d1d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





