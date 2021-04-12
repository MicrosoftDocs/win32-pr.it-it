---
description: Definisce i metodi che gestiscono gli eventi dell'interfaccia ITablet.
ms.assetid: 9acf32fa-b33f-4b9a-be73-804b7d5434e8
title: Interfaccia ITabletEventSink
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: fc42bfe8a6e69504c35d7926c4c5a8b688404897
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233871"
---
# <a name="itableteventsink-interface"></a><span data-ttu-id="3912c-103">Interfaccia ITabletEventSink</span><span class="sxs-lookup"><span data-stu-id="3912c-103">ITabletEventSink interface</span></span>

<span data-ttu-id="3912c-104">Definisce i metodi che gestiscono gli eventi dell' [**interfaccia ITablet**](itablet.md) .</span><span class="sxs-lookup"><span data-stu-id="3912c-104">Defines methods that handle the [**ITablet Interface**](itablet.md) events.</span></span>

## <a name="members"></a><span data-ttu-id="3912c-105">Membri</span><span class="sxs-lookup"><span data-stu-id="3912c-105">Members</span></span>

<span data-ttu-id="3912c-106">L'interfaccia **ITabletEventSink** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3912c-106">The **ITabletEventSink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3912c-107">**ITabletEventSink** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3912c-107">**ITabletEventSink** also has these types of members:</span></span>

-   [<span data-ttu-id="3912c-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="3912c-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3912c-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="3912c-109">Methods</span></span>

<span data-ttu-id="3912c-110">L'interfaccia **ITabletEventSink** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3912c-110">The **ITabletEventSink** interface has these methods.</span></span>



| <span data-ttu-id="3912c-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="3912c-111">Method</span></span>                                                        | <span data-ttu-id="3912c-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3912c-112">Description</span></span>                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3912c-113">**ContextCreate**</span><span class="sxs-lookup"><span data-stu-id="3912c-113">**ContextCreate**</span></span>](itableteventsink-contextcreate.md)       | <span data-ttu-id="3912c-114">Si verifica quando viene creato un nuovo contesto del tablet.</span><span class="sxs-lookup"><span data-stu-id="3912c-114">Occurs when a new tablet context is created.</span></span><br/>                                          |
| [<span data-ttu-id="3912c-115">**ContextDestroy**</span><span class="sxs-lookup"><span data-stu-id="3912c-115">**ContextDestroy**</span></span>](itableteventsink-contextdestroy.md)     | <span data-ttu-id="3912c-116">Si verifica quando un contesto del Tablet viene eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="3912c-116">Occurs when a tablet context is being destroyed.</span></span><br/>                                      |
| [<span data-ttu-id="3912c-117">**CursorDown**</span><span class="sxs-lookup"><span data-stu-id="3912c-117">**CursorDown**</span></span>](itableteventsink-cursordown.md)             | <span data-ttu-id="3912c-118">Si verifica quando la punta dello stilo contatta la superficie del Tablet di digitalizzazione.</span><span class="sxs-lookup"><span data-stu-id="3912c-118">Occurs when the stylus tip contacts the digitizing tablet surface.</span></span><br/>                    |
| [<span data-ttu-id="3912c-119">**CursorInRange**</span><span class="sxs-lookup"><span data-stu-id="3912c-119">**CursorInRange**</span></span>](itableteventsink-cursorinrange.md)       | <span data-ttu-id="3912c-120">Si verifica quando uno stilo rientra nell'intervallo di rilevamento del digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="3912c-120">Occurs when a stylus comes within the digitizer's range of detection.</span></span><br/>                 |
| [<span data-ttu-id="3912c-121">**CursorMove**</span><span class="sxs-lookup"><span data-stu-id="3912c-121">**CursorMove**</span></span>](itableteventsink-cursormove.md)             | <span data-ttu-id="3912c-122">Si verifica quando il cursore viene spostato sul digitalizzatore del tablet.</span><span class="sxs-lookup"><span data-stu-id="3912c-122">Occurs when the cursor moves over the tablet digitizer.</span></span><br/>                               |
| [<span data-ttu-id="3912c-123">**CursorNew**</span><span class="sxs-lookup"><span data-stu-id="3912c-123">**CursorNew**</span></span>](itableteventsink-cursornew.md)               | <span data-ttu-id="3912c-124">Si verifica quando un nuovo stilo viene aggiunto al sistema.</span><span class="sxs-lookup"><span data-stu-id="3912c-124">Occurs when a new stylus is added to the system.</span></span><br/>                                      |
| [<span data-ttu-id="3912c-125">**CursorOutOfRange**</span><span class="sxs-lookup"><span data-stu-id="3912c-125">**CursorOutOfRange**</span></span>](itableteventsink-cursoroutofrange.md) | <span data-ttu-id="3912c-126">Si verifica quando lo stilo lascia l'intervallo di rilevamento fisico (prossimità) del tablet.</span><span class="sxs-lookup"><span data-stu-id="3912c-126">Occurs when the stylus leaves the physical detection range (proximity) of the tablet.</span></span><br/> |
| [<span data-ttu-id="3912c-127">**CursorUp**</span><span class="sxs-lookup"><span data-stu-id="3912c-127">**CursorUp**</span></span>](itableteventsink-cursorup.md)                 | <span data-ttu-id="3912c-128">Si verifica quando l'utente ha generato lo stilo dalla superficie del digitalizzatore del Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="3912c-128">Occurs when the user has raised the stylus from the tablet digitizer surface.</span></span><br/>         |
| [<span data-ttu-id="3912c-129">**Pacchetti**</span><span class="sxs-lookup"><span data-stu-id="3912c-129">**Packets**</span></span>](itableteventsink-packets.md)                   | <span data-ttu-id="3912c-130">Si verifica quando lo stilo viene spostato sul digitalizzatore.</span><span class="sxs-lookup"><span data-stu-id="3912c-130">Occurs when the stylus is moving on the digitizer.</span></span><br/>                                    |
| [<span data-ttu-id="3912c-131">**SystemEvent**</span><span class="sxs-lookup"><span data-stu-id="3912c-131">**SystemEvent**</span></span>](itableteventsink-systemevent.md)           | <span data-ttu-id="3912c-132">Si verifica quando è disponibile un evento di sistema.</span><span class="sxs-lookup"><span data-stu-id="3912c-132">Occurs when a system event is available.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="3912c-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="3912c-133">Remarks</span></span>

