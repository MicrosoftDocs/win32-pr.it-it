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
# <a name="itabletcursorbutton-interface"></a>Interfaccia ITabletCursorButton

Rappresenta le informazioni generali su un pulsante in un dispositivo stilo.

## <a name="members"></a>Membri

L'interfaccia **ITabletCursorButton** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITabletCursorButton** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITabletCursorButton** dispone di questi metodi.



| Metodo                                         | Descrizione                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [**GetGuid**](itabletcursorbutton-getguid.md) | Recupera l'identificatore univoco del pulsante dello stilo.<br/> |
| [**GetName**](itabletcursorbutton-getname.md) | Recupera il nome del pulsante dello stilo.<br/>              |



 

## <a name="remarks"></a>Commenti

Gli sviluppatori non devono utilizzare questa interfaccia.

Il codice seguente illustra come viene definita l'interfaccia **ITabletCursorButton** .

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
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITabletCursorButton**](itabletcursorbutton.md)
</dt> </dl>

 

