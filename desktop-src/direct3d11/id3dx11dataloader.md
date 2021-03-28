---
title: Interfaccia ID3DX11DataLoader (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Oggetto caricamento dati utilizzato dall'interfaccia ID3DX11ThreadPump per il caricamento asincrono dei dati.
ms.assetid: 878929ea-0228-4650-9ca0-f83d60d9f915
keywords:
- Interfaccia ID3DX11DataLoader Direct3D 11
- Interfaccia ID3DX11DataLoader Direct3D 11, descritta
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
ms.openlocfilehash: 68236451bf2ba6f491d17541f7d4ca627f5063c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119178"
---
# <a name="id3dx11dataloader-interface"></a>Interfaccia ID3DX11DataLoader

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.

 

Oggetto caricamento dati utilizzato dall' [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md) per il caricamento asincrono dei dati.

## <a name="members"></a>Membri

L'interfaccia **ID3DX11DataLoader** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11DataLoader** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX11DataLoader** dispone di questi metodi.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Metodo</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataloader-decompress.md"><strong>Decomprimere</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/> Decomprime i dati codificati.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11dataloader-destroy.md"><strong>Eliminare</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/> Elimina il caricatore dopo il completamento di un elemento di lavoro.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataloader-load.md"><strong>Caricamento</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.
</blockquote>
<br/> Carica i dati da un disco.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Commenti

Questo oggetto può essere ereditato e i relativi membri ridefiniti. Questa operazione consente di personalizzare l'API per il caricamento e la decompressione dei formati di file personalizzati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>D3DX11core. h</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