<span data-ttu-id="3912c-134">Gli sviluppatori non devono utilizzare questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="3912c-134">Developers should not use this interface.</span></span>

<span data-ttu-id="3912c-135">Il codice seguente illustra come viene definita l'interfaccia **ITabletEventSink** .</span><span class="sxs-lookup"><span data-stu-id="3912c-135">The following code shows how the **ITabletEventSink** interface is defined.</span></span>

``` syntax
[
    object,
    uuid(788459C8-26C8-4666-BF57-04AD3A0A5EB5),
    pointer_default(unique)
]
interface ITabletEventSink: IUnknown
{

    HRESULT ContextCreate(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT ContextDestroy(
        [in] TABLET_CONTEXT_ID tcid
    );

    HRESULT CursorNew(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorInRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorOutOfRange(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid
    );

    HRESULT CursorDown(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT CursorUp(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] ULONG nSerialNumber,
        [in] ULONG cbPkt,
        [in, size_is(cbPkt)] BYTE *pbPkt
    );

    HRESULT Packets(
        [in] TABLET_CONTEXT_ID tcid,
        [in] ULONG cPkts,
        [in] ULONG cbPkts,
        [in, size_is(cbPkts)] BYTE * pbPkts,
        [in, unique, size_is(cPkts)
#ifndef NT_TARGET_XP
         ,disable_consistency_check
#endif
        ] ULONG *pnSerialNumbers,
        [in] CURSOR_ID cid
    );

    HRESULT SystemEvent(
        [in] TABLET_CONTEXT_ID tcid,
        [in] CURSOR_ID cid,
        [in] SYSTEM_EVENT event,
        [in] SYSTEM_EVENT_DATA eventdata
    );
};

     
```

## <a name="requirements"></a><span data-ttu-id="3912c-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3912c-136">Requirements</span></span>



| <span data-ttu-id="3912c-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3912c-137">Requirement</span></span> | <span data-ttu-id="3912c-138">Valore</span><span class="sxs-lookup"><span data-stu-id="3912c-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3912c-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3912c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3912c-140">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="3912c-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3912c-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3912c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3912c-142">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="3912c-142">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3912c-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="3912c-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="3912c-144"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3912c-144"><dt>Wisptis.exe</dt></span></span> </dl> |



 

