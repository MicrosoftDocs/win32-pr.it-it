---
description: Estende l'interfaccia ITablet.
ms.assetid: dd4f3b2e-7f63-4d5b-b50e-64458719c17a
title: Interfaccia ITablet2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b402695aa278105ad57209f3ff33e66ccaf8c746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316826"
---
# <a name="itablet2-interface"></a><span data-ttu-id="134ba-103">Interfaccia ITablet2</span><span class="sxs-lookup"><span data-stu-id="134ba-103">ITablet2 interface</span></span>

<span data-ttu-id="134ba-104">Estende l' [**interfaccia ITablet**](itablet.md).</span><span class="sxs-lookup"><span data-stu-id="134ba-104">Extends the [**ITablet Interface**](itablet.md).</span></span>

## <a name="members"></a><span data-ttu-id="134ba-105">Membri</span><span class="sxs-lookup"><span data-stu-id="134ba-105">Members</span></span>

<span data-ttu-id="134ba-106">L'interfaccia **ITablet2** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="134ba-106">The **ITablet2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="134ba-107">**ITablet2** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="134ba-107">**ITablet2** also has these types of members:</span></span>

-   [<span data-ttu-id="134ba-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="134ba-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="134ba-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="134ba-109">Methods</span></span>

<span data-ttu-id="134ba-110">L'interfaccia **ITablet2** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="134ba-110">The **ITablet2** interface has these methods.</span></span>



| <span data-ttu-id="134ba-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="134ba-111">Method</span></span>                                          | <span data-ttu-id="134ba-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="134ba-112">Description</span></span>                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="134ba-113">**GetDeviceKind**</span><span class="sxs-lookup"><span data-stu-id="134ba-113">**GetDeviceKind**</span></span>](itablet2-getdevicekind.md) | <span data-ttu-id="134ba-114">Restituisce il tipo di dispositivo hardware rappresentato dall'oggetto Tablet, ad esempio il mouse, la penna o il tocco.</span><span class="sxs-lookup"><span data-stu-id="134ba-114">Returns the type of hardware device the tablet object represents such as mouse, pen or touch.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="134ba-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="134ba-115">Remarks</span></span>

<span data-ttu-id="134ba-116">Questa interfaccia è stata introdotta in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="134ba-116">This interface was introduced in Windows Vista.</span></span>

<span data-ttu-id="134ba-117">Gli sviluppatori non devono utilizzare questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="134ba-117">Developers should not use this interface.</span></span>

<span data-ttu-id="134ba-118">Il codice seguente descrive il modo in cui viene definita l'interfaccia **ITablet2** .</span><span class="sxs-lookup"><span data-stu-id="134ba-118">The following code describes how the **ITablet2** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(C247F616-BBEB-406A-AED3-F75E656599AE),
    pointer_default(unique)
]
interface ITablet2 : IUnknown
{
    HRESULT GetDeviceKind([out] TABLET_DEVICE_KIND *pKind);

    HRESULT GetMatchingScreenRect([out] RECT *prcInput);
};
```

## <a name="requirements"></a><span data-ttu-id="134ba-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="134ba-119">Requirements</span></span>



| <span data-ttu-id="134ba-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="134ba-120">Requirement</span></span> | <span data-ttu-id="134ba-121">Valore</span><span class="sxs-lookup"><span data-stu-id="134ba-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="134ba-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="134ba-122">Minimum supported client</span></span><br/> | <span data-ttu-id="134ba-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="134ba-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="134ba-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="134ba-124">Minimum supported server</span></span><br/> | <span data-ttu-id="134ba-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="134ba-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="134ba-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="134ba-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="134ba-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="134ba-127"><dt>Wisptis.exe</dt></span></span> </dl> |



 

