---
title: Creazione di dischi con più sessioni
description: IMAPi è in grado di creare dischi dati multisessione. Quando si crea un disco a più sessioni, è necessario tenere presenti alcune considerazioni.
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc41dba861ce29bd3d3e25e33ba0ba5ab5bf38a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221270"
---
# <a name="creating-discs-with-multiple-sessions"></a>Creazione di dischi con più sessioni

IMAPi è in grado di creare dischi dati multisessione. Quando si crea un disco a più sessioni, è necessario tenere presenti alcune considerazioni.

Il metodo [**IDiscMaster:: SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) determina se è presente un disco MULTIsessione IMAPI nell'unità attiva al momento dell'impostazione. In tal caso, IMAPi passa automaticamente alla modalità multisessione. L'uso di [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) dopo che è stata stabilita la modalità multisessione causa la restituzione di una modalità a sessione singola da parte di IMAPI. Ciò significa che è necessario un disco vuoto per un'operazione di [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) Burn. Se il disco è in modalità multisessione, lo stesso disco deve trovarsi nel registratore attivo oppure verrà restituito un codice di errore IMAPi \_ e \_ WRONGDISC.

Selezionando un registratore nel formato Joliet, IMAPi leggerà le informazioni dal disco attualmente installato. Se il disco è un disco IMAPi Joliet precedente con spazio per un'altra sessione, IMAPi imposta automaticamente la modalità multisessione. Il disco deve essere presente nel registratore attivo quando si chiama [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).

La chiusura della prima sessione in un disco richiede 21 MB. Ogni sessione aggiuntiva richiede la chiusura di 11 MB.

 

 




