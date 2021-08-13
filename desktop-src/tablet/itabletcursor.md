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
ms.openlocfilehash: 83a24329b318ec2bb542a3bbb63a28d4db9fce877b99f75aa7091670825fa439
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716939"
---
# <a name="itabletcursor-interface"></a>Interfaccia ITabletCursor

Rappresenta un oggetto stilo.

## <a name="members"></a>Membri

**L'interfaccia ITabletCursor** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITabletCursor** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **ITabletCursor.**



| Metodo                                                 | Descrizione                                                            |
|:-------------------------------------------------------|:-----------------------------------------------------------------------|
| [**GetButton**](itabletcursor-getbutton.md)           | Recupera l'oggetto pulsante specificato da uno stilo del tablet.<br/> |
| [**GetButtonCount**](itabletcursor-getbuttoncount.md) | Recupera il numero di pulsanti sullo stilo del tablet.<br/>       |
| [**GetId**](itabletcursor-getid.md)                   | Recupera l'identificatore dello stilo.<br/>                            |
| [**GetName**](itabletcursor-getname.md)               | Recupera il nome dello stilo del tablet.<br/>                    |
| [**IsInverted**](itabletcursor-isinverted.md)         | Indica se lo stilo è capovolto.<br/>                     |



 

## <a name="remarks"></a>Commenti

Non usare questa interfaccia.

Il codice seguente descrive come viene definita **l'interfaccia ITabletCursor.**

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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

