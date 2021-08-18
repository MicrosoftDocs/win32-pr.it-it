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
ms.openlocfilehash: a1a773f7b4e08a718c419de2d51c0ff3bd9bba551267188b12889b9ec99d4ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716460"
---
# <a name="itableteventsink-interface"></a>Interfaccia ITabletEventSink

Definisce i metodi che gestiscono gli [**eventi dell'interfaccia ITablet.**](itablet.md)

## <a name="members"></a>Membri

**L'interfaccia ITabletEventSink** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITabletEventSink** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITabletEventSink** include questi metodi.



| Metodo                                                        | Descrizione                                                                                      |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**ContextCreate**](itableteventsink-contextcreate.md)       | Si verifica quando viene creato un nuovo contesto di tablet.<br/>                                          |
| [**ContextDestroy**](itableteventsink-contextdestroy.md)     | Si verifica quando un contesto di tablet viene eliminato.<br/>                                      |
| [**CursorDown**](itableteventsink-cursordown.md)             | Si verifica quando la punta dello stilo contatta la superficie del tablet di digitalizzazione.<br/>                    |
| [**Cursorinrange**](itableteventsink-cursorinrange.md)       | Si verifica quando uno stilo rientra nell'intervallo di rilevamento del digitalizzatore.<br/>                 |
| [**CursorMove**](itableteventsink-cursormove.md)             | Si verifica quando il cursore viene spostato sul digitalizzatore tablet.<br/>                               |
| [**CursorNew**](itableteventsink-cursornew.md)               | Si verifica quando viene aggiunto un nuovo stilo al sistema.<br/>                                      |
| [**CursorOutOfRange**](itableteventsink-cursoroutofrange.md) | Si verifica quando lo stilo esce dall'intervallo di rilevamento fisico (prossimità) della tablet.<br/> |
| [**CursorUp**](itableteventsink-cursorup.md)                 | Si verifica quando l'utente ha generato lo stilo dalla superficie del digitalizzatore tablet.<br/>         |
| [**Pacchetti**](itableteventsink-packets.md)                   | Si verifica quando lo stilo si sposta sul digitalizzatore.<br/>                                    |
| [**SystemEvent**](itableteventsink-systemevent.md)           | Si verifica quando è disponibile un evento di sistema.<br/>                                              |



 

## <a name="remarks"></a>Commenti

Gli sviluppatori non devono usare questa interfaccia.

Il codice seguente illustra come viene definita **l'interfaccia ITabletEventSink.**

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
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

