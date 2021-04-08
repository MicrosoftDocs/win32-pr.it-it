---
description: L'interfaccia ID3DXSprite fornisce un set di metodi che semplificano il processo di creazione di sprite con Microsoft Direct3D.
ms.assetid: ccf34fac-91a7-4734-bc62-aedaf4d66522
title: Interfaccia ID3DXSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3703132cd8a0f7744119d9b8cb5d9d48f260094c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886295"
---
# <a name="id3dxsprite-interface"></a>Interfaccia ID3DXSprite

L'interfaccia ID3DXSprite fornisce un set di metodi che semplificano il processo di creazione di sprite con Microsoft Direct3D.

## <a name="members"></a>Membri

L'interfaccia **ID3DXSprite** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXSprite** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXSprite** dispone di questi metodi.



| Metodo                                                | Descrizione                                                                                                                                                                                                                  |
|:------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inizia**](id3dxsprite--begin.md)                   | Prepara un dispositivo per il disegno degli sprite.<br/>                                                                                                                                                                            |
| [**Disegna**](id3dxsprite--draw.md)                     | Aggiunge uno sprite all'elenco di sprite in batch.<br/>                                                                                                                                                                     |
| [**Fine**](id3dxsprite--end.md)                       | Chiama [**ID3DXSprite:: Flush**](id3dxsprite--flush.md) e ripristina lo stato del dispositivo in modo che sia stato prima della chiamata a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md) .<br/>                                            |
| [**Svuotamento**](id3dxsprite--flush.md)                   | Impone l'invio di tutti gli sprite in batch al dispositivo. Gli Stati del dispositivo rimangono invariati dopo l'ultima chiamata a [**ID3DXSprite:: Begin**](id3dxsprite--begin.md). L'elenco degli sprite in batch viene quindi cancellato.<br/> |
| [**GetDevice**](id3dxsprite--getdevice.md)           | Recupera il dispositivo associato all'oggetto Sprite.<br/>                                                                                                                                                           |
| [**GetTransform**](id3dxsprite--gettransform.md)     | Ottiene la trasformazione sprite.<br/>                                                                                                                                                                                        |
| [**OnLostDevice**](id3dxsprite--onlostdevice.md)     | Usare questo metodo per rilasciare tutti i riferimenti alle risorse di memoria video ed eliminare tutti stateblocks. Questo metodo deve essere chiamato ogni volta che un dispositivo viene perso o prima di reimpostare un dispositivo.<br/>                              |
| [**OnResetDevice**](id3dxsprite--onresetdevice.md)   | Usare questo metodo per acquisire nuovamente le risorse e salvare lo stato iniziale.<br/>                                                                                                                                                   |
| [**SetTransform**](id3dxsprite--settransform.md)     | Imposta la trasformazione sprite.<br/>                                                                                                                                                                                        |
| [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) | Imposta la trasformazione di visualizzazione globale a sinistra per uno sprite. È necessaria una chiamata a questo metodo prima di eseguire il Billboard o l'ordinamento degli sprite.<br/>                                                                                 |
| [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) | Imposta la trasformazione di visualizzazione globale a destra per uno sprite. È necessaria una chiamata a questo metodo prima di eseguire il Billboard o l'ordinamento degli sprite.<br/>                                                                                |



 

## <a name="remarks"></a>Commenti

L'interfaccia **ID3DXSprite** viene ottenuta chiamando la funzione [**D3DXCreateSprite**](d3dxcreatesprite.md) .

L'applicazione in genere chiama prima [**ID3DXSprite:: Begin**](id3dxsprite--begin.md), che consente di controllare lo stato di rendering del dispositivo, la fusione alfa e la trasformazione e l'ordinamento degli sprite. Per ogni sprite da visualizzare, chiamare [**ID3DXSprite::D RAW**](id3dxsprite--draw.md). **ID3DXSprite::D RAW** può essere chiamato ripetutamente per archiviare un numero qualsiasi di sprite. Per visualizzare gli sprite in batch sul dispositivo, chiamare [**ID3DXSprite:: end**](id3dxsprite--end.md) o [**ID3DXSprite:: Flush**](id3dxsprite--flush.md).

Il tipo LPD3DXSPRITE è definito come puntatore all'interfaccia **ID3DXSprite** .


```
typedef interface ID3DXSprite ID3DXSprite;
typedef interface ID3DXSprite *LPD3DXSPRITE;
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

 

 
