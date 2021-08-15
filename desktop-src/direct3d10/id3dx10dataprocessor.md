---
description: Oggetto di elaborazione dati usato dall'interfaccia ID3DX10ThreadPump per l'elaborazione asincrona dei dati caricati.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: Interfaccia ID3DX10DataProcessor (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ddb192a0591ce241e216b3bd0471212fc4801fbf1c901430c187f5370237049d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128371"
---
# <a name="id3dx10dataprocessor-interface"></a>Interfaccia ID3DX10DataProcessor

Oggetto di elaborazione dati usato [**dall'interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per l'elaborazione asincrona dei dati caricati.

## <a name="members"></a>Membri

**L'interfaccia ID3DX10DataProcessor** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10DataProcessor** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX10DataProcessor** include questi metodi.



| Metodo                                                                | Descrizione                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDeviceObject**](id3dx10dataprocessor-createdeviceobject.md) | Creare un oggetto dispositivo.<br/>                                                                                                  |
| [**Distruggere**](id3dx10dataprocessor-destroy.md)                       | Usato da [**un'interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per eliminare il processore dopo il completamento di un elemento di lavoro.<br/> |
| [**Processo**](id3dx10dataprocessor-process.md)                       | Elaborare alcuni dati.<br/>                                                                                                       |



 

## <a name="remarks"></a>Commenti

Questo oggetto può essere ereditato e i relativi membri possono essere ridefiniti. In questo modo è possibile personalizzare l'API per l'elaborazione di formati di file personalizzati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
