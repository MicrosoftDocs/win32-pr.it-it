---
title: GetSamplePosition (oggetto trama DirectX HLSL)
description: Ottiene la posizione dell'esempio specificato.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 95be6d9b6c4cbf70aed059399af0892a3c75f0a3462b6ef2b0732e8180f4e123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068111"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a>GetSamplePosition (oggetto trama DirectX HLSL)

Ottiene la posizione dell'esempio specificato.

ret Object.GetSamplePosition( int s );



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                           | Descrizione                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Oggetto*<br/> | Un tipo texture2DMS o Texture2DMSArray [texture-object.](dx-graphics-hlsl-to-type.md)<br/> |
| <span id="s"></span><span id="S"></span>*s*<br/>                                         | \[\]nell'indice di esempio in base zero.<br/>                                                      |



 

## <a name="return-value"></a>Valore restituito

Restituisce la posizione di esempio (x,y), un vettore a virgola mobile a due componenti.

## <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

-   Shader Model 4.1 è disponibile in Direct3D 10.1 o versione successiva.

## <a name="remarks"></a>Commenti

Un pixel shader può essere valutato alla frequenza di campionamento (eseguire un pixel shader una volta per campione) o alla frequenza dei pixel (eseguire una pixel shader una volta per pixel). Collegare la semantica SV SampleIndex a un input pixel shader per richiamare un pixel shader alla frequenza di campionamento, il valore di input viene quindi usato come indice di esempio durante il campionamento della destinazione \_ di rendering.

È possibile eseguire l'interpolazione pixel shader'input in diversi modi. Per eseguire l'interpolazione in:

-   Un pixel al centro, non usare alcuna semantica.
-   Un esempio, usare la semantica SV \_ SampleIndex.
-   Posizione centrale, usare il [ \_ modificatore centroid.](dx-graphics-hlsl-struct.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto texture](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





