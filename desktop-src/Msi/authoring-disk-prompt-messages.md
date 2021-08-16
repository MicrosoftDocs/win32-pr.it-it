---
description: Usare le linee guida seguenti per creare un Windows installazione del programma di installazione che visualizza una finestra di messaggio che richiede all'utente di inserire un disco.
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Creazione di messaggi di richiesta del disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a27b324600b7098c4b11dd94528ce0f3aa624e6859df8d02ef43ee90d632068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381377"
---
# <a name="authoring-disk-prompt-messages"></a>Creazione di messaggi di richiesta del disco

Usare le linee guida seguenti per creare un Windows installazione del programma di installazione che visualizza una finestra di messaggio che richiede all'utente di inserire un disco.

**Per visualizzare una finestra di messaggio che richiede all'utente di inserire un disco**

1.  Usare le funzionalità di creazione del programma di installazione per impostare la stringa della proprietà [**DiskPrompt**](diskprompt.md) nella [tabella Property.](property-table.md) Deve includere il nome del prodotto da installare e un parametro segnaposto all'interno della stringa per il titolo stampato sul disco. Ad esempio, per Microsoft Publisher la proprietà **DiskPrompt** potrebbe essere "Microsoft Publisher: Disco \[ 1", dove 1 è il segnaposto per il titolo \] del \[ \] disco.
2.  Immettere i titoli di ogni disco richiesto in righe separate della colonna DiskPrompt della [tabella Media.](media-table.md) Ad esempio, la prima e l'unica voce nella tabella Media potrebbero essere "1-Install".
3.  Durante [l'azione InstallFiles](installfiles-action.md) il valore della colonna DiskPrompt della tabella [Media](media-table.md) viene sostituito con il segnaposto nella stringa della [**proprietà DiskPrompt.**](diskprompt.md)
4.  Il messaggio visualizzato dalla finestra di messaggio viene creato da una stringa di modello incorporata nella [tabella Error](error-table.md). Si tratta dell'errore 1302 e la stringa del modello è: "Please insert the disk: 2" (Inserire il disco: 2) e 2 rappresenta un segnaposto per la \[ \] proprietà \[ \] [**DiskPrompt.**](diskprompt.md)

Nell'esempio viene visualizzato il messaggio seguente all'utente: "Please insert the disk: Microsoft Publisher: Disk 1 – Install".

Si noti che i messaggi di richiesta del disco vengono visualizzati da [Interfaccia utente livelli tranne](user-interface-levels.md) Nessuno.

 

 



