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
ms.openlocfilehash: f37d70888ccedf0fe941f0387c064aba37dc287e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317929"
---
# <a name="itablet3-interface"></a>Interfaccia ITablet3

L'interfaccia ITablet3 consente l'esecuzione di query multitouch per l'input.

## <a name="members"></a>Membri

L'interfaccia **ITablet3** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITablet3** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITablet3** dispone di questi metodi.



| Metodo                                                  | Descrizione                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetMaximumCursors**](itablet3-getmaximumcursors.md) | Recupera il numero massimo di input supportati.<br/>        |
| [**MultiTouch**](itablet3-ismultitouch.md)           | Indica se il multitouch è abilitato per questo oggetto.<br/> |



 

## <a name="remarks"></a>Commenti

Gli sviluppatori non devono usare questa interfaccia

Il codice seguente descrive il modo in cui viene definita l'interfaccia **ITablet3** .

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                |
| Libreria<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



 

