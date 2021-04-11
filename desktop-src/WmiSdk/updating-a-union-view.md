---
description: È possibile aggiornare i valori delle proprietà colonne delle istanze della classe di visualizzazione Union. Le modifiche apportate all'istanza della classe di visualizzazione verranno propagate alle istanze della classe di origine che formano la classe di visualizzazione Unione.
ms.assetid: 375c9bc8-9f7b-42b4-a841-cf6af88887de
ms.tgt_platform: multiple
title: Aggiornamento di una visualizzazione Unione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b051147ab40aacbf9032c5a0998d5894148985c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130959"
---
# <a name="updating-a-union-view"></a>Aggiornamento di una visualizzazione Unione

È possibile aggiornare i valori delle proprietà colonne delle istanze della classe di visualizzazione Union. Le modifiche apportate all'istanza della classe di visualizzazione verranno propagate alle istanze della classe di origine che formano la classe di visualizzazione Unione.

Le restrizioni seguenti si applicano alle modifiche apportate alle istanze della classe di visualizzazione:

-   Non è possibile creare nuove istanze delle classi di visualizzazione.
-   Solo le classi Union supportano gli aggiornamenti. le viste join e Association creano istanze di visualizzazione di sola lettura.
-   Il completamento di un aggiornamento varia a seconda che un'istanza di origine sia aggiornabile. Se una proprietà di un'istanza di visualizzazione è mappata a una proprietà di sola lettura di un'istanza di origine, i tentativi di modificare la proprietà di visualizzazione hanno esito negativo.

 

 



