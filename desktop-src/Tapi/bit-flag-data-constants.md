---
description: Per le costanti dati di flag di bit estendibili, un fornitore di provider di servizi può definire nuovi valori per i bit specificati.
ms.assetid: bf3ca2b0-a9fb-4e63-87de-6d5cbe5cd746
title: Bit-Flag costanti di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e7842c7054fb973e4159b281486e4f4326debf3178b340770c0be280c7d1620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118871506"
---
# <a name="bit-flag-data-constants"></a>Bit-Flag costanti di dati

Per le costanti dati di flag di bit estendibili, un fornitore di provider di servizi può definire nuovi valori per i bit specificati. Poiché la maggior parte delle costanti di flag di bit sono **DWORD,** un numero specifico di bit inferiori è in genere riservato per le estensioni comuni, mentre i bit superiori rimanenti sono disponibili per le estensioni specifiche del fornitore. I flag di bit comuni vengono assegnati a partire dal bit zero e le estensioni specifiche del fornitore devono essere assegnate dal bit 31 in basso. Questo schema offre la massima flessibilità nell'assegnazione di posizioni di bit alle estensioni comuni, anziché alle estensioni specifiche del fornitore. Un fornitore deve definire nuovi valori che sono estensioni naturali dei flag di bit definiti dall'API.

Le strutture di dati estendibili hanno un campo di dimensioni variabili riservato per l'uso specifico del dispositivo. Poiché le dimensioni del campo sono variabili, il provider di servizi decide la quantità di informazioni e interpretazione del campo. Un fornitore che definisce un campo specifico del dispositivo deve creare queste estensioni naturali della struttura di dati originale definita dall'API.

 

 



