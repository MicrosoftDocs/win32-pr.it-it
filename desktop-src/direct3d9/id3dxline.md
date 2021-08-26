---
description: L'interfaccia ID3DXLine implementa il disegno di linee usando triangoli trame.
ms.assetid: 87472618-d3e4-4008-9009-ae17fc7b696d
title: Interfaccia ID3DXLine (D3dx9core.h)
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
ms.openlocfilehash: a9677ca802a800624b374212c6942ab6676423f8d63e62cbf136a8b9e69c533d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951371"
---
# <a name="id3dxline-interface"></a>Interfaccia ID3DXLine

L'interfaccia ID3DXLine implementa il disegno di linee usando triangoli trame.

## <a name="members"></a>Membri

**L'interfaccia ID3DXLine** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXLine** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXLine** include questi metodi.



| Metodo                                                | Descrizione                                                                                                                                                                                      |
|:------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inizia**](id3dxline--begin.md)                     | Prepara un dispositivo per il disegno di linee.<br/>                                                                                                                                                  |
| [**Disegna**](id3dxline--draw.md)                       | Disegna un elenco di linee nello spazio dello schermo. L'input è sotto forma di matrice che definisce i punti (di [**D3DXVECTOR2)**](d3dxvector2.md)nell'elenco di linee.<br/>                                   |
| [**DrawTransform**](id3dxline--drawtransform.md)     | Disegna un elenco di linee nello spazio dello schermo con una matrice di trasformazione di input specificata.<br/>                                                                                                      |
| [**Fine**](id3dxline--end.md)                         | Ripristina lo stato del dispositivo al momento della [**chiamata a ID3DXLine::Begin.**](id3dxline--begin.md)<br/>                                                                                 |
| [**GetAntialias**](id3dxline--getantialias.md)       | Ottiene lo stato dell'anti-aliasing della riga.<br/>                                                                                                                                                     |
| [**GetDevice**](id3dxline--getdevice.md)             | Recupera il dispositivo Direct3D associato all'oggetto linea.<br/>                                                                                                                        |
| [**GetGLLines**](id3dxline--getgllines.md)           | Ottiene la modalità di disegno linea in stile OpenGL.<br/>                                                                                                                                              |
| [**Getpattern**](id3dxline--getpattern.md)           | Ottiene il motivo dello stipple della riga.<br/>                                                                                                                                                        |
| [**GetPatternScale**](id3dxline--getpatternscale.md) | Ottiene il valore di scala dello schema stipple.<br/>                                                                                                                                                 |
| [**GetWidth**](id3dxline--getwidth.md)               | Ottiene lo spessore della linea.<br/>                                                                                                                                                       |
| [**OnLostDevice**](id3dxline--onlostdevice.md)       | Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti gli blocchi di stato. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.<br/> |
| [**OnResetDevice**](id3dxline--onresetdevice.md)     | Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.<br/>                                                                                                                       |
| [**SetAntialias**](id3dxline--setantialias.md)       | Attiva o disattiva l'anti-aliasing delle righe.<br/>                                                                                                                                                            |
| [**SetGLLines**](id3dxline--setgllines.md)           | Attiva o disattiva la modalità per disegnare linee in stile OpenGL.<br/>                                                                                                                                          |
| [**SetPattern**](id3dxline--setpattern.md)           | Applica un motivo a stipple alla linea.<br/>                                                                                                                                                |
| [**SetPatternScale**](id3dxline--setpatternscale.md) | Estende lo stipple pattern lungo la direzione della linea.<br/>                                                                                                                               |
| [**SetWidth**](id3dxline--setwidth.md)               | Specifica lo spessore della linea.<br/>                                                                                                                                                  |



 

## <a name="remarks"></a>Commenti

Creare un oggetto disegno linea con [**D3DXCreateLine.**](d3dxcreateline.md)

Il tipo LPD3DXLINE è definito come puntatore **all'interfaccia ID3DXLine.**


```
typedef interface ID3DXLine ID3DXLine;
typedef interface ID3DXLine *LPD3DXLINE;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
