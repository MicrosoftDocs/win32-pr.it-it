---
title: Funzione Sample(S,float,int,float,uint) (riferimento HLSL)
description: Campionare un oggetto Texture2D con un valore facoltativo per stringere i valori di livello di dettaglio (LOD) del campione e restituisce lo stato dell'operazione.
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
ms.openlocfilehash: 648897a4e2250e0b91544676a3469b2d29402c757bcc77b2285d0181ca2fa5f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986211"
---
# <a name="samplesfloatintfloatuint-function-hlsl-reference"></a>Funzione Sample(S,float,int,float,uint) (riferimento HLSL)

Campionare [**un oggetto Texture2D**](sm5-object-texture2d.md) con un valore facoltativo per stringere i valori di livello di dettaglio (LOD) del campione e restituisce lo stato dell'operazione.

> [!Note]  
> Richiede [il modello shader 5 o](d3d11-graphics-reference-sm5.md) versione successiva.

 

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

Stato [del campionatore.](dx-graphics-hlsl-sampler.md) Si tratta di un oggetto dichiarato in un file degli effetti che contiene assegnazioni di stato.

</dd> <dt>

*Località* \[ Pollici\]
</dt> <dd>

Coordinate di trama. Il tipo di argomento dipende dal tipo di oggetto trama.



| tipo Texture-Object                    | Tipo di parametro |
|----------------------------------------|----------------|
| Texture1D                              | float          |
| Texture1DArray, Texture2D              | float2         |
| Texture2DArray, Texture3D, TextureCube | float3         |
| TextureCubeArray                       | float4         |



 

</dd> <dt>

*Offset* \[ Pollici\]
</dt> <dd>

Offset facoltativo delle coordinate della trama, che può essere usato per qualsiasi tipo di oggetto trama. L'offset viene applicato alla posizione prima del campionamento. Gli offset di trama devono essere statici. Il tipo di argomento dipende dal tipo di oggetto trama. Per altre informazioni, vedere [Applicazione degli offset delle coordinate di trama.](dx-graphics-hlsl-to-sample.md)



| tipo Texture-Object           | Tipo di parametro |
|-------------------------------|----------------|
| Texture1D, Texture1DArray     | int            |
| Texture2D, Texture2DArray     | int2           |
| Texture3D                     | int3           |
| TextureCube, TextureCubeArray | non supportato  |



 

</dd> <dt>

*Clamp* \[ Pollici\]
</dt> <dd>

Valore facoltativo a cui stringere i valori LOD di esempio. Ad esempio, se si passa 2.0f per il valore clamp, si garantisce che nessun singolo campione accerta un livello mip inferiore a 2,0f.

</dd> <dt>

*Stato* \[ Cambio\]
</dt> <dd>

Stato dell'operazione. Non è possibile accedere direttamente allo stato. passare invece lo stato alla [**funzione intrinseca CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** restituisce **TRUE** se tutti i valori dell'operazione **Sample**, **Gather** o **Load** corrispondenti hanno eseguito l'accesso ai riquadri mappati in una [risorsa affiancata.](/windows/desktop/direct3d11/direct3d-11-2-features) Se sono stati prelevati valori da un riquadro non mappato, **CheckAccessFullyMapped** restituisce **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Formato della trama, ovvero uno dei valori tipi di dati elencati in [**FORMATO DXGI. \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

## <a name="remarks"></a>Commenti

Il campionamento trame usa la posizione del texel per cercare un valore texel. È possibile applicare un offset alla posizione prima della ricerca. Lo stato del campionatore contiene le opzioni di campionamento e filtro. Questo metodo può essere richiamato all'interno di pixel shader, ma non è supportato in un vertex shader o in un geometry shader.

Usare un offset solo in corrispondenza di un valore integer miplevel; In caso contrario, è possibile ottenere risultati diversi a seconda dell'implementazione dell'hardware o delle impostazioni del driver.

### <a name="calculating-texel-positions"></a>Calcolo delle posizioni di Texel

Le coordinate della trama sono valori a virgola mobile che fanno riferimento ai dati della trama, noto anche come spazio di trama normalizzato. Le modalità di ritorno a capo degli indirizzi vengono applicate in questo ordine (coordinate della trama + offset + modalità di ritorno a capo) per modificare le coordinate della trama al di fuori \[ dell'intervallo 0...1. \]

Per le matrici di trame, un valore aggiuntivo nel parametro location specifica un indice in una matrice di trame. Questo indice viene considerato come un valore float ridimensionato (anziché come spazio normalizzato per le coordinate di trama standard). La conversione in un indice integer viene eseguita nell'ordine seguente (float + round-to-nearest-even integer + clamp nell'intervallo di matrici).

### <a name="applying-texture-coordinate-offsets"></a>Applicazione degli offset delle coordinate di trama

Il parametro offset modifica le coordinate della trama, nello spazio texel. Anche se le coordinate della trama sono numeri a virgola mobile normalizzati, l'offset applica un offset intero. Si noti anche che gli offset di trama devono essere statici.

Il formato dei dati restituito è determinato dal formato della trama. Ad esempio, se la risorsa trama è stata definita con il formato DXGI \_ FORMAT A8B8G8R8 UNORM SRGB, l'operazione di campionamento converte i texel campionati da \_ \_ gamma 2.0 a 1.0, filtra e scrive il risultato come valore a virgola mobile nell'intervallo \_ \[ 0..1. \]

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Metodi di esempio](texture-sample-overload.md)
</dt> <dt>

[Oggetto Texture](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 
