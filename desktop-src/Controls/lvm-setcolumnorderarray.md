---
title: Messaggio LVM_SETCOLUMNORDERARRAY (COMmctrl. h)
description: Imposta l'ordine da sinistra a destra delle colonne in un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usare la \_ macro SetColumnOrderArray di ListView.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- Controlli di Windows Message LVM_SETCOLUMNORDERARRAY
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fdeb27074a3f6762e7fb3788fd7ccc0a2dcc5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047855"
---
# <a name="lvm_setcolumnorderarray-message"></a><span data-ttu-id="af60e-105">\_Messaggio SETCOLUMNORDERARRAY LVM</span><span class="sxs-lookup"><span data-stu-id="af60e-105">LVM\_SETCOLUMNORDERARRAY message</span></span>

<span data-ttu-id="af60e-106">Imposta l'ordine da sinistra a destra delle colonne in un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="af60e-106">Sets the left-to-right order of columns in a list-view control.</span></span> <span data-ttu-id="af60e-107">È possibile inviare questo messaggio in modo esplicito o usare la macro [**\_ SetColumnOrderArray di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) .</span><span class="sxs-lookup"><span data-stu-id="af60e-107">You can send this message explicitly or use the [**ListView\_SetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="af60e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="af60e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af60e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="af60e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af60e-110">Dimensioni, in elementi, del buffer in *lParam*.</span><span class="sxs-lookup"><span data-stu-id="af60e-110">Size, in elements, of the buffer at *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="af60e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="af60e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="af60e-112">Puntatore a una matrice che specifica l'ordine in cui devono essere visualizzate le colonne, da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="af60e-112">Pointer to an array that specifies the order in which columns should be displayed, from left to right.</span></span> <span data-ttu-id="af60e-113">Se, ad esempio, il contenuto della matrice è {2,0,1} , il controllo Visualizza la colonna 2, la colonna 0 e la colonna 1 in tale ordine.</span><span class="sxs-lookup"><span data-stu-id="af60e-113">For example, if the contents of the array are {2,0,1}, the control displays column 2, column 0, and column 1 in that order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af60e-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af60e-114">Return value</span></span>

<span data-ttu-id="af60e-115">Restituisce un valore diverso da zero se ha esito positivo oppure zero in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="af60e-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="af60e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af60e-116">Requirements</span></span>



| <span data-ttu-id="af60e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="af60e-117">Requirement</span></span> | <span data-ttu-id="af60e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="af60e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af60e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af60e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="af60e-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af60e-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="af60e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="af60e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="af60e-122">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="af60e-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="af60e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af60e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="af60e-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="af60e-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





