---
title: Differenze di threading tra le versioni di Direct3D
description: Molti modelli di programmazione multithread utilizzano le primitive di sincronizzazione (ad esempio, mutex) per creare sezioni critiche e impedire l'accesso al codice da parte di più thread alla volta.
ms.assetid: 0c4f984e-4dd0-4714-b911-592ca86d5dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e99c68dbdba1d6f0cdd789f6ccac8b81d4ac03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399353"
---
# <a name="threading-differences-between-direct3d-versions"></a>Differenze di threading tra le versioni di Direct3D

Molti modelli di programmazione multithread utilizzano le primitive di sincronizzazione (ad esempio, mutex) per creare sezioni critiche e impedire l'accesso al codice da parte di più thread alla volta.

Tuttavia, i metodi di creazione delle risorse dell'interfaccia [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) sono stati progettati per essere rientranti, senza richiedere primitive di sincronizzazione e sezioni critiche. Di conseguenza, i metodi di creazione delle risorse sono efficienti e facili da utilizzare.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 11, 10 e 9:<br/> Per impostazione predefinita, Direct3D 11 è thread-safe e continua a consentire alle applicazioni di rifiutare esplicitamente l'uso di D3D11 per \_ creare un \_ dispositivo \_ SINGLETHREADED. Se le applicazioni non sono thread-safe, devono rispettare le regole di Threading. Il runtime sincronizza i thread per conto dell'applicazione consentendo l'esecuzione simultanea dei thread. Infatti, la sincronizzazione in Direct3D 11 è più efficiente rispetto all'uso del livello thread-safe in Direct3D 10.<br/> Direct3D 10 può supportare l'esecuzione di un solo thread alla volta. Direct3D 10 è completamente thread-safe e consente a un'applicazione di rifiutare esplicitamente tale comportamento usando D3D10 per \_ creare un \_ dispositivo a \_ \_ thread singolo. <br/> Direct3D 9 non prevede l'impostazione predefinita per thread-safe. Tuttavia, quando si chiama [**CreateDevice**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-createdevice) o [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) per creare un dispositivo, è possibile specificare il \_ flag multithreading D3DCREATE per rendere l'API Direct3D 9 thread-safe. Questo causa un sovraccarico significativo della sincronizzazione. Pertanto, non è consigliabile rendere l'API Direct3D 9 thread-safe perché le prestazioni possono essere ridotte.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[MultiThreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

