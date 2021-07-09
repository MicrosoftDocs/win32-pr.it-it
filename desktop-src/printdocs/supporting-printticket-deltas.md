---
description: Informazioni sul supporto dei delta PrintTicket. Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica dello schema di stampa.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Supporto dei delta di PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f72f82875d0207ed232f4db897c78295ce2ee0
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548780"
---
# <a name="supporting-printticket-deltas"></a>Supporto dei delta di PrintTicket

Questo argomento non è corrente. Per le informazioni più aggiornate, vedere Specifica [dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

L'interfaccia del provider PrintTicket include metodi che possono essere usati per apportare modifiche incrementali a un oggetto PrintTicket esistente. Le modifiche incrementali di PrintTicket possono essere specificate in un oggetto PrintTicket parziale noto come delta di PrintTicket. Un oggetto PrintTicket modificato viene creato unendo un delta PrintTicket con un oggetto PrintTicket esistente. Per altre informazioni sui metodi che coinvolgono i delta di PrintTicket, vedere il documento dell'interfaccia del provider PrintTicket.

Quando viene elaborato un delta PrintTicket, è necessario eseguire i passaggi seguenti.

1.  Identificare le istanze Feature o ParameterInit comuni sia all'oggetto PrintTicket esistente (PrintTicket di destinazione) che al delta PrintTicket.

    -   Per ogni funzionalità comune sia al valore PrintTicket di destinazione che al delta PrintTicket, sostituire la funzionalità nell'oggetto PrintTicket di destinazione con la funzionalità corrispondente nel delta PrintTicket.

    -   Per ogni ParameterInit comune sia al valore PrintTicket di destinazione che al delta PrintTicket, sostituire ParameterInit nell'oggetto PrintTicket di destinazione con il parametro ParameterInit corrispondente nel delta PrintTicket.

2.  Copiare tutte le istanze Feature e ParameterInit rimanenti nel delta PrintTicket nell'oggetto PrintTicket di destinazione.

3.  Se l'algoritmo di risoluzione dei conflitti consente di definire priorità in PrintTicket stesso, è possibile scegliere di elevare le priorità delle istanze Feature e ParameterInit denominate nel delta PrintTicket.

4.  Eseguire la convalida di PrintTicket come descritto in [Elenco di controllo per la convalida di PrintTicket](printticket-validation-checklist.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dello schema di stampa](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



