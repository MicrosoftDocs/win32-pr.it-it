---
description: L'interfaccia ID3DXPRTEngine viene utilizzata per calcolare una simulazione di trasferimento di luminosità (PRT) pre-calcolata. I metodi vengono in genere usati offline per calcolare vettori di trasferimento per vertice o per Texel prima della modellazione 3D in tempo reale.
ms.assetid: d5be657f-2b0c-48fd-a7f0-ddb90107772f
title: Interfaccia ID3DXPRTEngine (D3DX9Mesh. h)
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
ms.openlocfilehash: 5507a79a60b2ffcb3cf801ea0454c7306bcde056
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322457"
---
# <a name="id3dxprtengine-interface"></a>Interfaccia ID3DXPRTEngine

L'interfaccia ID3DXPRTEngine viene utilizzata per calcolare una simulazione di trasferimento di luminosità (PRT) pre-calcolata. I metodi vengono in genere usati offline per calcolare vettori di trasferimento per vertice o per Texel prima della modellazione 3D in tempo reale.

## <a name="members"></a>Membri

L'interfaccia **ID3DXPRTEngine** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXPRTEngine** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXPRTEngine** dispone di questi metodi.



| Metodo                                                                                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ClosestRayIntersects**](id3dxprtengine--closestrayintersects.md)                       | Usa un'analisi efficiente del raggio nelle simulazioni del trasferimento di luminosità pre-calcolate (PRT) per determinare se un raggio interseca una mesh. Se viene rilevata un'intersezione, il metodo restituisce l'indice della faccia mesh più vicina raggiunta dal raggio e dalle coordinate baricentrica del punto di intersezione.<br/>                                                                                                                                                                                |
| [**ComputeBounce**](id3dxprtengine--computebounce.md)                                     | Calcola la luminosità di origine risultante da un singolo rimbalzo della luce con riflesso. Questo metodo può essere usato per qualsiasi scena illuminata, incluso un modello PRT (precomputed Radiance Transfer) basato su SH (sferica).<br/>                                                                                                                                                                                                                                                    |
| [**ComputeBounceAdaptive**](id3dxprtengine--computebounceadaptive.md)                     | Calcola la luminosità di origine risultante da un singolo rimbalzo della luce con riflesso, usando il campionamento adattivo. Questo metodo genera nuovi vertici e visi sulla mesh per approssimare in modo più accurato il segnale PRT (pre-Computed Radiance Transfer). Questo metodo può essere usato per qualsiasi scena illuminata, incluso un modello di PRT a sferica (SH).<br/>                                                                                                                   |
| [**ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)                 | Calcola il contributo di illuminazione diretta agli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione di un'armonica sferica (SH).<br/>                                                                                                                                                                                                                                                                                                                            |
| [**ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) | Calcola il contributo di illuminazione diretta per gli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione armonica sferica (SH), usando il campionamento adattivo. Questo metodo genera nuovi vertici e visi sulla mesh per approssimare in modo più accurato il segnale PRT (pre-Computed Radiance Transfer).<br/>                                                                                                                                                           |
| [**ComputeDirectLightingSHGPU**](id3dxprtengine--computedirectlightingshgpu.md)           | Usa la GPU per calcolare il contributo di illuminazione diretta agli oggetti 3D in cui la luminosità di origine è rappresentata da un'approssimazione di un'armonica sferica (SH). Il calcolo dell'illuminazione sulla GPU sarà in genere molto più veloce rispetto alla CPU.<br/>                                                                                                                                                                                                                            |
| [**ComputeLDPRTCoeffs**](id3dxprtengine--computeldprtcoeffs.md)                           | Consente di calcolare i coefficienti LDPRT (precomputed Radiance Transfer) a livello locale rispetto ai vettori normali per campione per ridurre al minimo l'errore dei minimi quadrati rispetto ai dati [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input. Questi coefficienti possono essere usati con vettori normali o trasformati per modellare gli effetti globali sugli oggetti dinamici.<br/>                                                                                                                     |
| [**ComputeSS**](id3dxprtengine--computess.md)                                             | Calcola la luminosità di origine risultante dalla dispersione della sottosuperficie, usando le proprietà del materiale impostate da [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). Questo metodo può essere utilizzato solo per i materiali definiti per ogni vertice in un oggetto mesh.<br/>                                                                                                                                                                                                       |
| [**ComputeSSAdaptive**](id3dxprtengine--computessadaptive.md)                             | Calcola un vettore di trasferimento che esegue il mapping della luminosità di origine alla luminosità di uscita risultante dalla dispersione della sottosuperficie, usando il campionamento adattivo e le proprietà del materiale impostate da [**ID3DXPRTEngine:: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). Il metodo genera nuovi vertici e visi sulla mesh per approssimare in modo più accurato il segnale PRT (pre-Computed Radiance Transfer). Questo metodo può essere utilizzato solo per i materiali definiti per ogni vertice in un oggetto mesh.<br/> |
| [**ComputeSurfSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md)               | Calcola gli esempi di trasferimento di radianza (PRT) pre-calcolati per un punto arbitrario (e il vettore normale).<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md)           | Calcola, in un punto arbitrario non su una mesh, un vettore di trasferimento che esegue il mapping della luminosità del codice sorgente, rappresentata da un'approssimazione ad armonica sferica (SH), per uscire dallo splendore.<br/>                                                                                                                                                                                                                                                                                                   |
| [**ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)                       | Calcola una proiezione dell'illuminazione diretta dal rimbalzo della luce precedente in vettori di base armonici sferici che rappresentano la radianza dell'evento imprevisto nelle posizioni specificate.<br/>                                                                                                                                                                                                                                                                                         |
| [**ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)       | Calcola una proiezione di illuminazione distante in vettori di base armonica sferica (SH) che rappresentano la luminosità dell'evento imprevisto in posizioni specificate.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ExtractPerVertexAlbedo**](id3dxprtengine--extractpervertexalbedo.md)                   | Copia i valori di albedo per vertice da una mesh.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**FreeBounceData**](id3dxprtengine--freebouncedata.md)                                   | Libera la memoria usata per i dati di simulazione della luce rimbalzata temporanea.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**FreeSSData**](id3dxprtengine--freessdata.md)                                           | Libera la memoria usata per i dati di simulazione della luce della sottosuperficie temporanea.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| [**GetAdaptedMesh**](id3dxprtengine--getadaptedmesh.md)                                   | Restituisce una mesh con modifiche derivanti dal campionamento spaziale adattivo. La mesh restituita contiene solo posizioni, normali e coordinate di trama (se definito).<br/>                                                                                                                                                                                                                                                                                                   |
| [**GetNumFaces**](id3dxprtengine--getnumfaces.md)                                         | Recupera il numero di visi nella mesh, inclusi eventuali nuovi visi aggiunti in seguito al campionamento spaziale adattivo.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**GetNumVerts**](id3dxprtengine--getnumverts.md)                                         | Recupera il numero di vertici nella mesh, inclusi tutti i nuovi vertici aggiunti come risultato del campionamento spaziale adattivo.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**GetVertexAlbedo**](id3dxprtengine--getvertexalbedo.md)                                 | Recupera i valori albedo dei vertici mesh.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md)                                   | Moltiplica ogni vettore PRT (pre-Computed Radiance Transfer) per l'albedo per vertice.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**ResampleBuffer**](id3dxprtengine--resamplebuffer.md)                                   | Ricampiona un buffer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input e lo salva in un buffer di output. Questo metodo può essere utilizzato per convertire un buffer di vertice in un buffer di trama e viceversa. Può essere usato anche per convertire i buffer a canale singolo in buffer a 3 canali e viceversa.<br/>                                                                                                                                                                                  |
| [**RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)                               | Suddivide i visi su una mesh, consentendo il campionamento adattivo conservativo che non eliminerà le funzionalità sulla rete.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**ScaleMeshChunk**](id3dxprtengine--scalemeshchunk.md)                                   | Ridimensiona tutti gli esempi associati a una data mesh specificata. Il metodo è utile per il calcolo della dispersione della sottosuperficie.<br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**CallBack**](id3dxprtengine--setcallback.md)                                         | Imposta un puntatore a una funzione di callback facoltativa che calcola la percentuale di calcoli armonici sferici (SH) completati e fornisce al chiamante la possibilità di interrompere il simulatore.<br/>                                                                                                                                                                                                                                                                               |
| [**SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md)                               | Imposta le proprietà del materiale mesh nella scena 3D. Utilizzare questo metodo per specificare i parametri di dispersione della sottosuperficie.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**SetMinMaxIntersection**](id3dxprtengine--setminmaxintersection.md)                     | Imposta le distanze minime e massime di intersezione tra oggetti 3D. Questi valori di distanza possono essere utilizzati per controllare la distanza minima o massima che gli oggetti possono nascondere o rispecchiare la luce. Ad esempio, il metodo può essere usato per limitare l'ombreggiatura delle funzionalità vicine di un modello 3D.<br/>                                                                                                                                                                          |
| [**SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md)                             | Imposta un valore albedo per ogni Texel, sovrascrivendo i valori albedo precedenti.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**SetPerTexelNormal**](id3dxprtengine--setpertexelnormal.md)                             | Imposta un vettore normale per ogni Texel in un oggetto trama. Questo metodo viene usato per archiviare i vettori normali dei vertici da una mesh (o le normali del vertice interpolato se viene calcolato il trasferimento di luminosità precalcolata basata su pixel).<br/>                                                                                                                                                                                                                                          |
| [**SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md)                           | Imposta un valore albedo per ogni vertice mesh, sovrascrivendo i valori albedo precedenti.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| [**SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)                                 | Imposta le proprietà di campionamento utilizzate dal simulatore di trasferimento di luminosità (PRT) pre-calcolato.<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| [**ShadowRayIntersects**](id3dxprtengine--shadowrayintersects.md)                         | Usa un'analisi efficiente del raggio nelle simulazioni del trasferimento di luminosità pre-calcolate (PRT) per determinare se un raggio interseca una mesh. Viene in genere utilizzato per determinare se un punto specificato è ombreggiato.<br/>                                                                                                                                                                                                                                                                             |



 

## <a name="remarks"></a>Commenti

Per eseguire la conversione da valori RGB a luminanza, viene utilizzata la formula seguente:


```
Luminance = R * 0.2125 + G * 0.7154 + B * 0.0721
```



L'interfaccia **ID3DXPRTEngine** viene ottenuta chiamando la funzione [**D3DXCreatePRTEngine**](d3dxcreateprtengine.md) .

Il tipo LPD3DXPRTENGINE è definito come puntatore all'interfaccia **ID3DXPRTEngine** .


```
typedef interface ID3DXPRTEngine ID3DXPRTEngine;
typedef interface ID3DXPRTEngine *LPD3DXPRTENGINE;
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

[**D3DXCreatePRTEngine**](d3dxcreateprtengine.md)
</dt> <dt>

[Trasferimento Radiance pre-calcolato (Direct3D 9)](precomputed-radiance-transfer.md)
</dt> </dl>

 

 
