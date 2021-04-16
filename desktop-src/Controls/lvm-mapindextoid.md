---
title: Messaggio LVM_MAPINDEXTOID (COMmctrl. h)
description: Esegue il mapping dell'indice di un elemento a un ID univoco.
ms.assetid: d0486e21-2703-4289-abb0-f5f9c7b60b40
keywords:
- Controlli di Windows Message LVM_MAPINDEXTOID
topic_type:
- apiref
api_name:
- LVM_MAPINDEXTOID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a2a5de558b025e61bef26fd20278f125372769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476090"
---
# <a name="lvm_mapindextoid-message"></a><span data-ttu-id="5527e-104">\_Messaggio MAPINDEXTOID LVM</span><span class="sxs-lookup"><span data-stu-id="5527e-104">LVM\_MAPINDEXTOID message</span></span>

<span data-ttu-id="5527e-105">Esegue il mapping dell'indice di un elemento a un ID univoco.</span><span class="sxs-lookup"><span data-stu-id="5527e-105">Maps the index of an item to a unique ID.</span></span>

## <a name="parameters"></a><span data-ttu-id="5527e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5527e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5527e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5527e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5527e-108">Indice di un elemento.</span><span class="sxs-lookup"><span data-stu-id="5527e-108">The index of an item.</span></span>

</dd> <dt>

<span data-ttu-id="5527e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5527e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5527e-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="5527e-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5527e-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5527e-111">Return value</span></span>

<span data-ttu-id="5527e-112">Restituisce un ID univoco.</span><span class="sxs-lookup"><span data-stu-id="5527e-112">Returns a unique ID.</span></span>

## <a name="remarks"></a><span data-ttu-id="5527e-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="5527e-113">Remarks</span></span>

<span data-ttu-id="5527e-114">I controlli di visualizzazione elenco internamente rilevano gli elementi in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="5527e-114">List-view controls internally track items by index.</span></span> <span data-ttu-id="5527e-115">Questo può presentare problemi perché gli indici possono cambiare durante la durata del controllo.</span><span class="sxs-lookup"><span data-stu-id="5527e-115">This can present problems because indexes can change during the control's lifetime.</span></span>

<span data-ttu-id="5527e-116">Il controllo elenco-visualizzazione consente di contrassegnare un elemento con un ID quando viene creato l'elemento.</span><span class="sxs-lookup"><span data-stu-id="5527e-116">The list-view control can tag an item with an ID when the item is created.</span></span> <span data-ttu-id="5527e-117">È possibile usare questo ID per garantire l'univocità durante il ciclo di vita del controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="5527e-117">You can use this ID to guarantee uniqueness during the lifetime of the list-view control.</span></span>

<span data-ttu-id="5527e-118">Per identificare in modo univoco un elemento, prendere l'indice restituito da una chiamata, ad esempio [**IComponent:: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) e chiamare **LVM \_ MAPINDEXTOID**.</span><span class="sxs-lookup"><span data-stu-id="5527e-118">To uniquely identify an item, take the index that is returned from a call such as [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) and call **LVM\_MAPINDEXTOID**.</span></span> <span data-ttu-id="5527e-119">Il valore restituito è un ID univoco.</span><span class="sxs-lookup"><span data-stu-id="5527e-119">The return value is a unique ID.</span></span>

> [!Note]  
> <span data-ttu-id="5527e-120">In un ambiente con multithreading, l'indice è garantito solo nel thread che ospita il controllo visualizzazione elenco, non nei thread in background.</span><span class="sxs-lookup"><span data-stu-id="5527e-120">In a multithreaded environment, the index is only guaranteed on the thread that hosts the list-view control, not on background threads.</span></span>

 

> [!Note]  
> <span data-ttu-id="5527e-121">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="5527e-121">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="5527e-122">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5527e-122">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5527e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5527e-123">Requirements</span></span>



| <span data-ttu-id="5527e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5527e-124">Requirement</span></span> | <span data-ttu-id="5527e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5527e-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5527e-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5527e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5527e-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5527e-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5527e-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5527e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5527e-129">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5527e-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5527e-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5527e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5527e-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5527e-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

