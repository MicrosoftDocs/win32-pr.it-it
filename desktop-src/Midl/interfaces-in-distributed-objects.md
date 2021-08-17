---
title: Interfacce negli oggetti distribuiti
description: Nel calcolo distribuito, un'interfaccia è una raccolta di definizioni e funzioni remote che consente a due o più programmi di interagire tra contesti diversi.
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- interfacce MIDL , in oggetti distribuiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8661e7e07f08d35151afe8fb256539ed574b0a0162178e3a9e63dc8c43c59ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807138"
---
# <a name="interfaces-in-distributed-objects"></a>Interfacce negli oggetti distribuiti

Nel calcolo distribuito, un'interfaccia è una raccolta di definizioni e funzioni remote che consente a due o più programmi di interagire tra contesti diversi. In un'applicazione RPC un'interfaccia specifica:

-   Modalità di identificazione reciproca delle applicazioni client e server.
-   Modalità di trasmissione dei dati tra client e server.
-   Procedure remote che l'applicazione client può chiamare.
-   Tipi di dati per i parametri e valori restituiti delle procedure remote.

Il Microsoft Interface Definition Language (MIDL) è per l'implementazione di interfacce usate nelle applicazioni distribuite. Con MIDL, un'applicazione può avere una o più interfacce. Ogni interfaccia specifica un contratto distribuito univoco tra i programmi client e server. Le applicazioni basate su chiamate di procedura remota (RPC), Component Object Model (COM) e DCOM (Distributed Component Object Model) specificano le interfacce tramite MIDL.

MIDL è simile a C e C++ in molti modi. Per una panoramica della scrittura di interfacce MIDL, vedere [Sviluppo dell'interfaccia](/windows/desktop/Rpc/developing-the-interface).

 

 