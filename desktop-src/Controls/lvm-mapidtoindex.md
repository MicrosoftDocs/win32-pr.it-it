---
title: Messaggio LVM_MAPIDTOINDEX (COMmctrl. h)
description: Esegue il mapping dell'ID di un elemento a un indice.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- Controlli di Windows Message LVM_MAPIDTOINDEX
topic_type:
- apiref
api_name:
- LVM_MAPIDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb4cb8aa49b37186ef689ed8cb319bbb92b62d75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302204"
---
# <a name="lvm_mapidtoindex-message"></a><span data-ttu-id="fae98-104">\_Messaggio MAPIDTOINDEX LVM</span><span class="sxs-lookup"><span data-stu-id="fae98-104">LVM\_MAPIDTOINDEX message</span></span>

<span data-ttu-id="fae98-105">Esegue il mapping dell'ID di un elemento a un indice.</span><span class="sxs-lookup"><span data-stu-id="fae98-105">Maps the ID of an item to an index.</span></span>

## <a name="parameters"></a><span data-ttu-id="fae98-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fae98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fae98-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fae98-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fae98-108">ID univoco di un elemento.</span><span class="sxs-lookup"><span data-stu-id="fae98-108">The unique ID of an item.</span></span>

</dd> <dt>

<span data-ttu-id="fae98-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fae98-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fae98-110">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="fae98-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fae98-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fae98-111">Return value</span></span>

<span data-ttu-id="fae98-112">Restituisce l'indice più recente.</span><span class="sxs-lookup"><span data-stu-id="fae98-112">Returns the most current index.</span></span>

## <a name="remarks"></a><span data-ttu-id="fae98-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="fae98-113">Remarks</span></span>

<span data-ttu-id="fae98-114">I controlli di visualizzazione elenco internamente rilevano gli elementi in base all'indice.</span><span class="sxs-lookup"><span data-stu-id="fae98-114">List-view controls internally track items by index.</span></span> <span data-ttu-id="fae98-115">Questo può presentare problemi perché gli indici possono cambiare durante la durata del controllo.</span><span class="sxs-lookup"><span data-stu-id="fae98-115">This can present problems because indexes can change during the control's lifetime.</span></span>

<span data-ttu-id="fae98-116">Il controllo elenco-visualizzazione consente di contrassegnare un elemento con un ID quando viene creato l'elemento.</span><span class="sxs-lookup"><span data-stu-id="fae98-116">The list-view control can tag an item with an ID when the item is created.</span></span> <span data-ttu-id="fae98-117">È possibile usare questo ID per garantire l'univocità durante il ciclo di vita del controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="fae98-117">You can use this ID to guarantee uniqueness during the lifetime of the list-view control.</span></span>

<span data-ttu-id="fae98-118">Per identificare in modo univoco un elemento, prendere l'indice restituito da una chiamata, ad esempio [**IComponent:: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) e chiamare [**LVM \_ MAPINDEXTOID**](lvm-mapindextoid.md).</span><span class="sxs-lookup"><span data-stu-id="fae98-118">To uniquely identify an item, take the index that is returned from a call such as [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) and call [**LVM\_MAPINDEXTOID**](lvm-mapindextoid.md).</span></span> <span data-ttu-id="fae98-119">Il valore restituito è un ID univoco.</span><span class="sxs-lookup"><span data-stu-id="fae98-119">The return value is a unique ID.</span></span>

<span data-ttu-id="fae98-120">Se è necessario l'indice di un elemento dopo la creazione di un ID, è possibile chiamare **LVM \_ MAPIDTOINDEX** con l'ID univoco e viene restituito l'indice più recente.</span><span class="sxs-lookup"><span data-stu-id="fae98-120">If you need the index of an item after an ID is created you can call **LVM\_MAPIDTOINDEX** with the unique ID and it returns the most current index.</span></span>

<span data-ttu-id="fae98-121">**LVM \_ MAPIDTOINDEX** non è supportato nello stile [**\_ OWNERDATA di LVS**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="fae98-121">**LVM\_MAPIDTOINDEX** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="fae98-122">In un ambiente con multithreading, l'indice è garantito solo nel thread che ospita il controllo visualizzazione elenco, non nei thread in background.</span><span class="sxs-lookup"><span data-stu-id="fae98-122">In a multithreaded environment, the index is only guaranteed on the thread that hosts the list-view control, not on background threads.</span></span>

 

> [!Note]  
> <span data-ttu-id="fae98-123">Per utilizzare questo messaggio, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="fae98-123">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="fae98-124">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fae98-124">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fae98-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fae98-125">Requirements</span></span>



| <span data-ttu-id="fae98-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="fae98-126">Requirement</span></span> | <span data-ttu-id="fae98-127">Valore</span><span class="sxs-lookup"><span data-stu-id="fae98-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fae98-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fae98-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fae98-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fae98-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fae98-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fae98-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fae98-131">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fae98-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fae98-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fae98-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fae98-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fae98-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

