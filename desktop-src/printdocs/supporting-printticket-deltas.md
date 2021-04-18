---
description: Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la specifica dello schema di stampa.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Supporto di Delta PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730c8d32d881dd30a6ab57b88d8fc1dfa87eee7a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321037"
---
# <a name="supporting-printticket-deltas"></a>Supporto di Delta PrintTicket

Questo argomento non è aggiornato. Per informazioni aggiornate, vedere la [specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

L'interfaccia del provider PrintTicket dispone di metodi che possono essere utilizzati per apportare modifiche incrementali a un oggetto PrintTicket esistente. Le modifiche del PrintTicket incrementale possono essere specificate in un oggetto PrintTicket parziale noto come Delta PrintTicket. Un oggetto PrintTicket modificato viene creato unendo un Delta PrintTicket con un oggetto PrintTicket esistente. Per ulteriori informazioni sui metodi che coinvolgono i Delta PrintTicket, vedere il documento di interfaccia del provider PrintTicket imminente.

Quando viene elaborato un Delta PrintTicket, è necessario eseguire i passaggi seguenti.

1.  Identificare le istanze di feature o ParameterInit comuni sia al PrintTicket esistente (il PrintTicket di destinazione) sia al Delta PrintTicket.

    -   Per ogni funzionalità comune sia per l'oggetto PrintTicket di destinazione che per il Delta PrintTicket, sostituire la funzionalità nel PrintTicket di destinazione con la caratteristica corrispondente nel Delta PrintTicket.

    -   Per ogni ParameterInit comune sia al PrintTicket di destinazione sia al Delta PrintTicket, sostituire ParameterInit nel PrintTicket di destinazione con il ParameterInit corrispondente nel Delta PrintTicket.

2.  Copiare tutte le istanze ParameterInit e della funzionalità rimanenti nel Delta PrintTicket nel PrintTicket di destinazione.

3.  Se l'algoritmo di risoluzione dei conflitti consente di specificare le priorità nel PrintTicket stesso, è possibile scegliere di elevare le priorità della funzionalità e delle istanze di ParameterInit denominate nel Delta PrintTicket.

4.  Eseguire la convalida PrintTicket come descritto nell' [elenco di controllo di convalida PrintTicket](printticket-validation-checklist.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



