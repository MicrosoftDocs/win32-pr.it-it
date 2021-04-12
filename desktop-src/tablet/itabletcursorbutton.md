---
description: Rappresenta le informazioni generali su un pulsante in un dispositivo stilo.
ms.assetid: 20c9f8bb-8f8d-4469-baff-b9001c8adb3b
title: Interfaccia ITabletCursorButton
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c8f13e46699c1bea42bd8f8a7f78313aeba68aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346866"
---
# <a name="itabletcursorbutton-interface"></a><span data-ttu-id="6e9b3-103">Interfaccia ITabletCursorButton</span><span class="sxs-lookup"><span data-stu-id="6e9b3-103">ITabletCursorButton interface</span></span>

<span data-ttu-id="6e9b3-104">Rappresenta le informazioni generali su un pulsante in un dispositivo stilo.</span><span class="sxs-lookup"><span data-stu-id="6e9b3-104">Represents general information about a button on a stylus device.</span></span>

## <a name="members"></a><span data-ttu-id="6e9b3-105">Membri</span><span class="sxs-lookup"><span data-stu-id="6e9b3-105">Members</span></span>

<span data-ttu-id="6e9b3-106">L'interfaccia **ITabletCursorButton** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6e9b3-106">The **ITabletCursorButton** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6e9b3-107">**ITabletCursorButton** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6e9b3-107">**ITabletCursorButton** also has these types of members:</span></span>

-   [<span data-ttu-id="6e9b3-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="6e9b3-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6e9b3-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="6e9b3-109">Methods</span></span>

<span data-ttu-id="6e9b3-110">L'interfaccia **ITabletCursorButton** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6e9b3-110">The **ITabletCursorButton** interface has these methods.</span></span>



| <span data-ttu-id="6e9b3-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="6e9b3-111">Method</span></span>                                         | <span data-ttu-id="6e9b3-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e9b3-112">Description</span></span>                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="6e9b3-113">**GetGuid**</span><span class="sxs-lookup"><span data-stu-id="6e9b3-113">**GetGuid**</span></span>](itabletcursorbutton-getguid.md) | <span data-ttu-id="6e9b3-114">Recupera l'identificatore univoco del pulsante dello stilo.</span><span class="sxs-lookup"><span data-stu-id="6e9b3-114">Retrieves the unique identifier of the stylus button.</span></span><br/> |
| [<span data-ttu-id="6e9b3-115">**GetName**</span><span class="sxs-lookup"><span data-stu-id="6e9b3-115">**GetName**</span></span>](itabletcursorbutton-getname.md) | <span data-ttu-id="6e9b3-116">Recupera il nome del pulsante dello stilo.</span><span class="sxs-lookup"><span data-stu-id="6e9b3-116">Retrieves the name of the stylus button.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="6e9b3-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e9b3-117">Remarks</span></span>

<span data-ttu-id="6e9b3-118">Gli sviluppatori non devono utilizzare questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6e9b3-118">Developers should not use this interface.</span></span>

<span data-ttu-id="6e9b3-119">Il codice seguente illustra come viene definita l'interfaccia **ITabletCursorButton** .</span><span class="sxs-lookup"><span data-stu-id="6e9b3-119">The following code shows how the **ITabletCursorButton** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(997A992E-8B6C-4945-BC17-A1EE563B3AB7),
    pointer_default(unique)
]
interface ITabletCursorButton : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetGuid(
        [out] GUID *pguidBtn);
};
```

## <a name="requirements"></a><span data-ttu-id="6e9b3-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e9b3-120">Requirements</span></span>



| <span data-ttu-id="6e9b3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e9b3-121">Requirement</span></span> | <span data-ttu-id="6e9b3-122">Valore</span><span class="sxs-lookup"><span data-stu-id="6e9b3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e9b3-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e9b3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6e9b3-124">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="6e9b3-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6e9b3-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e9b3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6e9b3-126">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="6e9b3-126">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6e9b3-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="6e9b3-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e9b3-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6e9b3-128"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e9b3-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e9b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e9b3-130">**Interfaccia ITabletCursorButton**</span><span class="sxs-lookup"><span data-stu-id="6e9b3-130">**ITabletCursorButton Interface**</span></span>](itabletcursorbutton.md)
</dt> </dl>

 

