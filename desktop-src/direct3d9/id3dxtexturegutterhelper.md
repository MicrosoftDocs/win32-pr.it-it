---
description: L'interfaccia ID3DXTextureGutterHelper viene utilizzata per creare e gestire aree di gronda in una trama. Le aree di rilegatura separano le trame e consentono l'interpolazione bilineare per evitare il rendering di artefatti a limiti di trama
ms.assetid: 097e27bf-a1a6-4e7e-bdad-33015b50f91f
title: Interfaccia ID3DXTextureGutterHelper (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ece03e14da490bd6d6f5aef69f9457939bc8bab7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355614"
---
# <a name="id3dxtexturegutterhelper-interface"></a>Interfaccia ID3DXTextureGutterHelper

L'interfaccia ID3DXTextureGutterHelper viene utilizzata per creare e gestire aree di gronda in una trama. Le aree di rilegatura separano le trame e consentono l'interpolazione bilineare per evitare il rendering di artefatti a limiti di trama

Il Get... i metodi forniscono l'accesso alle strutture di dati utilizzate dall'oggetto Apply... Metodi.

## <a name="members"></a>Membri

L'interfaccia **ID3DXTextureGutterHelper** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXTextureGutterHelper** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXTextureGutterHelper** dispone di questi metodi.



| Metodo                                                                   | Descrizione                                                                                            |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) | Applica le grondature a un buffer di trama FLOAT.<br/>                                                  |
| [**ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md)     | Applica le grondanze a un oggetto buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .<br/>               |
| [**ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)     | Applica le grondanze a un oggetto trama [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .<br/>        |
| [**GetBaryMap**](id3dxtexturegutterhelper--getbarymap.md)               | Recupera le coordinate baricentrica Texel.<br/>                                                    |
| [**GetFaceMap**](id3dxtexturegutterhelper--getfacemap.md)               | Recupera l'indice della faccia mesh a cui appartiene ogni Texel.<br/>                           |
| [**GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md)           | Riceve un valore della classe Texel che indica la classe Texel in base alla posizione di ogni Texel.<br/> |
| [**GetHeight**](id3dxtexturegutterhelper--getheight.md)                 | Recupera l'altezza, in pixel, della trama.<br/>                                             |
| [**GetTexelMap**](id3dxtexturegutterhelper--gettexelmap.md)             | Recupera le coordinate di trama (u, v) di ogni Texel.<br/>                                     |
| [**GetWidth**](id3dxtexturegutterhelper--getwidth.md)                   | Recupera la larghezza della trama in pixel.<br/>                                              |
| [**ResampleTex**](id3dxtexturegutterhelper--resampletex.md)             | Ricampiona una trama nella parametrizzazione di questo gutterhelper.<br/>                              |
| [**SetBaryMap**](id3dxtexturegutterhelper--setbarymap.md)               | Imposta le coordinate del baricentrica Texel.<br/>                                                         |
| [**SetFaceMap**](id3dxtexturegutterhelper--setfacemap.md)               | Imposta l'indice della faccia mesh a cui appartiene ogni Texel.<br/>                                |
| [**SetGutterMap**](id3dxtexturegutterhelper--setguttermap.md)           | Imposta un valore della classe Texel che indica la classe Texel in base alla posizione di ogni Texel.<br/>     |
| [**SetTexelMap**](id3dxtexturegutterhelper--settexelmap.md)             | Imposta le coordinate di trama (u, v) di ogni Texel.<br/>                                          |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Se usato con il trasferimento di luminosità pre-calcolato (PRT), questa interfaccia richiede una parametrizzazione univoca del modello. Ogni Texel deve corrispondere a un singolo punto sulla superficie del modello e viceversa. Se il modello include più trame, deve essere suddiviso in parti separate, ognuna delle quali contiene un oggetto di supporto per la gronda per trama.

 

Questa interfaccia può essere utilizzata per generare una mappa nello spazio di trama in cui ogni Texel si trova in una delle quattro classi.



| Classe Texel | Percorso Texel                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Punto non valido; Texel non verrà usato.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Triangolo interno.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Barra interna.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Barra interna; Texel verrà valutato come un esempio completo nei metodi [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)o [**ID3DXTextureGutterHelper:: ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) . |



 

Per le classi 1 e 2, un Texel viene archiviato con la faccia a cui appartiene, insieme alle coordinate baricentrica dei primi due vertici della faccia. I vertici della gronda vengono assegnati al bordo più vicino nello spazio di trama.

Nessuna classe Texel 3.

L'interfaccia **ID3DXTextureGutterHelper** viene ottenuta chiamando la funzione [**D3DXCreateTextureGutterHelper**](d3dxcreatetexturegutterhelper.md) .

Il tipo LPD3DXTEXTUREGUTTERHELPER è definito come puntatore all'interfaccia **ID3DXTextureGutterHelper** .


```
typedef interface ID3DXTextureGutterHelper ID3DXTextureGutterHelper;
typedef interface ID3DXTextureGutterHelper *LPD3DXTEXTUREGUTTERHELPER;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
