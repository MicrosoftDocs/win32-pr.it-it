---
title: GetDimensions (oggetto trama DirectX HLSL)
description: Ottiene le informazioni sulle dimensioni della trama. Il blocco Syntax Mostra tutti i parametri possibili nella dichiarazione di metodo. La tabella nella sezione Osservazioni Mostra i parametri implementati per ogni tipo di oggetto trama.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ad4be68049c92955c5ddb06a0c5eccfe2c26b77
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857762"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a>GetDimensions (oggetto trama DirectX HLSL)

Ottiene le informazioni sulle dimensioni della trama. Il blocco Syntax Mostra tutti i parametri possibili nella dichiarazione di metodo. La tabella nella sezione Osservazioni Mostra i parametri implementati per ogni tipo di oggetto trama.



|                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------|
| void Object. GetDimensions (UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples); |



 

typeX indica che esistono due tipi possibili: **uint** o **float**.

## <a name="parameters"></a>Parametri



| Elemento                                                                                                                               | Descrizione                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Oggetto*<br/>                                     | Qualsiasi tipo [di oggetto trama](dx-graphics-hlsl-to-type.md) ad eccezione di un oggetto **buffer** .<br/>                                       |
| <span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*<br/>                             | \[in \] un indice in base zero che identifica il livello di mipmap. Se questo argomento non viene utilizzato, si presuppone il primo livello MIP.<br/> |
| <span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Larghezza*<br/>                                         | \[\]larghezza della trama, in Texel.<br/>                                                                                     |
| <span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Altezza*<br/>                                     | \[\]altezza della trama, in Texel.<br/>                                                                                    |
| <span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elementi*<br/>                             | \[\]numero di elementi in una matrice.<br/>                                                                               |
| <span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Profondità*<br/>                                         | \[\]profondità della trama, in Texel.<br/>                                                                                     |
| <span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*<br/>     | \[\]il numero di livelli di mipmap.<br/>                                                                                      |
| <span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*<br/> | \[\]numero di campioni.<br/>                                                                                            |



 

## <a name="return-value"></a>Valore restituito

nessuno

## <a name="overloaded-methods"></a>Metodi di overload

In questa tabella sono elencate tutte le diverse versioni del metodo. le versioni variano in base al numero di parametri di input. Si noti che per ogni metodo che accetta parametri Integer esiste un metodo di overload che accetta parametri a virgola mobile.



| Tipo di Texture-Object | Parametri di input                                                               |
|---------------------|--------------------------------------------------------------------------------|
| Texture1D           | UINT MipLevel, UINT Width, UINT NumberOfLevels                                 |
| Texture1D           | Lunghezza UINT                                                                     |
| Texture1D           | UINT MipLevel, float width, float NumberOfLevels                               |
| Texture1D           | Larghezza float                                                                    |
| Texture1DArray      | UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels                  |
| Texture1DArray      | Lunghezza UINT, elementi UINT                                                      |
| Texture1DArray      | UINT MipLevel, float width, float Elements, float NumberOfLevels               |
| Texture1DArray      | float width, float Elements                                                    |
| Texture2D           | UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels                    |
| Texture2D           | Lunghezza UINT, altezza UINT                                                        |
| Texture2D           | UINT MipLevel, float width, float height, float NumberOfLevels                 |
| Texture2D           | Larghezza float, altezza float                                                      |
| Texture2DArray      | UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels     |
| Texture2DArray      | Lunghezza UINT, altezza UINT, elementi UINT                                         |
| Texture2DArray      | UINT MipLevel, float width, float height, float Elements, float NumberOfLevels |
| Texture2DArray      | Spessore float, altezza float, elementi float                                      |
| Texture3D           | UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels        |
| Texture3D           | Lunghezza UINT, altezza UINT, profondità UINT                                            |
| Texture3D           | UINT MipLevel, float width, float height, float Depth, float NumberOfLevels    |
| Texture3D           | Larghezza float, altezza float, profondità a virgola mobile                                         |
| TextureCube         | UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels                    |
| TextureCube         | Lunghezza UINT, altezza UINT                                                        |
| TextureCube         | UINT MipLevel, float width, float height, UINT NumberOfLevels                  |
| TextureCube         | Larghezza float, altezza float                                                      |
| TextureCubeArray    | UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels     |
| TextureCubeArray    | Lunghezza UINT, altezza UINT, elementi UINT                                         |
| TextureCubeArray    | UINT MipLevel, float width, float height, float Elements, float NumberOfLevels |
| TextureCubeArray    | Spessore float, altezza float, elementi float                                      |
| Texture2DMS         | UINT Width, UINT Height, UINT Samples                                          |
| Texture2DMS         | float width, float height, float Samples                                       |
| Texture2DMSArray    | Lunghezza UINT, altezza UINT, elementi UINT, esempi UINT                           |
| Texture2DMSArray    | float width, float height, float Elements, float Samples                       |



 

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  Restituisce le dimensioni per il livello mipmap più grande (zero).
2.  TextureCubeArray è disponibile nel modello Shader 4,1 o versione successiva.
3.  Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Texture-oggetto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





