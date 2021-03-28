---
title: RestartStrip (oggetto Stream-Output DirectX HLSL)
description: Termina la striscia primitiva corrente e avvia una nuova striscia. Se la striscia corrente non ha un numero sufficiente di vertici emessi per riempire la topologia primitiva, la primitiva incompleta alla fine verrà ignorata.
ms.assetid: ca8eb7cf-1b4a-4082-b768-01390c5f8b47
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 16b31bbd1e2f72ce6b31a0c079f7ec5739aba87a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993424"
---
# <a name="restartstrip-directx-hlsl-stream-output-object"></a>RestartStrip (oggetto Stream-Output DirectX HLSL)

Termina la striscia primitiva corrente e avvia una nuova striscia. Se la striscia corrente non ha un numero sufficiente di vertici emessi per riempire la topologia primitiva, la primitiva incompleta alla fine verrà ignorata.



|                 |
|-----------------|
| RestartStrip(); |



 

## <a name="parameters"></a>Parametri



| Elemento                                                                                     | Descrizione |
|------------------------------------------------------------------------------------------|-------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno**<br/> |             |



 

## <a name="return-value"></a>Valore restituito

nessuno

## <a name="remarks"></a>Osservazioni

Un taglio striscia causa la fine della striscia corrente e una nuova striscia da avviare. Una striscia può essere eseguita chiamando in modo esplicito questo metodo o semplicemente eseguendo il rendering fino al valore di indice massimo (1, ovvero 0xFFFFFFFF per gli indici a 32 bit o 0xFFFF per gli indici a 16 bit). Ogni istanza di un oggetto di estrazione con istanza indicizzata genera automaticamente uno strip Cut. Questo vale anche se la topologia non è una striscia di triangolo.

> [!Note]  
> Il supporto per il riavvio e il valore "Magic value" per un taglio sono disponibili solo su dispositivi di [livello funzionalità](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 o superiore.

 

L'output viene sempre considerato una striscia di triangolo. Per rendere l'output un elenco di triangolo, è necessario chiamare RestartStrip tra ogni triangolo. Le ventole del triangolo non sono supportate.

## <a name="minimum-shader-model"></a>Modello Shader minimo

Questa funzione è supportata nei modelli shader seguenti.



| Modello di shader                                              | Supportato |
|-----------------------------------------------------------|-----------|
| [Modello Shader 4](dx-graphics-hlsl-sm4.md)                | sì       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stream-oggetto di output](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

