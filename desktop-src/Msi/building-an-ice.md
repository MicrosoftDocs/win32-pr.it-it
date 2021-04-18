---
description: Se non si riesce a trovare gli analizzatori di coerenza interni necessari tra le azioni personalizzate ICE elencate nella Guida di riferimento a ICE, sarà necessario preparare il proprio ghiaccio per convalidare il pacchetto.
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: Creazione di un ghiaccio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de8dab0284a612723461d11b420ed1f22b244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311007"
---
# <a name="building-an-ice"></a>Creazione di un ghiaccio

Se non si riesce a trovare gli [analizzatori di coerenza interni](internal-consistency-evaluators-ices.md) necessari tra le azioni personalizzate Ice elencate nella Guida di [riferimento a Ice](ice-reference.md), sarà necessario preparare il proprio ghiaccio per convalidare il pacchetto.

Quando si creano azioni personalizzate ICE, è necessario eseguire le operazioni seguenti:

-   Basare i ghiacci solo sulle azioni personalizzate dei tipi elencati nella tabella illustrata.
-   Chiamare [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e pubblicare un \_ tipo di messaggio utente INSTALLMESSAGE. Quando si creano i messaggi ICE, seguire il formato dei messaggi nelle [linee guida](ice-message-guidelines.md)per i messaggi di ghiaccio.
-   Scrivere il ghiaccio in modo che acquisisca eventuali errori dell'API e restituisca sempre l'errore \_ Success. Questa operazione è necessaria per consentire l'esecuzione di azioni personalizzate successive in seguito all'errore di un ghiaccio.

Le azioni personalizzate ICE sono limitate ai tipi di azione personalizzati seguenti.



| Tipo di azione personalizzata                                 | Descrizione               |
|----------------------------------------------------|---------------------------|
| [Tipo di azione personalizzata 1](custom-action-type-1.md)   | DLL nel flusso binario      |
| [Tipo di azione personalizzata 2](custom-action-type-2.md)   | EXE nel flusso binario      |
| [Tipo di azione personalizzata 5](custom-action-type-5.md)   | JScript nel flusso binario  |
| [Tipo di azione personalizzata 6](custom-action-type-6.md)   | VBScript nel flusso binario |
| [Tipo di azione personalizzata 37](custom-action-type-37.md) | Codice JScript come stringa    |
| [Tipo di azione personalizzata 38](custom-action-type-38.md) | Codice VBScript come stringa   |



 

Quando si crea un'azione personalizzata ICE, non eseguire le operazioni seguenti:

-   Non presupporre che l'handle del motore ricevuto dal ghiaccio sia un'istanza di installazione del database del programma di installazione. Se non si tratta di un'istanza di installazione, alcune proprietà non sono definite, le directory di origine e di destinazione non vengono risolte e gli Stati della funzionalità corrente non sono definiti.
-   Non fare affidamento sull'esecuzione precedente, o non sull'esecuzione, di qualsiasi azione del programma di installazione, azione personalizzata o un altro ghiaccio. Poiché un ghiaccio precedente potrebbe avere creato colonne temporanee in qualsiasi tabella, gli autori devono fare riferimento alle colonne in base al nome laddove possibile. I ghiacci devono eseguire la pulizia di eventuali colonne o tabelle temporanee prima di uscire.
-   Non presupporre che gli autori abbiano accesso a un'immagine della directory di origine del database.
-   Non presupporre che le modifiche apportate al database non vengano mantenute.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di ghiaccio in C++](sample-ice-in-c-.md)
</dt> <dt>

[Esempio di ghiaccio in VBScript](sample-ice-in-vbscript.md)
</dt> </dl>

 

 



