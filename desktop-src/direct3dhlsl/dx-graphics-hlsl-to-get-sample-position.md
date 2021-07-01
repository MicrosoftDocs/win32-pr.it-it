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
ms.openlocfilehash: 9a1e5f4dc71d5af2e7973ef180c919a49e65ef81
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118586"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a>GetSamplePosition (oggetto trama DirectX HLSL)

Ottiene la posizione dell'esempio specificato.

ret Object.GetSamplePosition( int s );



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                           | Descrizione                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Oggetto*<br/> | Tipo [texture-object](dx-graphics-hlsl-to-type.md) Texture2DMS o Texture2DMSArray.<br/> |
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

Un pixel shader può essere valutato alla frequenza di campionamento (eseguire un'pixel shader una volta per campione) o alla frequenza dei pixel (eseguire una pixel shader una volta per pixel). Collegare la semantica SV SampleIndex a un input pixel shader per richiamare un pixel shader alla frequenza di campionamento, il valore di input viene quindi usato come indice di esempio durante il campionamento della \_ destinazione di rendering.

È possibile eseguire l'interpolazione pixel shader'input in diversi modi. Per eseguire l'interpolazione in:

-   Un pixel al centro, non usare alcuna semantica.
-   Un esempio, usare la semantica SV \_ SampleIndex.
-   Posizione centrale, usare il [ \_ modificatore centroid.](dx-graphics-hlsl-struct.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto texture](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





