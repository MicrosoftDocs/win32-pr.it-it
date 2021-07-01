---
title: GetDimensions (oggetto Texture HLSL DirectX)
description: Ottiene informazioni sulle dimensioni della trama. Il blocco di sintassi mostra tutti i parametri possibili nella dichiarazione del metodo. La tabella nella sezione Osservazioni mostra i parametri implementati per ogni tipo di oggetto trama.
ms.assetid: b72e54da-382a-4b90-bbfe-0b32effc7c05
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bb6ef3c35af60ea776622718099acdedb5188ba8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119837"
---
# <a name="getdimensions-directx-hlsl-texture-object"></a>GetDimensions (oggetto Texture HLSL DirectX)

Ottiene informazioni sulle dimensioni della trama. Il blocco di sintassi mostra tutti i parametri possibili nella dichiarazione del metodo. La tabella nella sezione Osservazioni mostra i parametri implementati per ogni tipo di oggetto trama.

void Object.GetDimensions( UINT MipLevel, typeX Width, typeX Height, typeX Elements, typeX Depth, typeX NumberOfLevels, typeX NumberOfSamples );



 

typeX indica che esistono due tipi possibili: **uint** o **float.**

## <a name="parameters"></a>Parametri



| Elemento                                                                                                                               | Descrizione                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Oggetto*<br/>                                     | Qualsiasi [tipo di oggetto trama](dx-graphics-hlsl-to-type.md) ad eccezione di un oggetto **Buffer.**<br/>                                       |
| <span id="MipLevel"></span><span id="miplevel"></span><span id="MIPLEVEL"></span>*MipLevel*<br/>                             | \[in \] Un indice in base zero che identifica il livello mipmap. Se questo argomento non viene usato, viene usato il primo livello mip.<br/> |
| <span id="Width"></span><span id="width"></span><span id="WIDTH"></span>*Larghezza*<br/>                                         | \[out \] Larghezza della trama, in texel.<br/>                                                                                     |
| <span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>*Altezza*<br/>                                     | \[out \] Altezza della trama, in texel.<br/>                                                                                    |
| <span id="Elements"></span><span id="elements"></span><span id="ELEMENTS"></span>*Elementi*<br/>                             | \[out \] Numero di elementi in una matrice.<br/>                                                                               |
| <span id="Depth"></span><span id="depth"></span><span id="DEPTH"></span>*Profondità*<br/>                                         | \[out \] Profondità della trama, in texel.<br/>                                                                                     |
| <span id="NumberOfLevels"></span><span id="numberoflevels"></span><span id="NUMBEROFLEVELS"></span>*NumberOfLevels*<br/>     | \[out \] Numero di livelli mipmap.<br/>                                                                                      |
| <span id="NumberOfSamples"></span><span id="numberofsamples"></span><span id="NUMBEROFSAMPLES"></span>*NumberOfSamples*<br/> | \[out \] Numero di campioni.<br/>                                                                                            |



 

## <a name="return-value"></a>Valore restituito

Nessuno

## <a name="overloaded-methods"></a>Metodi di overload

In questa tabella sono elencate tutte le diverse versioni del metodo . le versioni differiscono per il numero di parametri di input. Si noti che per ogni metodo che accetta parametri integer, esiste un metodo di overload che accetta parametri a virgola mobile.



| tipo Texture-Object | Parametri di input                                                               |
|---------------------|--------------------------------------------------------------------------------|
| Texture1D           | UINT MipLevel, UINT Width, UINT NumberOfLevels                                 |
| Texture1D           | Larghezza UINT                                                                     |
| Texture1D           | UINT MipLevel, float Width, float NumberOfLevels                               |
| Texture1D           | Float Width                                                                    |
| Texture1DArray      | UINT MipLevel, UINT Width, UINT Elements, UINT NumberOfLevels                  |
| Texture1DArray      | Larghezza UINT, elementi UINT                                                      |
| Texture1DArray      | UINT MipLevel, float Width, float Elements, float NumberOfLevels               |
| Texture1DArray      | float Width, float Elements                                                    |
| Texture2D           | UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels                    |
| Texture2D           | Larghezza UINT, Altezza UINT                                                        |
| Texture2D           | UINT MipLevel, float Width, float Height, float NumberOfLevels                 |
| Texture2D           | float Width, float Height                                                      |
| Texture2DArray      | UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels     |
| Texture2DArray      | Larghezza UINT, Altezza UINT, Elementi UINT                                         |
| Texture2DArray      | UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels |
| Texture2DArray      | Float Width, float Height, float Elements                                      |
| Texture3D           | UINT MipLevel, UINT Width, UINT Height, UINT Depth, UINT NumberOfLevels        |
| Texture3D           | Larghezza UINT, Altezza UINT, Profondità UINT                                            |
| Texture3D           | UINT MipLevel, float Width, float Height, float Depth, float NumberOfLevels    |
| Texture3D           | float Width, float Height, float Depth                                         |
| TextureCube         | UINT MipLevel, UINT Width, UINT Height, UINT NumberOfLevels                    |
| TextureCube         | Larghezza UINT, Altezza UINT                                                        |
| TextureCube         | UINT MipLevel, float Width, float Height, UINT NumberOfLevels                  |
| TextureCube         | float Width, float Height                                                      |
| TextureCubeArray    | UINT MipLevel, UINT Width, UINT Height, UINT Elements, UINT NumberOfLevels     |
| TextureCubeArray    | Larghezza UINT, Altezza UINT, Elementi UINT                                         |
| TextureCubeArray    | UINT MipLevel, float Width, float Height, float Elements, float NumberOfLevels |
| TextureCubeArray    | Float Width, float Height, float Elements                                      |
| Texture2DMS         | Esempi di UINT Width, UINT Height, UINT                                          |
| Texture2DMS         | Esempi di float Width, float Height, float                                       |
| Texture2DMSArray    | Larghezza UINT, Altezza UINT, Elementi UINT, Esempi UINT                           |
| Texture2DMSArray    | Float Width, float Height, float Elements, float Samples                       |



 

## <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

1.  Restituisce le dimensioni per il livello mipmap più grande (zero).
2.  TextureCubeArray è disponibile in Shader Model 4.1 o versione successiva.
3.  Shader Model 4.1 è disponibile in Direct3D 10.1 o versione successiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto texture](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





