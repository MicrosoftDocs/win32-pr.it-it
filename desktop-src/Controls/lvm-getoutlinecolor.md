---
title: Messaggio LVM_GETOUTLINECOLOR (COMmctrl. h)
description: Recupera il colore del bordo di un controllo di visualizzazione elenco se \_ \_ è impostato lo stile della finestra estesa LVS ex BORDERSELECT.
ms.assetid: cc9d69d1-1470-4eaa-8d54-e31b796cf685
keywords:
- Controlli di Windows Message LVM_GETOUTLINECOLOR
topic_type:
- apiref
api_name:
- LVM_GETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489f21f2f6d4dcca2c79d92a13a85d7718a85693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874322"
---
# <a name="lvm_getoutlinecolor-message"></a><span data-ttu-id="b2d7f-104">\_Messaggio GETOUTLINECOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="b2d7f-104">LVM\_GETOUTLINECOLOR message</span></span>

<span data-ttu-id="b2d7f-105">Recupera il colore del bordo di un controllo di visualizzazione elenco se è impostato lo stile della finestra estesa [**LVS \_ ex \_ BORDERSELECT**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="b2d7f-105">Retrieves the color of the border of a list-view control if the [**LVS\_EX\_BORDERSELECT**](extended-list-view-styles.md) extended window style is set.</span></span>

## <a name="parameters"></a><span data-ttu-id="b2d7f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b2d7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2d7f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b2d7f-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b2d7f-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b2d7f-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b2d7f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b2d7f-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b2d7f-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b2d7f-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2d7f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b2d7f-111">Return value</span></span>

<span data-ttu-id="b2d7f-112">Restituisce una struttura **COLORREF** che contiene il colore del bordo di un controllo di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="b2d7f-112">Returns a **COLORREF** structure that contains the color of the border of a list-view control.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2d7f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="b2d7f-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b2d7f-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="b2d7f-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b2d7f-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b2d7f-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b2d7f-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b2d7f-116">Requirements</span></span>



| <span data-ttu-id="b2d7f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2d7f-117">Requirement</span></span> | <span data-ttu-id="b2d7f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="b2d7f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2d7f-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2d7f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b2d7f-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2d7f-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b2d7f-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b2d7f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b2d7f-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b2d7f-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b2d7f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b2d7f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2d7f-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2d7f-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





