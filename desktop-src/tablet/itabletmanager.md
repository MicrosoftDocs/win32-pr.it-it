---
description: Consente di accedere a tutti i tablet collegati al computer.
ms.assetid: d0fd9a6f-93fe-43d6-97fd-fee45854dfa1
title: Interfaccia ITabletManager
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletManager
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 3400d98a832819d1edd640cd78586f1cfb06bdee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058286"
---
# <a name="itabletmanager-interface"></a><span data-ttu-id="3264f-103">Interfaccia ITabletManager</span><span class="sxs-lookup"><span data-stu-id="3264f-103">ITabletManager interface</span></span>

<span data-ttu-id="3264f-104">Consente di accedere a tutti i tablet collegati al computer.</span><span class="sxs-lookup"><span data-stu-id="3264f-104">Provides access to all of the tablets attached to the computer.</span></span>

## <a name="members"></a><span data-ttu-id="3264f-105">Membri</span><span class="sxs-lookup"><span data-stu-id="3264f-105">Members</span></span>

<span data-ttu-id="3264f-106">L'interfaccia **ITabletManager** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3264f-106">The **ITabletManager** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3264f-107">**ITabletManager** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3264f-107">**ITabletManager** also has these types of members:</span></span>

-   [<span data-ttu-id="3264f-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="3264f-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3264f-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="3264f-109">Methods</span></span>

<span data-ttu-id="3264f-110">L'interfaccia **ITabletManager** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3264f-110">The **ITabletManager** interface has these methods.</span></span>



| <span data-ttu-id="3264f-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="3264f-111">Method</span></span>                                                  | <span data-ttu-id="3264f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3264f-112">Description</span></span>                                                        |
|:--------------------------------------------------------|:-------------------------------------------------------------------|
| <span data-ttu-id="3264f-113">[**Gettablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3264f-113">[**GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))</span></span>           | <span data-ttu-id="3264f-114">Recupera l'oggetto Tablet specificato.</span><span class="sxs-lookup"><span data-stu-id="3264f-114">Retrieves the specified tablet object.</span></span><br/>                  |
| [<span data-ttu-id="3264f-115">**GetTabletCount**</span><span class="sxs-lookup"><span data-stu-id="3264f-115">**GetTabletCount**</span></span>](itabletmanager-gettabletcount.md) | <span data-ttu-id="3264f-116">Recupera il numero di tablet collegato al sistema.</span><span class="sxs-lookup"><span data-stu-id="3264f-116">Retrieves the number of tablets attached to the system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3264f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="3264f-117">Remarks</span></span>

<span data-ttu-id="3264f-118">Gli sviluppatori non devono utilizzare questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="3264f-118">Developers should not use this interface.</span></span>

<span data-ttu-id="3264f-119">Il codice seguente illustra come viene implementata l'interfaccia **ITabletManager** .</span><span class="sxs-lookup"><span data-stu-id="3264f-119">The following code shows how the **ITabletManager** interface is implemented.</span></span>

``` syntax
[
    object,
    uuid(764DE8AA-1867-47C1-8F6A-122445ABD89A),
    pointer_default(unique)
]
interface ITabletManager : IUnknown
{
    HRESULT GetDefaultTablet(
        [out] ITablet **ppTablet);

    HRESULT GetTabletCount(
        [out] ULONG *pcTablets);

    HRESULT GetTablet(
        [in] ULONG iTablet,
        [out] ITablet **ppTablet);

    HRESULT GetTabletContextById(
        [in] TABLET_CONTEXT_ID tcid,
        [out] ITabletContext **ppContext);

    HRESULT GetCursorById(
        [in] CURSOR_ID cid,
        [out] ITabletCursor **ppCursor);
};
        
        
```

<span data-ttu-id="3264f-120">Chiamare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con un ID di classe CLSID \_ TabletManagerS, quindi chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere un puntatore all' **interfaccia ITabletManager**.</span><span class="sxs-lookup"><span data-stu-id="3264f-120">Call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with a class ID of CLSID\_TabletManagerS, and then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get a pointer to the **ITabletManager Interface**.</span></span> <span data-ttu-id="3264f-121">Il \_ GUID TABLETMANAGERS CLSID viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="3264f-121">The CLSID\_TabletManagerS GUID is defined as follows:</span></span>

``` syntax
#define CLSID_TabletManagerS uuid(A5B020FD-E04B-4e67-B65A-E7DEED25B2CF)
```

## <a name="requirements"></a><span data-ttu-id="3264f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3264f-122">Requirements</span></span>



| <span data-ttu-id="3264f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3264f-123">Requirement</span></span> | <span data-ttu-id="3264f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3264f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3264f-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3264f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3264f-126">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3264f-126">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3264f-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3264f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3264f-128">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3264f-128">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3264f-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="3264f-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="3264f-130"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3264f-130"><dt>Wisptis.exe</dt></span></span> </dl> |



 

