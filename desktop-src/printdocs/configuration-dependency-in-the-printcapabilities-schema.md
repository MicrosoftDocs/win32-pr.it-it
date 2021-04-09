---
title: Dipendenza della configurazione PrintCapabilities
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 9b1f3f49-2a4a-4413-9708-a430011314e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e7f376d8bd0dab823adb3a2e0665db27508b1d7
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103886048"
---
# <a name="configuration-dependency-in-the-printcapabilities-schema"></a>Dipendenza di configurazione nello schema PrintCapabilities

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Lo schema PrintCapabilities è strettamente parallelo al Framework dello schema di stampa, in termini di elementi utilizzati e della struttura generale espressa dagli elementi padre e figlio. Le dipendenze di configurazione, che riguardano in modo specifico l'elemento PrintCapabilities, sono elencate qui come un'estensione del framework generale. Le dipendenze di configurazione fanno riferimento al fatto che alcuni elementi, incluso il relativo contenuto, possono essere modificati o addirittura eliminati da un documento PrintCapabilities a quello successivo, in seguito a dipendenze dalla configurazione. Anche se è necessario che un elemento padre sia indipendente dalla configurazione, i relativi elementi figlio potrebbero avere dipendenze. Tali dipendenze vengono espresse utilizzando \* \* costrutti switch/case nei file GPD.

Come esempio di una dipendenza di configurazione, prendere in considerazione i valori associati a ogni proprietà nel documento PrintCapabilities. Ogni documento PrintCapabilities può variare nelle istanze di proprietà definite e nelle istanze di valore assegnate a tali istanze di proprietà.



| Tipo di elemento                                                                                                                                                                             | Dipendenza dalla configurazione                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funzionalità <br/> Opzione<br/> ParameterInit<br/> ParameterRef<br/> PrintCapabilities<br/> PrintTicket<br/> Proprietà<br/> ScoredProperty<br/> | Questi elementi non devono avere dipendenze di configurazione.<br/>                                                                                                                                                           |
| ParameterDef <br/>                                                                                                                                                                 | Gli elementi e gli elementi ParameterDef in essi contenuti in qualsiasi livello di annidamento non devono avere dipendenze di configurazione.<br/>                                                                                        |
| Proprietà <br/>                                                                                                                                                                     | Gli elementi Property possono avere dipendenze di configurazione, tranne quando vengono visualizzati all'interno di elementi ParameterDef.<br/>                                                                                                       |
| Valore <br/>                                                                                                                                                                        | Gli elementi valore visualizzati negli elementi ScoredProperty non devono avere dipendenze di configurazione. Gli elementi di valore visualizzati all'interno di un elemento Property possono avere dipendenze arbitrarie dalla configurazione.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




