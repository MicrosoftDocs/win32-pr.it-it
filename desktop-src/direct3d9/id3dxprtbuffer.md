---
description: L'interfaccia ID3DXPRTBuffer viene usata come buffer di dati per archiviare i dati di vertici e pixel da usare con i metodi e le funzioni PRT (Precomputed Radiance Transfer).
ms.assetid: 36c1fd13-0949-4991-93cb-41ace458802d
title: Interfaccia ID3DXPRTBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 69f4a40055adea1440436cc54cecc5735db95bc01787cb779cc8a7d6c51b0011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120545"
---
# <a name="id3dxprtbuffer-interface"></a>Interfaccia ID3DXPRTBuffer

L'interfaccia ID3DXPRTBuffer viene usata come buffer di dati per archiviare i dati di vertici e pixel da usare con i metodi e le funzioni PRT (Precomputed Radiance Transfer).

## <a name="members"></a>Membri

**L'interfaccia ID3DXPRTBuffer** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXPRTBuffer** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXPRTBuffer** include questi metodi.



| Metodo                                                   | Descrizione                                                                                                                                                                                   |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBuffer**](id3dxprtbuffer--addbuffer.md)           | Aggiunge un altro buffer a **ID3DXPRTBuffer** e archivia i risultati in **ID3DXPRTBuffer.**<br/>                                                                                        |
| [**AttachGH**](id3dxprtbuffer--attachgh.md)             | Associa un [**oggetto ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) all'oggetto **ID3DXPRTBuffer.**<br/>                                                              |
| [**EvalGH**](id3dxprtbuffer--evalgh.md)                 | Applica i dati archiviati della trame a un buffer di trama **ID3DXPRTBuffer.**<br/>                                                                                                        |
| [**ExtractTexture**](id3dxprtbuffer--extracttexture.md) | Estrae i dati dei coefficienti da un canale di colore del buffer per un intervallo specificato di coefficienti e aggiunge i dati a un [**oggetto IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)<br/> |
| [**ExtractToMesh**](id3dxprtbuffer--extracttomesh.md)   | Estrae i dati del coefficiente da un buffer a canale singolo e li aggiunge a [**un oggetto ID3DXMesh.**](id3dxmesh.md)<br/>                                                              |
| [**Getheight**](id3dxprtbuffer--getheight.md)           | Recupera l'altezza della trama, in pixel.<br/>                                                                                                                                    |
| [**GetNumChannels**](id3dxprtbuffer--getnumchannels.md) | Recupera il numero di canali di colore utilizzati in memoria per archiviare i campioni.<br/>                                                                                                            |
| [**GetNumCoeffs**](id3dxprtbuffer--getnumcoeffs.md)     | Recupera il numero di scalari per canale di colore utilizzato in memoria per archiviare i campioni.<br/>                                                                                                 |
| [**GetNumSamples**](id3dxprtbuffer--getnumsamples.md)   | Recupera il numero di vertici (o texel) campionati.<br/>                                                                                                                              |
| [**GetWidth**](id3dxprtbuffer--getwidth.md)             | Recupera la larghezza della trama, in pixel.<br/>                                                                                                                                     |
| [**IsTexture**](id3dxprtbuffer--istexture.md)           | Indica se il buffer contiene una trama.<br/>                                                                                                                                   |
| [**LockBuffer**](id3dxprtbuffer--lockbuffer.md)         | Blocca un intervallo di dati di esempio vertice o texel e ottiene un puntatore alla posizione nella memoria buffer.<br/>                                                                               |
| [**ReleaseGH**](id3dxprtbuffer--releasegh.md)           | Annulla l'associazione di un oggetto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) associato **all'oggetto ID3DXPRTBuffer.**<br/>                                                   |
| [**Ridimensionamento**](id3dxprtbuffer--resize.md)                 | Modifica il numero di campioni contenuti nel buffer.<br/>                                                                                                                             |
| [**ScaleBuffer**](id3dxprtbuffer--scalebuffer.md)       | Moltiplica ogni valore nel buffer per un valore costante.<br/>                                                                                                                          |
| [**UnlockBuffer**](id3dxprtbuffer--unlockbuffer.md)     | Termina la durata del puntatore ppData restituito da [**ID3DXPRTBuffer::LockBuffer**](id3dxprtbuffer--lockbuffer.md).<br/>                                                              |



 

## <a name="remarks"></a>Commenti

**L'interfaccia ID3DXPRTBuffer** viene ottenuta chiamando le funzioni [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) o [**D3DXCreatePRTBufferTex.**](d3dxcreateprtbuffertex.md)

Il tipo LPD3DXPRTBUFFER è definito come puntatore **all'interfaccia ID3DXPRTBuffer.**


```
typedef interface ID3DXPRTBuffer ID3DXPRTBuffer;
typedef interface ID3DXPRTBuffer *LPD3DXPRTBUFFER;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> <dt>

[**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
