---
title: Interfacce negli oggetti distribuiti
description: Nell'elaborazione distribuita un'interfaccia è una raccolta di definizioni e funzioni remote che consente a due o più programmi di interagire tra contesti diversi.
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- interfacce MIDL, in oggetti distribuiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cbee13dcbab9ccaa6ef6ad3ad3880daa9b14ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337286"
---
# <a name="interfaces-in-distributed-objects"></a>Interfacce negli oggetti distribuiti

Nell'elaborazione distribuita un'interfaccia è una raccolta di definizioni e funzioni remote che consente a due o più programmi di interagire tra contesti diversi. In un'applicazione RPC, un'interfaccia specifica:

-   Modo in cui le applicazioni client e server si identificano tra loro.
-   Modalità di trasmissione dei dati tra client e server.
-   Procedure remote che l'applicazione client può chiamare.
-   Tipi di dati per i parametri e valori restituiti delle procedure remote.

Il Microsoft Interface Definition Language (MIDL) è per l'implementazione di interfacce utilizzate nelle applicazioni distribuite. Con MIDL, un'applicazione può disporre di un'interfaccia o di molti. Ogni interfaccia specifica un contratto distribuito univoco tra i programmi client e server. Le applicazioni basate su RPC (Remote Procedure Call), Component Object Model (COM) e Distributed Component Object Model (DCOM) specificano le interfacce usando MIDL.

MIDL è simile a C e C++ in molti modi. Per una panoramica sulla scrittura di interfacce MIDL, vedere [sviluppo dell'interfaccia](/windows/desktop/Rpc/developing-the-interface).

 

 