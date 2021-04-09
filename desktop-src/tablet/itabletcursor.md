---
description: Rappresenta un oggetto stilo.
ms.assetid: c55945b7-59df-49b5-b25f-fa96056889fc
title: Interfaccia ITabletCursor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursor
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: eecbebc7090fb57d3794f3d056c24fba61fa5c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885326"
---
# <a name="itabletcursor-interface"></a><span data-ttu-id="910b7-103">Interfaccia ITabletCursor</span><span class="sxs-lookup"><span data-stu-id="910b7-103">ITabletCursor interface</span></span>

<span data-ttu-id="910b7-104">Rappresenta un oggetto stilo.</span><span class="sxs-lookup"><span data-stu-id="910b7-104">Represents a stylus object.</span></span>

## <a name="members"></a><span data-ttu-id="910b7-105">Membri</span><span class="sxs-lookup"><span data-stu-id="910b7-105">Members</span></span>

<span data-ttu-id="910b7-106">L'interfaccia **ITabletCursor** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="910b7-106">The **ITabletCursor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="910b7-107">**ITabletCursor** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="910b7-107">**ITabletCursor** also has these types of members:</span></span>

-   [<span data-ttu-id="910b7-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="910b7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="910b7-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="910b7-109">Methods</span></span>

<span data-ttu-id="910b7-110">L'interfaccia **ITabletCursor** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="910b7-110">The **ITabletCursor** interface has these methods.</span></span>



| <span data-ttu-id="910b7-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="910b7-111">Method</span></span>                                                 | <span data-ttu-id="910b7-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="910b7-112">Description</span></span>                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="910b7-113">**GetButton**</span><span class="sxs-lookup"><span data-stu-id="910b7-113">**GetButton**</span></span>](itabletcursor-getbutton.md)           | <span data-ttu-id="910b7-114">Recupera l'oggetto pulsante specificato da uno stilo del tablet.</span><span class="sxs-lookup"><span data-stu-id="910b7-114">Retrieves the specified button object from a tablet stylus.</span></span><br/> |
| [<span data-ttu-id="910b7-115">**GetButtonCount**</span><span class="sxs-lookup"><span data-stu-id="910b7-115">**GetButtonCount**</span></span>](itabletcursor-getbuttoncount.md) | <span data-ttu-id="910b7-116">Recupera il numero di pulsanti sullo stilo del tablet.</span><span class="sxs-lookup"><span data-stu-id="910b7-116">Retrieves the number of buttons on the tablet stylus.</span></span><br/>       |
| [<span data-ttu-id="910b7-117">**GetId**</span><span class="sxs-lookup"><span data-stu-id="910b7-117">**GetId**</span></span>](itabletcursor-getid.md)                   | <span data-ttu-id="910b7-118">Recupera l'identificatore dello stilo.</span><span class="sxs-lookup"><span data-stu-id="910b7-118">Retrieves the stylus identifier.</span></span><br/>                            |
| [<span data-ttu-id="910b7-119">**GetName**</span><span class="sxs-lookup"><span data-stu-id="910b7-119">**GetName**</span></span>](itabletcursor-getname.md)               | <span data-ttu-id="910b7-120">Recupera il nome dello stilo del tablet.</span><span class="sxs-lookup"><span data-stu-id="910b7-120">Retrieves the name of the tablet stylus.</span></span><br/>                    |
| [<span data-ttu-id="910b7-121">**Invertito**</span><span class="sxs-lookup"><span data-stu-id="910b7-121">**IsInverted**</span></span>](itabletcursor-isinverted.md)         | <span data-ttu-id="910b7-122">Indica se lo stilo è capovolto.</span><span class="sxs-lookup"><span data-stu-id="910b7-122">Indicates if the stylus is upside down.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="910b7-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="910b7-123">Remarks</span></span>

<span data-ttu-id="910b7-124">Non usare questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="910b7-124">Do not use this interface.</span></span>

<span data-ttu-id="910b7-125">Il codice seguente descrive il modo in cui viene definita l'interfaccia **ITabletCursor** .</span><span class="sxs-lookup"><span data-stu-id="910b7-125">The following code describes how the **ITabletCursor** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(EF9953C6-B472-4B02-9D22-D0E247ADE0E8,
    pointer_default(unique)
]
interface ITabletCursor : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT IsInverted();

    HRESULT GetId(
        [out] CURSOR_ID *pCid);

    HRESULT GetTablet(
        [out] ITablet **ppTablet);

    HRESULT GetButtonCount(
        [out] ULONG *pcButtons);

    HRESULT GetButton(
        [in] ULONG iButton,
        [out] ITabletCursorButton **ppButton);
};

     
```

## <a name="requirements"></a><span data-ttu-id="910b7-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="910b7-126">Requirements</span></span>



| <span data-ttu-id="910b7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="910b7-127">Requirement</span></span> | <span data-ttu-id="910b7-128">Valore</span><span class="sxs-lookup"><span data-stu-id="910b7-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="910b7-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="910b7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="910b7-130">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="910b7-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="910b7-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="910b7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="910b7-132">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="910b7-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="910b7-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="910b7-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="910b7-134"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="910b7-134"><dt>Wisptis.exe</dt></span></span> </dl> |



 

