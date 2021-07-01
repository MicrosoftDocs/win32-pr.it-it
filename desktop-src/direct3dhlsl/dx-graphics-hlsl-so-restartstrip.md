---
title: RestartStrip (oggetto Stream-Output DirectX HLSL)
description: Termina la striscia primitiva corrente e avvia una nuova striscia. Se la striscia corrente non ha un numero di vertici sufficiente per riempire la topologia primitiva, la primitiva incompleta alla fine verrà eliminata.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aafd6407d556a6d0b4269c38192107edbc7cb1fa
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120196"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a>RestartStrip (oggetto Stream-Output DirectX HLSL)

Termina la striscia primitiva corrente e avvia una nuova striscia. Se la striscia corrente non ha un numero di vertici sufficiente per riempire la topologia primitiva, la primitiva incompleta alla fine verrà eliminata.

RestartStrip();



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                     | Descrizione |
|------------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno**<br/> |             |



 

## <a name="return-value"></a>Valore restituito

nessuno

## <a name="remarks"></a>Osservazioni

Un taglio di strip determina la fine della striscia corrente e l'avvio di una nuova striscia. È possibile eseguire un strip cut chiamando in modo esplicito questo metodo o semplicemente effettuando il rendering fino al valore massimo dell'indice ( 1, che è 0xffffffff per indici a 32 bit o 0xffff per indici a 16 bit). Ogni istanza di un disegno con istanze indicizzate genera automaticamente un strip cut. Questo vale anche se la topologia non è una striscia a triangolo.

> [!Note]  
> Il supporto per il riavvio e l'1 [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) "valore magico" per un taglio sono disponibili solo nei dispositivi con livello di funzionalità 10.0 o versione successiva.

 

Si presuppone sempre che l'output sia una striscia triangolare. Per rendere l'output un elenco di triangoli, è necessario chiamare RestartStrip tra ogni triangolo. Le ventole a triangolo non sono supportate.

## <a name="minimum-shader-model"></a>Modello shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello shader 4](dx-graphics-hlsl-sm4.md)                | yes       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Modello shader 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Modello shader 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Oggetto stream-output](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

