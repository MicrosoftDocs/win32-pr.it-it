---
title: Proprietà di messaggi e code di messaggi
description: Un messaggio ha proprietà che specificano un'etichetta, un corpo del messaggio e una serie di opzioni.
ms.assetid: d0c9126e-a2c6-4d70-b87a-154a570899fc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c18b3a4751cd3be4473067dd9ca5aca17717672e6b67b559c10c502513fa2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928110"
---
# <a name="message-and-message-queue-properties"></a>Proprietà di messaggi e code di messaggi

Un messaggio ha proprietà che specificano un'etichetta, un corpo del messaggio e una serie di opzioni. Le opzioni delle proprietà dei messaggi possono includere qualità del servizio, priorità, inserimento nel journal, privacy e livelli di autenticazione e la durata del messaggio. Nelle applicazioni di accodamento messaggi convenzionali (non RPC), queste proprietà vengono specificate chiamando le funzioni API MSMQ o i metodi degli oggetti COM, descritti nella documentazione di MSMQ SDK. Le applicazioni client RPC possono impostare determinate proprietà per le chiamate di procedura remota chiamando [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) e [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo). Una volta impostate, le proprietà rimangono effettive per ogni messaggio fino a quando non vengono reimpostate dall'applicazione client.

Una coda di messaggi ha un proprio set di proprietà, oltre a quelle dei messaggi. Queste proprietà identificano in modo univoco una coda e definiscono la classe di servizio fornita dalla coda, i livelli di privacy e autenticazione necessari per i messaggi in questa coda e se i messaggi devono far parte di una transazione distribuita. Come per le proprietà dei messaggi, è possibile specificare le proprietà di una coda di messaggi chiamando le funzioni API MSMQ o i metodi degli oggetti COM, descritti nella documentazione di MSMQ. Tuttavia, un'applicazione server RPC può specificare le proprietà della propria coda di ricezione quando chiama [**RpcServerUseProtseqEpEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqepex) per stabilire l'associazione.

 

 




