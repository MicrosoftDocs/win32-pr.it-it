---
title: Messaggio TB_SETBITMAPSIZE (COMmctrl. h)
description: Imposta la dimensione delle immagini bitmap da aggiungere a una barra degli strumenti.
ms.assetid: 20b99cd8-6ef1-4037-92d2-c64a1003b5fe
keywords:
- Controlli di Windows Message TB_SETBITMAPSIZE
topic_type:
- apiref
api_name:
- TB_SETBITMAPSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c8a717151041fb83b7a0206acf570a6ad7f76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475137"
---
# <a name="tb_setbitmapsize-message"></a><span data-ttu-id="2dbfd-104">TB \_ SETBITMAPSIZE messaggio</span><span class="sxs-lookup"><span data-stu-id="2dbfd-104">TB\_SETBITMAPSIZE message</span></span>

<span data-ttu-id="2dbfd-105">Imposta la dimensione delle immagini bitmap da aggiungere a una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="2dbfd-105">Sets the size of the bitmapped images to be added to a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="2dbfd-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2dbfd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dbfd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2dbfd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2dbfd-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2dbfd-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2dbfd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2dbfd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2dbfd-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifica la larghezza, in pixel, delle immagini bitmap.</span><span class="sxs-lookup"><span data-stu-id="2dbfd-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the width, in pixels, of the bitmapped images.</span></span> <span data-ttu-id="2dbfd-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifica l'altezza, in pixel, delle immagini bitmap.</span><span class="sxs-lookup"><span data-stu-id="2dbfd-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the height, in pixels, of the bitmapped images.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dbfd-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2dbfd-112">Return value</span></span>

<span data-ttu-id="2dbfd-113">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2dbfd-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2dbfd-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="2dbfd-114">Remarks</span></span>

<span data-ttu-id="2dbfd-115">È possibile impostare le dimensioni solo prima di aggiungere bitmap alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="2dbfd-115">The size can be set only before adding any bitmaps to the toolbar.</span></span> <span data-ttu-id="2dbfd-116">Se le dimensioni della bitmap non vengono impostate in modo esplicito in un'applicazione, le dimensioni predefinite sono pari a 16 per 15 pixel.</span><span class="sxs-lookup"><span data-stu-id="2dbfd-116">If an application does not explicitly set the bitmap size, the size defaults to 16 by 15 pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dbfd-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2dbfd-117">Requirements</span></span>



| <span data-ttu-id="2dbfd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dbfd-118">Requirement</span></span> | <span data-ttu-id="2dbfd-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2dbfd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2dbfd-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dbfd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2dbfd-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2dbfd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2dbfd-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dbfd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2dbfd-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2dbfd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2dbfd-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2dbfd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dbfd-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dbfd-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

