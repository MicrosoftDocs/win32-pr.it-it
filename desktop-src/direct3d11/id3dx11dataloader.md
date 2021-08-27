---
title: Interfaccia ID3DX11DataLoader (D3DX11core.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Oggetto di caricamento dati usato dall'interfaccia ID3DX11ThreadPump per il caricamento asincrono dei dati.
ms.assetid: 878929ea-0228-4650-9ca0-f83d60d9f915
keywords:
- Interfaccia ID3DX11DataLoader Direct3D 11
- INTERFACCIA ID3DX11DataLoader Direct3D 11 , descritta
topic_type:
- apiref
api_name:
- ID3DX11DataLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b688fcbeff21edf23f6a3be1b39be5a9cf0000
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471647"
---
# <a name="id3dx11dataloader-interface"></a>Interfaccia ID3DX11DataLoader

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Oggetto di caricamento dati usato [**dall'interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md) per il caricamento asincrono dei dati.

## <a name="members"></a>Membri

**L'interfaccia ID3DX11DataLoader** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ID3DX11DataLoader** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX11DataLoader** include questi metodi.




| Metodo | Descrizione | 
|--------|-------------|
| <a href="id3dx11dataloader-decompress.md"><strong>Decomprimere</strong></a> | <blockquote>[!Note]<br />La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</blockquote><br /> Decomprime i dati codificati.<br /> | 
| <a href="id3dx11dataloader-destroy.md"><strong>Distruggere</strong></a> | <blockquote>[!Note]<br />La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</blockquote><br /> Elimina il caricatore dopo il completamento di un elemento di lavoro.<br /> | 
| <a href="id3dx11dataloader-load.md"><strong>Caricamento</strong></a> | <blockquote>[!Note]<br />La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</blockquote><br /> Carica i dati da un disco.<br /> | 




 

## <a name="remarks"></a>Commenti

Questo oggetto può essere ereditato e i relativi membri possono essere ridefiniti. In questo modo è possibile personalizzare l'API per il caricamento e la decompressione dei formati di file personalizzati.

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

 

