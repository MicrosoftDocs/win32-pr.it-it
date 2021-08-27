---
description: Strutture sockaddr e presupposti per l'ordinamento dei byte in Winsock.
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: Presupposti per l'ordinamento dei byte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21c1e680b0fe658994723b0a1d87c2a7d6adbf0a00a5452b185401b03099089
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097911"
---
# <a name="byte-ordering-assumptions"></a>Presupposti per l'ordinamento dei byte

Un provider di servizi deve considerare tutti i componenti [**sockaddr**](sockaddr-2.md) esclusivi del parametro della famiglia di indirizzi come se fossero nell'ordine dei byte di rete e il parametro della famiglia di indirizzi come nell'ordine dei byte del computer locale. È responsabilità dell'applicazione Winsock assicurarsi che gli indirizzi contenuti nelle strutture **sockaddr** siano disposti correttamente. L'API Winsock fornisce una serie di routine di conversione per semplificare questa attività. Attualmente queste routine comprendono la conversione tra l'ordine dei byte naturale dell'host locale e l'ordinamento dei byte di rete big-Endian o little-Endian. L'architettura Winsock può supportare altri schemi di ordinamento dei byte in futuro.

 

 



