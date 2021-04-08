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
# <a name="itabletmanager-interface"></a>Interfaccia ITabletManager

Consente di accedere a tutti i tablet collegati al computer.

## <a name="members"></a>Membri

L'interfaccia **ITabletManager** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletManager** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITabletManager** dispone di questi metodi.



| Metodo                                                  | Descrizione                                                        |
|:--------------------------------------------------------|:-------------------------------------------------------------------|
| [**Gettablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85))           | Recupera l'oggetto Tablet specificato.<br/>                  |
| [**GetTabletCount**](itabletmanager-gettabletcount.md) | Recupera il numero di tablet collegato al sistema.<br/> |



 

## <a name="remarks"></a>Commenti

Gli sviluppatori non devono utilizzare questa interfaccia.

Il codice seguente illustra come viene implementata l'interfaccia **ITabletManager** .

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

Chiamare [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con un ID di classe CLSID \_ TabletManagerS, quindi chiamare [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere un puntatore all' **interfaccia ITabletManager**. Il \_ GUID TABLETMANAGERS CLSID viene definito come segue:

``` syntax
#define CLSID_TabletManagerS uuid(A5B020FD-E04B-4e67-B65A-E7DEED25B2CF)
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

