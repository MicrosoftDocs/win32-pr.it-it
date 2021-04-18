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
ms.openlocfilehash: b402695aa278105ad57209f3ff33e66ccaf8c746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316826"
---
# <a name="itablet2-interface"></a>Interfaccia ITablet2

Estende l' [**interfaccia ITablet**](itablet.md).

## <a name="members"></a>Membri

L'interfaccia **ITablet2** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITablet2** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITablet2** dispone di questi metodi.



| Metodo                                          | Descrizione                                                                                              |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**GetDeviceKind**](itablet2-getdevicekind.md) | Restituisce il tipo di dispositivo hardware rappresentato dall'oggetto Tablet, ad esempio il mouse, la penna o il tocco.<br/> |



 

## <a name="remarks"></a>Commenti

Questa interfaccia è stata introdotta in Windows Vista.

Gli sviluppatori non devono utilizzare questa interfaccia.

Il codice seguente descrive il modo in cui viene definita l'interfaccia **ITablet2** .

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                         |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

