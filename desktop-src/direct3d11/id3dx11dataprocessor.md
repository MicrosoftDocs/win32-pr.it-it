---
title: Interfaccia ID3DX11DataProcessor (D3DX11core.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Oggetto di elaborazione dati usato dall'interfaccia ID3DX11ThreadPump per il caricamento asincrono dei dati.
ms.assetid: ab893879-416f-4b17-9035-a7f03a62b753
keywords:
- Interfaccia ID3DX11DataProcessor Direct3D 11
- INTERFACCIA ID3DX11DataProcessor Direct3D 11 , descritta
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 808c7d1bf1bdef1223e5b57e40ea5e6a90878101
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469348"
---
# <a name="id3dx11dataprocessor-interface"></a>Interfaccia ID3DX11DataProcessor

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Oggetto di elaborazione dati usato [**dall'interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md) per il caricamento asincrono dei dati.

## <a name="members"></a>Membri

**L'interfaccia ID3DX11DataProcessor** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11DataProcessor** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX11DataProcessor** include questi metodi.




| Metodo | Descrizione | 
|--------|-------------|
| <a href="id3dx11dataprocessor-createdeviceobject.md"><strong>CreateDeviceObject</strong></a> | <blockquote>[!Note]<br />La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</blockquote><br /> Crea un oggetto dispositivo.<br /> | 
| <a href="id3dx11dataprocessor-destroy.md"><strong>Distruggere</strong></a> | <blockquote>[!Note]<br />La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</blockquote><br /> Elimina il processore dopo il completamento di un elemento di lavoro.<br /> | 
| <a href="id3dx11dataprocessor-process.md"><strong>Processo</strong></a> | <blockquote>[!Note]<br />La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</blockquote><br /> Elabora i dati.<br /> | 




 

## <a name="remarks"></a>Commenti

Questo oggetto può essere ereditato e i relativi membri vengono ridefiniti per l'elaborazione di formati di file personalizzati.

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>D3DX11core.h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

