---
description: Strutture SOCKADDR e presupposti per l'ordinamento di byte in Winsock.
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: Presupposti per l'ordinamento di byte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe6abf9ed46302bd037d1eb130b18c5568518cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307036"
---
# <a name="byte-ordering-assumptions"></a>Presupposti per l'ordinamento di byte

Un provider di servizi deve considerare tutti i componenti [**sockaddr**](sockaddr-2.md) esclusivi del parametro della famiglia di indirizzi come se fossero nell'ordine dei byte di rete e il parametro della famiglia di indirizzi come nell'ordine dei byte del computer locale. È responsabilità dell'applicazione Winsock verificare che gli indirizzi contenuti nelle strutture **sockaddr** siano disposti correttamente. L'API Winsock fornisce diverse routine di conversione per semplificare questa attività. Attualmente queste routine comprendono la conversione tra l'ordine dei byte naturale dell'host locale e l'ordine dei byte di rete big endian o little-endian. L'architettura Winsock può supportare altri schemi di ordinamento dei byte in futuro.

 

 



