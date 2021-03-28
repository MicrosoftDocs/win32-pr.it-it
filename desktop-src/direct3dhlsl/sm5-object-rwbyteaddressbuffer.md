---
title: RWByteAddressBuffer
description: Un buffer di lettura/scrittura che indicizza in byte.
ms.assetid: 8370c14c-5822-4240-942d-565aa223d48c
keywords:
- HLSL RWByteAddressBuffer
topic_type:
- apiref
api_name:
- RWByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d065926b0769e15284cbe705783be012d82554b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399053"
---
# <a name="rwbyteaddressbuffer"></a>RWByteAddressBuffer

Un buffer di lettura/scrittura che indicizza in byte.



| Metodo                                                                                          | Descrizione                         |
|-------------------------------------------------------------------------------------------------|-------------------------------------|
| [**GetDimensions**](sm5-object-rwbyteaddressbuffer-getdimensions.md)                           | Ottiene le dimensioni della risorsa.       |
| [**InterlockedAdd**](sm5-object-rwbyteaddressbuffer-interlockedadd.md)                         | Aggiunge, in modo atomico.                   |
| [**InterlockedAnd**](sm5-object-rwbyteaddressbuffer-interlockedand.md)                         | E, atomicamente.                   |
| [**InterlockedCompareExchange**](sm5-object-rwbyteaddressbuffer-interlockedcompareexchange.md) | Confronta e scambia, in modo atomico. |
| [**InterlockedCompareStore**](sm5-object-rwbyteaddressbuffer-interlockedcomparestore.md)       | Confronta e archivia in modo atomico.    |
| [**InterlockedExchange**](sm5-object-rwbyteaddressbuffer-interlockedexchange.md)               | Scambi, atomicamente.              |
| [**InterlockedMax**](sm5-object-rwbyteaddressbuffer-interlockedmax.md)                         | Trova il valore massimo, atomicamente.          |
| [**InterlockedMin**](sm5-object-rwbyteaddressbuffer-interlockedmin.md)                         | Trovare il minimo, atomicamente.           |
| [**Interblocco**](sm5-object-rwbyteaddressbuffer-interlockedor.md)                           | ORs, atomicamente.                    |
| [**InterlockedXor**](sm5-object-rwbyteaddressbuffer-interlockedxor.md)                         | XOR, atomicamente.                   |
| [**Caricamento**](rwbyteaddressbuffer-load.md)                                                        | Ottiene un valore.                     |
| [**Load2**](rwbyteaddressbuffer-load2.md)                                                      | Ottiene due valori.                    |
| [**Load3**](rwbyteaddressbuffer-load3.md)                                                      | Ottiene tre valori.                  |
| [**Load4**](rwbyteaddressbuffer-load4.md)                                                      | Ottiene quattro valori.                   |
| [**Store**](sm5-object-rwbyteaddressbuffer-store.md)                                           | Imposta un valore.                     |
| [**Archivio2**](sm5-object-rwbyteaddressbuffer-store2.md)                                         | Imposta due valori.                    |
| [**Store3**](sm5-object-rwbyteaddressbuffer-store3.md)                                         | Imposta tre valori.                  |
| [**Store4**](sm5-object-rwbyteaddressbuffer-store4.md)                                         | Imposta quattro valori.                   |



 

Gli oggetti RWByteAddressBuffer possono essere preceduti dalla classe di archiviazione **globallycoherent**. Questa classe di archiviazione causa barriere e sincronizzazioni di memoria per scaricare i dati nell'intera GPU, in modo che altri gruppi possano visualizzare le Scritture. Senza questo identificatore, una barriera di memoria o una sincronizzazione Scarica un UAV solo all'interno del gruppo corrente.

Il formato UAV associato a questa risorsa deve essere creato con il formato DXGI \_ R32 formato senza \_ \_ tipo.

Il UAV associato a questa risorsa deve essere stato creato con il [**\_ flag UAV del buffer D3D11 \_ \_ \_ RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).

È possibile utilizzare il tipo di oggetto **RWByteAddressBuffer** quando si utilizzano buffer non elaborati. Per altre informazioni sulla visualizzazione non elaborata dei buffer, vedere [visualizzazioni non elaborate dei buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questo oggetto è supportato nei modelli shader seguenti.



| Modello di shader                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | Supportato |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) e High shader Models Shader Model [4](dx-graphics-hlsl-sm4.md) (disponibile tramite l'API Direct3D 11 usando il livello di funzionalità 10,0 o 10,1 ([**D3D \_ feature \_ Level**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) \_ 10 \_ X) sui dispositivi che supportano compute shader. Per ulteriori informazioni sul supporto di compute shader nell'hardware di livello inferiore, vedere [Compute Shaders su hardware di livello inferiore](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).<br/> | sì       |



 

Questo oggetto è supportato per i tipi di shader seguenti:



| Vertice | Hull | Dominio | Geometria | Pixel | Calcolo |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

