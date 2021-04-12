---
title: Proprietà Message e Message Queue
description: Un messaggio dispone di proprietà che specificano un'etichetta, un corpo del messaggio e un numero di opzioni.
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0139a588b52f1de1de43d8ec50aebdaf57b995ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330951"
---
# <a name="message-and-message-queue-properties"></a>Proprietà Message e Message Queue

Un messaggio dispone di proprietà che specificano un'etichetta, un corpo del messaggio e un numero di opzioni. Le opzioni delle proprietà dei messaggi possono includere la qualità del servizio, la priorità, il journaling, la privacy e i livelli di autenticazione e la durata del messaggio. Nelle applicazioni di Accodamento messaggi convenzionali (non RPC), è possibile specificare queste proprietà chiamando le funzioni dell'API MSMQ o i metodi dell'oggetto COM, descritti nella documentazione di MSMQ SDK. Le applicazioni client RPC possono impostare determinate proprietà per le chiamate a procedure remote chiamando [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) e [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo). Una volta impostate, le proprietà rimangono attive per ogni messaggio fino a quando non vengono reimpostate dall'applicazione client.

Una coda di messaggi dispone di un proprio set di proprietà, oltre a quelle dei messaggi. Queste proprietà identificano in modo univoco una coda e definiscono la classe di servizio fornita dalla coda, i livelli di privacy e autenticazione necessari per i messaggi in questa coda e se i messaggi devono far parte di una transazione distribuita. Come per le proprietà dei messaggi, è possibile specificare le proprietà di una coda di messaggi chiamando le funzioni dell'API MSMQ o i metodi dell'oggetto COM, descritti nella documentazione di MSMQ. Tuttavia, un'applicazione server RPC può specificare le proprietà della propria coda di ricezione quando chiama [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) per stabilire l'associazione.

 

 




