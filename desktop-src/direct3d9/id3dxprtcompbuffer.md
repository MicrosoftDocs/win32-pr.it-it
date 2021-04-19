---
description: L'interfaccia ID3DXPRTCompBuffer archivia una versione compressa di un buffer ID3DXPRTBuffer per l'uso con l'analisi dei componenti principali (PCA).
ms.assetid: 97f8576c-24d5-4f60-923b-4d8d94382fe9
title: Interfaccia ID3DXPRTCompBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 323ed6f2bbe9ce4caf495a00330c1b1e0e83e158
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323456"
---
# <a name="id3dxprtcompbuffer-interface"></a>Interfaccia ID3DXPRTCompBuffer

L'interfaccia **ID3DXPRTCompBuffer** archivia una versione compressa di un buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) per l'uso con l'analisi dei componenti principali (PCA).

## <a name="members"></a>Membri

L'interfaccia **ID3DXPRTCompBuffer** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPRTCompBuffer** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXPRTCompBuffer** dispone di questi metodi.



| Metodo                                                             | Descrizione                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExtractBasis**](id3dxprtcompbuffer--extractbasis.md)           | Estrae i vettori di base di media e dell'analisi dei componenti principali (PCA) per un determinato cluster da un buffer di dati compresso **ID3DXPRTCompBuffer** .<br/>                                                                       |
| [**ExtractClusterIDs**](id3dxprtcompbuffer--extractclusterids.md) | Estrae gli ID cluster per campione da un buffer di dati compresso **ID3DXPRTCompBuffer** .<br/>                                                                                                                              |
| [**ExtractPCA**](id3dxprtcompbuffer--extractpca.md)               | Estrae i coefficienti di proiezione dell'analisi dei componenti principale per campione da un buffer di dati compresso **ID3DXPRTCompBuffer** .<br/>                                                                               |
| [**ExtractTexture**](id3dxprtcompbuffer--extracttexture.md)       | Estrae i coefficienti di proiezione del componente principale per campione (PCA) da un buffer di dati compresso **ID3DXPRTCompBuffer** e aggiunge i dati a un oggetto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .<br/> |
| [**ExtractToMesh**](id3dxprtcompbuffer--extracttomesh.md)         | Estrae i coefficienti di proiezione del componente principale per campione (PCA) da un buffer di dati compresso **ID3DXPRTCompBuffer** e aggiunge i dati a un oggetto [**ID3DXMesh**](id3dxmesh.md) .<br/>                 |
| [**GetHeight**](id3dxprtcompbuffer--getheight.md)                 | Recupera l'altezza, in pixel, della trama.<br/>                                                                                                                                                                         |
| [**GetNumChannels**](id3dxprtcompbuffer--getnumchannels.md)       | Recupera il numero di canali di colore utilizzati in memoria per archiviare gli esempi.<br/>                                                                                                                                                 |
| [**GetNumClusters**](id3dxprtcompbuffer--getnumclusters.md)       | Recupera il numero di cluster da utilizzare per la compressione.<br/>                                                                                                                                                                |
| [**GetNumCoeffs**](id3dxprtcompbuffer--getnumcoeffs.md)           | Recupera il numero di scalari per canale di colore utilizzato in memoria per archiviare gli esempi.<br/>                                                                                                                                      |
| [**GetNumPCA**](id3dxprtcompbuffer--getnumpca.md)                 | Recupera il numero di vettori di base dell'analisi dei componenti principali (PCA) da usare in ogni cluster.<br/>                                                                                                                        |
| [**GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md)         | Recupera il numero di vertici (o Texel) campionati.<br/>                                                                                                                                                                   |
| [**GetWidth**](id3dxprtcompbuffer--getwidth.md)                   | Recupera la larghezza della trama in pixel.<br/>                                                                                                                                                                          |
| [**Trama**](id3dxprtcompbuffer--istexture.md)                 | Indica se il buffer contiene una trama.<br/>                                                                                                                                                                        |
| [**NormalizeData**](id3dxprtcompbuffer--normalizedata.md)         | Normalizza tutti i pesi di analisi del componente principale (PCA) in modo che siano compresi tra-1 e 1. I vettori di base vengono modificati per riflettere questa normalizzazione.<br/>                                                                  |



 

## <a name="remarks"></a>Commenti

L'interfaccia **ID3DXPRTCompBuffer** viene ottenuta chiamando la funzione [**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md) .

Il tipo LPD3DXPRTCOMPBUFFER è definito come puntatore all'interfaccia **ID3DXPRTCompBuffer** .


```
typedef interface ID3DXPRTCompBuffer ID3DXPRTCompBuffer;
typedef interface ID3DXPRTCompBuffer *LPD3DXPRTCOMPBUFFER;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[**D3DXCreatePRTCompBuffer**](d3dxcreateprtcompbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer**](id3dxprtbuffer.md)
</dt> </dl>

 

 
