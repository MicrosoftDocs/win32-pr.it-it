---
title: Funzione Sample (S, float, int, float, uint) (riferimento HLSL)
description: Esegue il campionamento di un Texture2D con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in e restituisce lo stato dell'operazione.
ms.assetid: 1B9F48C4-DDB9-4547-B4AF-81A3ADA44C3F
keywords:
- Funzione di esempio HLSL
topic_type:
- apiref
api_name:
- Sample
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b378cb4031acecb8e0018053c7547e1948cc3e6
ms.sourcegitcommit: 0d6365d4e852b09a9100d9cfb9a5334922ebf478
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/17/2020
ms.locfileid: "103735218"
---
# <a name="samplesfloatintfloatuint-function-hlsl-reference"></a>Funzione Sample (S, float, int, float, uint) (riferimento HLSL)

Esegue il campionamento di un [**Texture2D**](sm5-object-texture2d.md) con un valore facoltativo per bloccare i valori del livello di dettaglio (LOD) di esempio in e restituisce lo stato dell'operazione.

> [!Note]  
> Richiede il [modello di shader 5](d3d11-graphics-reference-sm5.md) o versione successiva.

 

## <a name="syntax"></a>Sintassi

``` syntax
DXGI_FORMAT Sample(
  in  SamplerState S,
  in  float Location,
  in  int Offset,
  in  float Clamp,
  out uint Status
);
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*S* \[ in\]
</dt> <dd>

[Stato del campionatore](dx-graphics-hlsl-sampler.md). Si tratta di un oggetto dichiarato in un file di effetti che contiene le assegnazioni di stato.

</dd> <dt>

*Posizione* \[ in\]
</dt> <dd>

Coordinate di trama. Il tipo di argomento dipende dal tipo di oggetto trama.



| Tipo di Texture-Object                    | Tipo di parametro |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Offset* \[ in\]
</dt> <dd>

Offset della coordinata di trama facoltativo che può essere usato per qualsiasi tipo di oggetto trama. l'offset viene applicato al percorso prima del campionamento. Gli offset della trama devono essere statici. Il tipo di argomento dipende dal tipo di oggetto trama. Per altre informazioni, vedere [applicazione degli offset delle coordinate di trama](dx-graphics-hlsl-to-sample.md).



| Tipo di Texture-Object           | Tipo di parametro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | INT            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | non supportato  |



 

</dd> <dt>

*Blocca* \[ in\]
</dt> <dd>

Valore facoltativo a cui bloccare i valori LOD di esempio. Se ad esempio si passa 2.0 f per il valore del morsetto, si garantisce che nessun singolo campione acceda a un livello MIP inferiore a 2.0 f.

</dd> <dt>

*Stato* \[ di out\]
</dt> <dd>

Stato dell'operazione. Non è possibile accedere direttamente allo stato; passare invece lo stato alla funzione intrinseca [**CheckAccessFullyMapped**](checkaccessfullymapped.md) . **CheckAccessFullyMapped** restituisce **true** se tutti i valori dell'operazione di **campionamento**, **raccolta** o **caricamento** corrispondente hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata](/windows/desktop/direct3d11/direct3d-11-2-features). Se sono stati ricavati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il formato di trama, che è uno dei valori tipizzati elencati [**nel \_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format).

## <a name="remarks"></a>Commenti

Il campionamento della trama usa la posizione di Texel per cercare un valore di Texel. Un offset può essere applicato alla posizione prima della ricerca. Lo stato del campionatore contiene le opzioni di campionamento e filtro. Questo metodo può essere richiamato all'interno di una pixel shader, ma non è supportato in un vertex shader o in un geometry shader.

Usare un offset solo in un miplevel Integer; in caso contrario, è possibile ottenere risultati diversi a seconda dell'implementazione dell'hardware o delle impostazioni del driver.

### <a name="calculating-texel-positions"></a>Calcolo delle posizioni di Texel

Le coordinate di trama sono valori a virgola mobile che fanno riferimento a dati di trama, noti anche come spazio di trama normalizzato. Le modalità di wrapping degli indirizzi vengono applicate in questo ordine (coordinate di trama + offset + modalità a capo) per modificare le coordinate di trama al di fuori dell' \[ intervallo 0... 1 \] .

Per le matrici di trama, un valore aggiuntivo nel parametro location specifica un indice in una matrice di trame. Questo indice viene considerato come valore float scalato, invece dello spazio normalizzato per le coordinate di trama standard. La conversione in un indice Integer viene eseguita nell'ordine seguente (float + round-to-more-even integer + Clamp nell'intervallo di matrici).

### <a name="applying-texture-coordinate-offsets"></a>Applicazione degli offset delle coordinate di trama

Il parametro offset modifica le coordinate di trama, nello spazio Texel. Anche se le coordinate di trama sono numeri a virgola mobile normalizzati, l'offset applica un offset intero. Si noti inoltre che gli offset della trama devono essere statici.

Il formato di dati restituito è determinato dal formato di trama. Se, ad esempio, la risorsa di trama è stata definita con il formato DXGI \_ \_ A8B8G8R8 \_ UNORM \_ sRGB format, l'operazione di campionamento converte i Texel campionati da gamma 2,0 a 1,0, filtra e scrive il risultato come valore a virgola mobile nell'intervallo \[ 0.. 1 \] .

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi di esempio](texture-sample-overload.md)
</dt> <dt>

[Texture-oggetto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
