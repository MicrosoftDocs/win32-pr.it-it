---
title: GetSamplePosition (oggetto trama di DirectX HLSL)
description: Ottiene la posizione dell'esempio specificato.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 062bf08064faf112fdc1efe5b371fcad72efeeea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398200"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a>GetSamplePosition (oggetto trama di DirectX HLSL)

Ottiene la posizione dell'esempio specificato.



|                                        |
|----------------------------------------|
| RET Object. GetSamplePosition (int s); |



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                           | Descrizione                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Oggetto*<br/> | Un Texture2DMS o un tipo di [oggetto trama](dx-graphics-hlsl-to-type.md) Texture2DMSArray.<br/> |
| <span id="s"></span><span id="S"></span>*s*<br/>                                         | \[nell' \] indice di esempio in base zero.<br/>                                                      |



 

## <a name="return-value"></a>Valore restituito

Restituisce la posizione di esempio (x, y), un vettore a virgola mobile a due componenti.

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

-   Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.

## <a name="remarks"></a>Commenti

Un pixel shader può essere valutato in base alla frequenza di campionamento (eseguire una pixel shader una sola volta per campione) o alla frequenza in pixel (eseguire una pixel shader una volta per pixel). Per \_ richiamare una pixel shader a pixel shader una frequenza di campionamento, il valore di input viene quindi utilizzato come indice di esempio durante il campionamento della destinazione di rendering.

È possibile interpolare un input di pixel shader in diversi modi. Per interpolare:

-   Un pixel Center, non usare alcuna semantica.
-   Esempio, usare la \_ semantica SV SampleIndex.
-   Una posizione del centro, usare il modificatore di [ \_ baricentro](dx-graphics-hlsl-struct.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Texture-oggetto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





