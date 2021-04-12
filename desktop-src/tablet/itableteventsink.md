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
# <a name="itableteventsink-interface"></a>Interfaccia ITabletEventSink

Definisce i metodi che gestiscono gli eventi dell' [**interfaccia ITablet**](itablet.md) .

## <a name="members"></a>Membri

L'interfaccia **ITabletEventSink** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletEventSink** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITabletEventSink** dispone di questi metodi.



| Metodo                                                        | Descrizione                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**ContextCreate**](itableteventsink-contextcreate.md)       | Si verifica quando viene creato un nuovo contesto del tablet.<br/>                                          |
| [**ContextDestroy**](itableteventsink-contextdestroy.md)     | Si verifica quando un contesto del Tablet viene eliminato definitivamente.<br/>                                      |
| [**CursorDown**](itableteventsink-cursordown.md)             | Si verifica quando la punta dello stilo contatta la superficie del Tablet di digitalizzazione.<br/>                    |
| [**CursorInRange**](itableteventsink-cursorinrange.md)       | Si verifica quando uno stilo rientra nell'intervallo di rilevamento del digitalizzatore.<br/>                 |
| [**CursorMove**](itableteventsink-cursormove.md)             | Si verifica quando il cursore viene spostato sul digitalizzatore del tablet.<br/>                               |
| [**CursorNew**](itableteventsink-cursornew.md)               | Si verifica quando un nuovo stilo viene aggiunto al sistema.<br/>                                      |
| [**CursorOutOfRange**](itableteventsink-cursoroutofrange.md) | Si verifica quando lo stilo lascia l'intervallo di rilevamento fisico (prossimità) del tablet.<br/> |
| [**CursorUp**](itableteventsink-cursorup.md)                 | Si verifica quando l'utente ha generato lo stilo dalla superficie del digitalizzatore del Tablet PC.<br/>         |
| [**Pacchetti**](itableteventsink-packets.md)                   | Si verifica quando lo stilo viene spostato sul digitalizzatore.<br/>                                    |
| [**SystemEvent**](itableteventsink-systemevent.md)           | Si verifica quando è disponibile un evento di sistema.<br/>                                              |



 

## <a name="remarks"></a>Commenti

Gli sviluppatori non devono utilizzare questa interfaccia.

Il codice seguente illustra come viene definita l'interfaccia **ITabletEventSink** .

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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

