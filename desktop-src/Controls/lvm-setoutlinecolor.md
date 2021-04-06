---
title: Messaggio LVM_SETOUTLINECOLOR (COMmctrl. h)
description: Imposta il colore del bordo di un controllo di visualizzazione elenco se \_ \_ è impostato lo stile della finestra estesa LVS ex BORDERSELECT.
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- Controlli di Windows Message LVM_SETOUTLINECOLOR
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 776cb13479e4d091d394941844691c117a4ebbef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873318"
---
# <a name="lvm_setoutlinecolor-message"></a><span data-ttu-id="d37a3-104">\_Messaggio SETOUTLINECOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="d37a3-104">LVM\_SETOUTLINECOLOR message</span></span>

<span data-ttu-id="d37a3-105">Imposta il colore del bordo di un controllo di visualizzazione elenco se è impostato lo stile della finestra estesa [**LVS \_ ex \_ BORDERSELECT**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="d37a3-105">Sets the color of the border of a list-view control if the [**LVS\_EX\_BORDERSELECT**](extended-list-view-styles.md) extended window style is set.</span></span>

## <a name="parameters"></a><span data-ttu-id="d37a3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d37a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d37a3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d37a3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="d37a3-108">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d37a3-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="d37a3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d37a3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d37a3-110">Struttura **COLORREF** che specifica il colore per l'impostazione del bordo.</span><span class="sxs-lookup"><span data-stu-id="d37a3-110">**COLORREF** structure that specifies the color to set the border.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d37a3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d37a3-111">Return value</span></span>

<span data-ttu-id="d37a3-112">Restituisce la struttura **COLORREF** che contiene il colore del contorno.</span><span class="sxs-lookup"><span data-stu-id="d37a3-112">Returns **COLORREF** structure that contains the outline color.</span></span>

## <a name="remarks"></a><span data-ttu-id="d37a3-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="d37a3-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d37a3-114">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="d37a3-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="d37a3-115">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d37a3-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d37a3-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d37a3-116">Requirements</span></span>



| <span data-ttu-id="d37a3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d37a3-117">Requirement</span></span> | <span data-ttu-id="d37a3-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d37a3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d37a3-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d37a3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d37a3-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d37a3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d37a3-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d37a3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d37a3-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d37a3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d37a3-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d37a3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d37a3-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d37a3-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





