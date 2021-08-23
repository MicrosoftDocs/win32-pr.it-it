---
description: Se non è possibile trovare gli analizzatori di coerenza interna necessari tra le azioni personalizzate ICE esistenti elencate nel riferimento ICE, è necessario preparare il proprio ICE per convalidare il pacchetto.
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: Creazione di un ice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b4b79ab8e17d53ccfb60484c0d307f668c44a7a0e530cf776b10e73a697541c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500766"
---
# <a name="building-an-ice"></a>Creazione di un ice

Se non è possibile [](internal-consistency-evaluators-ices.md) trovare gli analizzatori di coerenza interna necessari tra le azioni personalizzate ICE esistenti elencate in [Ice Reference](ice-reference.md), sarà necessario preparare il proprio ICE per convalidare il pacchetto.

Quando si crea un'azione personalizzata ICE, è necessario eseguire le operazioni seguenti:

-   Basare le ICE solo sulle azioni personalizzate dei tipi elencati nella tabella illustrata.
-   Chiamare [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) e pubblicare un tipo di messaggio INSTALLMESSAGE \_ USER. Quando si crea un messaggio ICE, seguire il formato del messaggio nelle [linee guida per i messaggi ICE.](ice-message-guidelines.md)
-   Scrivere il codice ICE in modo che acquisisca eventuali errori api e restituisca sempre ERROR \_ SUCCESS. Questa operazione è necessaria per consentire l'esecuzione di azioni personalizzate successive in seguito all'errore di un ice.

Le azioni personalizzate ICE sono limitate ai tipi di azione personalizzati seguenti.



| Tipo di azione personalizzata                                 | Descrizione               |
|----------------------------------------------------|---------------------------|
| [Tipo di azione personalizzata 1](custom-action-type-1.md)   | DLL nel flusso binario      |
| [Tipo di azione personalizzata 2](custom-action-type-2.md)   | EXE nel flusso binario      |
| [Tipo di azione personalizzata 5](custom-action-type-5.md)   | JScript nel flusso binario  |
| [Tipo di azione personalizzata 6](custom-action-type-6.md)   | VBScript nel flusso binario |
| [Tipo di azione personalizzata 37](custom-action-type-37.md) | JScript codice come stringa    |
| [Tipo di azione personalizzata 38](custom-action-type-38.md) | Codice VBScript come stringa   |



 

Quando si crea un'azione personalizzata ICE, non eseguire le operazioni seguenti:

-   Non presupporre che l'handle del motore ricevuto da ICE sia un'istanza di installazione del database del programma di installazione. Se non è un'istanza di installazione, alcune proprietà non sono definite, le directory di origine e di destinazione non vengono risolte e gli stati delle funzionalità correnti non sono definiti.
-   Non basarsi sull'esecuzione precedente o sulla mancata esecuzione di qualsiasi azione del programma di installazione, azione personalizzata o un'altra ice. Poiché un ice precedente potrebbe aver creato colonne temporanee in qualsiasi tabella, gli autori devono fare riferimento alle colonne in base al nome quando possibile. Prima di uscire, le tabelle o le colonne temporanee devono essere pulite.
-   Non presupporre che gli autori hanno accesso a un'immagine della directory di origine del database.
-   Non presupporre che le modifiche apportate al database non siano persistenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di ICE in C++](sample-ice-in-c-.md)
</dt> <dt>

[Esempio di ICE in VBScript](sample-ice-in-vbscript.md)
</dt> </dl>

 

 



