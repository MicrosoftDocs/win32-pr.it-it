---
description: L'interfaccia ID3DXLine implementa il disegno a linee usando triangoli con trama.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: Interfaccia ID3DXLine (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1c535ff736e9a26e8316e4715f4be4022a6417df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058698"
---
# <a name="id3dxline-interface"></a>Interfaccia ID3DXLine

L'interfaccia ID3DXLine implementa il disegno a linee usando triangoli con trama.

## <a name="members"></a>Membri

L'interfaccia **ID3DXLine** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXLine** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXLine** dispone di questi metodi.



| Metodo                                                | Descrizione                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inizia**](id3dxline--begin.md)                     | Prepara un dispositivo per il disegno delle linee.<br/>                                                                                                                                                  |
| [**Disegna**](id3dxline--draw.md)                       | Disegna una striscia di linea nello spazio dello schermo. L'input è sotto forma di matrice che definisce i punti (di [**D3DXVECTOR2**](d3dxvector2.md)) nell'elenco di righe.<br/>                                   |
| [**DrawTransform**](id3dxline--drawtransform.md)     | Disegna una striscia di linea nello spazio dello schermo con una matrice di trasformazione input specificata.<br/>                                                                                                      |
| [**Fine**](id3dxline--end.md)                         | Ripristina lo stato del dispositivo nel modo in cui si trovava quando è stato chiamato [**ID3DXLine:: Begin**](id3dxline--begin.md) .<br/>                                                                                 |
| [**GetAntialias**](id3dxline--getantialias.md)       | Ottiene lo stato di anti-aliasing della linea.<br/>                                                                                                                                                     |
| [**GetDevice**](id3dxline--getdevice.md)             | Recupera il dispositivo Direct3D associato all'oggetto riga.<br/>                                                                                                                        |
| [**GetGLLines**](id3dxline--getgllines.md)           | Ottiene la modalità di disegno di riga in stile OpenGL.<br/>                                                                                                                                              |
| [**GetPattern**](id3dxline--getpattern.md)           | Ottiene il pattern stipple di linea.<br/>                                                                                                                                                        |
| [**GetPatternScale**](id3dxline--getpatternscale.md) | Ottiene il valore della scala del pattern stipple.<br/>                                                                                                                                                 |
| [**GetWidth**](id3dxline--getwidth.md)               | Ottiene lo spessore della linea.<br/>                                                                                                                                                       |
| [**OnLostDevice**](id3dxline--onlostdevice.md)       | Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.<br/> |
| [**OnResetDevice**](id3dxline--onresetdevice.md)     | Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.<br/>                                                                                                                       |
| [**SetAntialias**](id3dxline--setantialias.md)       | Consente di abilitare l'anti-aliasing della linea.<br/>                                                                                                                                                            |
| [**SetGLLines**](id3dxline--setgllines.md)           | Consente di impostare la modalità per creare linee di tipo OpenGL.<br/>                                                                                                                                          |
| [**Criteri di ricerca**](id3dxline--setpattern.md)           | Applica un modello stipple alla riga.<br/>                                                                                                                                                |
| [**SetPatternScale**](id3dxline--setpatternscale.md) | Estende il pattern stipple lungo la direzione della riga.<br/>                                                                                                                               |
| [**SetWidth**](id3dxline--setwidth.md)               | Specifica lo spessore della linea.<br/>                                                                                                                                                  |



 

## <a name="remarks"></a>Commenti

Creare un oggetto disegno a linee con [**D3DXCreateLine**](d3dxcreateline.md).

Il tipo LPD3DXLINE è definito come puntatore all'interfaccia **ID3DXLine** .


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
