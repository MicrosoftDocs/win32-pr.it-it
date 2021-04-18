---
description: Per le costanti di dati dei flag di bit estendibili, un fornitore del provider di servizi può definire nuovi valori per i bit specificati.
ms.assetid: bf3ca2b0-a9fb-4e63-87de-6d5cbe5cd746
title: Costanti dati Bit-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238627505bf414ed0ab94ff2f5c35197705c91d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309975"
---
# <a name="bit-flag-data-constants"></a>Costanti dati Bit-Flag

Per le costanti di dati dei flag di bit estendibili, un fornitore del provider di servizi può definire nuovi valori per i bit specificati. Poiché la maggior parte delle costanti di flag di bit è **DWORD** s, un numero specifico di bit inferiori è generalmente riservato per le estensioni comuni, mentre i bit superiori rimanenti sono disponibili per le estensioni specifiche del fornitore. I flag di bit comuni sono assegnati dal bit zero e le estensioni specifiche del fornitore devono essere assegnate dal bit 31 verso il basso. Questo schema offre la massima flessibilità nell'assegnazione di posizioni di bit a estensioni comuni, anziché estensioni specifiche del fornitore. Si prevede che un fornitore definisca nuovi valori che sono estensioni naturali dei flag di bit definiti dall'API.

Le strutture di dati estendibili hanno un campo di dimensioni sempre più riservato per l'uso specifico del dispositivo. Poiché il campo è di dimensioni variabili, il provider di servizi decide la quantità di informazioni e l'interpretazione del campo. Si prevede che un fornitore che definisce un campo specifico del dispositivo renda le estensioni naturali della struttura di dati originale definita dall'API.

 

 



