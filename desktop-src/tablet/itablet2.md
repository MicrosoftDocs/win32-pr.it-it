---
description: Estende l'interfaccia ITablet.
ms.assetid: dd4f3b2e-7f63-4d5b-b50e-64458719c17a
title: Interfaccia ITablet2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 0df1114f5808e5fd08a1a2dbe00ccfb451eaa7096c978d3f4d454e508c0a2fcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118717350"
---
# <a name="itablet2-interface"></a>Interfaccia ITablet2

Estende [**l'interfaccia ITablet**](itablet.md).

## <a name="members"></a>Membri

**L'interfaccia ITablet2** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITablet2** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITablet2** include questi metodi.



| Metodo                                          | Descrizione                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**GetDeviceKind**](itablet2-getdevicekind.md) | Restituisce il tipo di dispositivo hardware rappresentato dall'oggetto tablet, ad esempio mouse, penna o tocco.<br/> |



 

## <a name="remarks"></a>Commenti

Questa interfaccia è stata introdotta in Windows Vista.

Gli sviluppatori non devono usare questa interfaccia.

Il codice seguente descrive come viene definita **l'interfaccia ITablet2.**

``` syntax
[
    object,
    uuid(C247F616-BBEB-406A-AED3-F75E656599AE),
    pointer_default(unique)
]
interface ITablet2 : IUnknown
{
    HRESULT GetDeviceKind([out] TABLET_DEVICE_KIND *pKind);

    HRESULT GetMatchingScreenRect([out] RECT *prcInput);
};
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

