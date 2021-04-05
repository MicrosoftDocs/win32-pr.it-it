---
description: Oggetto di elaborazione dati utilizzato dall'interfaccia ID3DX10ThreadPump per l'elaborazione asincrona dei dati caricati.
ms.assetid: c932f558-10da-45fc-a833-8ed86fa065ab
title: Interfaccia ID3DX10DataProcessor (D3DX10. h)
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
ms.openlocfilehash: de573e50a1442396df78dd6a3c8f0bd09c1cbf6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886334"
---
# <a name="id3dx10dataprocessor-interface"></a>Interfaccia ID3DX10DataProcessor

Oggetto di elaborazione dati utilizzato dall' [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per l'elaborazione asincrona dei dati caricati.

## <a name="members"></a>Membri

L'interfaccia **ID3DX10DataProcessor** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10DataProcessor** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX10DataProcessor** dispone di questi metodi.



| Metodo                                                                | Descrizione                                                                                                                         |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDeviceObject**](id3dx10dataprocessor-createdeviceobject.md) | Creare un oggetto dispositivo.<br/>                                                                                                  |
| [**Eliminare**](id3dx10dataprocessor-destroy.md)                       | Usato da un' [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per eliminare il processore dopo il completamento di un elemento di lavoro.<br/> |
| [**Processo**](id3dx10dataprocessor-process.md)                       | Elaborare alcuni dati.<br/>                                                                                                       |



 

## <a name="remarks"></a>Commenti

Questo oggetto può essere ereditato e i relativi membri ridefiniti. Questa operazione consente di personalizzare l'API per l'elaborazione di formati di file personalizzati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
