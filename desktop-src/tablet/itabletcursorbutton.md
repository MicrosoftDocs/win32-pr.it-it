---
description: Rappresenta informazioni generali su un pulsante in un dispositivo stilo.
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
ms.openlocfilehash: 76f5e581a4db81d9e260b388cc129d915121a69f3b360441e4220fd58aa0e623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938601"
---
# <a name="itabletcursorbutton-interface"></a>Interfaccia ITabletCursorButton

Rappresenta informazioni generali su un pulsante in un dispositivo stilo.

## <a name="members"></a>Membri

**L'interfaccia ITabletCursorButton** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITabletCursorButton** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **ITabletCursorButton.**



| Metodo                                         | Descrizione                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [**GetGuid**](itabletcursorbutton-getguid.md) | Recupera l'identificatore univoco del pulsante dello stilo.<br/> |
| [**GetName**](itabletcursorbutton-getname.md) | Recupera il nome del pulsante dello stilo.<br/>              |



 

## <a name="remarks"></a>Commenti

Gli sviluppatori non devono usare questa interfaccia.

Il codice seguente illustra come viene **definita l'interfaccia ITabletCursorButton.**

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

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITabletCursorButton**](itabletcursorbutton.md)
</dt> </dl>

 

