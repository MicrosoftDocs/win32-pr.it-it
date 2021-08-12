---
description: L'interfaccia ID3DXPRTEngine viene usata per calcolare una simulazione PRT (Precomputed Radiance Transfer). I metodi vengono in genere usati offline per calcolare vettori di trasferimento per vertice o per texel prima della modellazione 3D in tempo reale.
ms.assetid: d5be657f-2b0c-48fd-a7f0-ddb90107772f
title: Interfaccia ID3DXPRTEngine (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: bef527f9044c01b0696e86b44ddaef7ec72c336771ed136ddd071d11c0d73836
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293355"
---
# <a name="id3dxprtengine-interface"></a>Interfaccia ID3DXPRTEngine

L'interfaccia ID3DXPRTEngine viene usata per calcolare una simulazione PRT (Precomputed Radiance Transfer). I metodi vengono in genere usati offline per calcolare vettori di trasferimento per vertice o per texel prima della modellazione 3D in tempo reale.

## <a name="members"></a>Membri

**L'interfaccia ID3DXPRTEngine** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DXPRTEngine** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DXPRTEngine** include questi metodi.



| Metodo                                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)                       | Usa il ray tracing efficiente nelle simulazioni PRT (Precomputed Radiance Transfer) per determinare se un raggio interseca una mesh. Se viene trovata un'intersezione, il metodo restituisce l'indice della faccia della mesh più vicina a cui viene raggiunto il raggio e le coordinate barycentriche del punto di intersezione.<br/>                                                                                                                                                                                |
| [**ComputeBounce**](id3dxprtengine--computebounce.md)                                     | Calcola la luminosità di origine risultante da un singolo butto di luce interreflected. Questo metodo può essere usato per qualsiasi scena accesa, incluso un modello PRT (Precomputed Radiance Transfer) sferico basato su arance(SH).<br/>                                                                                                                                                                                                                                                    |
| [**ComputeBounceAdaptive**](id3dxprtengine--computebounceadaptive.md)                     | Calcola la luminosità di origine risultante da un singolo rimbalzo di luce interreflected, usando il campionamento adattivo. Questo metodo genera nuovi vertici e visi nella mesh per approssimare in modo più accurato il segnale PRT (Precomputed Radiance Transfer). Questo metodo può essere usato per qualsiasi scena accesa, incluso un modello PRT sferico basato su sh(SH).<br/>                                                                                                                   |
| [**ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)                 | Calcola il contributo di illuminazione diretta agli oggetti 3D in cui la radice di origine è rappresentata da un'approssimazione sferica arica (SH).<br/>                                                                                                                                                                                                                                                                                                                            |
| [**ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) | Calcola il contributo di illuminazione diretta agli oggetti 3D in cui la radice di origine è rappresentata da un'approssimazione sferica aricale (SH), usando il campionamento adattivo. Questo metodo genera nuovi vertici e visi nella mesh per approssimare in modo più accurato il segnale PRT (Precomputed Radiance Transfer).<br/>                                                                                                                                                           |
| [**ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md)           | Usa la GPU per calcolare il contributo di illuminazione diretta agli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione sferica arica (SH). Il calcolo dell'illuminazione della GPU sarà in genere molto più veloce rispetto alla CPU.<br/>                                                                                                                                                                                                                            |
| [**ComputeLDPRTCoeffs**](id3dxprtengine--computeldprtcoeffs.md)                           | Calcola i coefficienti LDPRT (Precomputed Radiance Transfer) locali rispetto ai vettori normali per campione per ridurre al minimo l'errore dei minimi quadrati rispetto ai dati [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input. Questi coefficienti possono essere usati con vettori normali con interfaccia o trasformati per modellare gli effetti globali sugli oggetti dinamici.<br/>                                                                                                                     |
| [**Calcoli**](id3dxprtengine--computess.md)                                             | Calcola la luminosità di origine risultante dalla dispersione dei subsurface, usando le proprietà dei materiali impostate da [**ID3DXPRTEngine::SetMeshMaterials.**](id3dxprtengine--setmeshmaterials.md) Questo metodo può essere usato solo per i materiali definiti per vertice in un oggetto mesh.<br/>                                                                                                                                                                                                       |
| [**ComputeSSAdaptive**](id3dxprtengine--computessadaptive.md)                             | Calcola un vettore di trasferimento che esegue il mapping della radice di origine per uscire dalla dispersione delle sottoaree, usando il campionamento adattivo e le proprietà materiali impostate da [**ID3DXPRTEngine::SetMeshMaterials.**](id3dxprtengine--setmeshmaterials.md) Il metodo genera nuovi vertici e visi nella mesh per approssimare in modo più accurato il segnale PRT (Precomputed Radiance Transfer). Questo metodo può essere usato solo per i materiali definiti per vertice in un oggetto mesh.<br/> |
| [**ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md)               | Calcola campioni di trasferimento della radice pre-calcolata (PRT) per un punto arbitrario (e un vettore normale).<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md)           | Calcola, in un punto arbitrario non su una mesh, un vettore di trasferimento che esegue il mapping della radice di origine (rappresentata da un'approssimazione sferica aricale) per uscire dalla radice.<br/>                                                                                                                                                                                                                                                                                                   |
| [**ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)                       | Calcola una proiezione dell'illuminazione diretta dal mancato rilascio della luce precedente in vettori di base sferici aricali (SH) che rappresentano la luminosità dell'evento imprevisto in posizioni specificate.<br/>                                                                                                                                                                                                                                                                                         |
| [**ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)       | Calcola una proiezione di illuminazione distante in vettori di base sferici aricali (SH) che rappresentano la luminosità degli eventi imprevisti in posizioni specificate.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ExtractPerVertexAlbedo**](id3dxprtengine--extractpervertexalbedo.md)                   | Copia i valori albedo per vertice da una mesh.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**FreeBounceData**](id3dxprtengine--freebouncedata.md)                                   | Libera la memoria usata per i dati temporanei di simulazione di luce temporaneo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**FreeSSData**](id3dxprtengine--freessdata.md)                                           | Libera la memoria usata per i dati temporanei di simulazione della dispersione di luce sotto la superficie.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**GetAdaptedMesh**](id3dxprtengine--getadaptedmesh.md)                                   | Restituisce una mesh con modifiche risultanti dal campionamento spaziale adattivo. La mesh restituita contiene solo posizioni, normali e coordinate di trama (se definite).<br/>                                                                                                                                                                                                                                                                                                   |
| [**GetNumFaces**](id3dxprtengine--getnumfaces.md)                                         | Recupera il numero di visi nella mesh, inclusi eventuali nuovi visi aggiunti come risultato del campionamento spaziale adattivo.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**GetNumVerts**](id3dxprtengine--getnumverts.md)                                         | Recupera il numero di vertici nella mesh, inclusi eventuali nuovi vertici aggiunti come risultato del campionamento spaziale adattivo.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**GetVertexAlbedo**](id3dxprtengine--getvertexalbedo.md)                                 | Recupera i valori albedo dei vertici della mesh.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md)                                   | Moltiplica ogni vettore PRT (Pre-Computed Radiance Transfer) per l'albedo per vertice.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ResampleBuffer**](id3dxprtengine--resamplebuffer.md)                                   | Ricampiona un buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input e lo salva in un buffer di output. Questo metodo può essere usato per convertire un buffer dei vertici in un buffer di trama e viceversa. Può essere usato anche per convertire i buffer a canale singolo in buffer a 3 canali e viceversa.<br/>                                                                                                                                                                                  |
| [**RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)                               | Sottodivide i visi in una mesh, consentendo il campionamento adattivo conservativo che non eliminerà le funzioni nella mesh.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**ScaleMeshChunk**](id3dxprtengine--scalemeshchunk.md)                                   | Ridimensiona tutti gli esempi associati a una determinata sottomesh. Il metodo è utile per calcolare la dispersione delle sottoaree.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**SetCallBack**](id3dxprtengine--setcallback.md)                                         | Imposta un puntatore a una funzione di callback facoltativa che calcola la percentuale di calcoli sferici aricali completati e offre al chiamante la possibilità di interrompere il simulatore.<br/>                                                                                                                                                                                                                                                                               |
| [**SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)                               | Imposta le proprietà del materiale mesh nella scena 3D. Usare questo metodo per specificare i parametri di dispersione sotto la superficie.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)                     | Imposta le distanze minima e massima di intersezione tra oggetti 3D. Questi valori di distanza possono essere usati per controllare la distanza minima o massima che gli oggetti possono nascondere o riflettere la luce. Ad esempio, il metodo può essere usato per limitare l'ombreggiatura delle caratteristiche vicine di un modello 3D.<br/>                                                                                                                                                                          |
| [**SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md)                             | Imposta un valore albedo per ogni texel, sovrascrivendo i valori albedo precedenti.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**SetPerTexelNormal**](id3dxprtengine--setpertexelnormal.md)                             | Imposta un vettore normale per ogni texel in un oggetto trama. Questo metodo viene usato per archiviare i vettori normali dei vertici da una mesh (o normali vertici interpolati se viene calcolato il trasferimento della radice pre-calcolata (PRT) basato su pixel).<br/>                                                                                                                                                                                                                                          |
| [**SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md)                           | Imposta un valore albedo per ogni vertice della mesh, sovrascrivendo i valori albedo precedenti.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| [**SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)                                 | Imposta le proprietà di campionamento usate dal simulatore PRT (Pre-computed Radiance Transfer).<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| [**ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)                         | Usa il ray tracing efficiente nelle simulazioni PRT (Precomputed Radiance Transfer) per determinare se un raggio interseca una mesh. Utilizzato in genere per determinare se un determinato punto è ombreggiato.<br/>                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Commenti

Per eseguire la conversione da RGB a valori di luminance, viene usata la formula seguente:


```
Luminance = R * 0.2125 + G * 0.7154 + B * 0.0721
```



**L'interfaccia ID3DXPRTEngine** viene ottenuta chiamando la [**funzione D3DXCreatePRTEngine.**](d3dxcreateprtengine.md)

Il tipo LPD3DXPRTENGINE è definito come puntatore **all'interfaccia ID3DXPRTEngine.**


```
typedef interface ID3DXPRTEngine ID3DXPRTEngine;
typedef interface ID3DXPRTEngine *LPD3DXPRTENGINE;
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

[**D3DXCreatePRTEngine**](d3dxcreateprtengine.md)
</dt> <dt>

[Trasferimento di radiance pre-ricalcolato (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
