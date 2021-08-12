---
description: L'interfaccia ITablet3 consente l'esecuzione di query multitouch per l'input.
ms.assetid: 949f2d83-7761-4d60-b8fe-5a9ac7567238
title: Interfaccia ITablet3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: b774ab5626d1eab5d8f4179b27924686fed56661fb776039a65ff40b3b64ebba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449844"
---
# <a name="itablet3-interface"></a>Interfaccia ITablet3

L'interfaccia ITablet3 consente l'esecuzione di query multitouch per l'input.

## <a name="members"></a>Membri

**L'interfaccia ITablet3** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITablet3** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITablet3** include questi metodi.



| Metodo                                                  | Descrizione                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetMaximumCursors**](itablet3-getmaximumcursors.md) | Recupera il numero massimo di input supportati.<br/>        |
| [**isMultiTouch**](itablet3-ismultitouch.md)           | Indica se multitouch è abilitato per questo oggetto.<br/> |



 

## <a name="remarks"></a>Commenti

Gli sviluppatori non devono usare questa interfaccia

Nel codice seguente viene descritto come viene **definita l'interfaccia ITablet3.**

``` syntax
[
  object,
  uuid(AC0E3951-0A2F-448E-88D0-49DA0C453460)
  pointer_default(unique)
]
interface ITablet3 : IUnknown
{
    HRESULT IsMultiTouch([out] BOOL *pIsMultiTouch);

    HRESULT GetMaximumCursors([out] ULONG *pMaximumCursors);
};
  
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

