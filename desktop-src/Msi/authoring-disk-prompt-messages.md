---
description: Usare le linee guida seguenti per creare un'installazione di Windows Installer che visualizza una finestra di messaggio che richiede all'utente di inserire un disco.
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Creazione di messaggi di richiesta del disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f536a27c2adb5896992eb19a86bff64b9498d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311045"
---
# <a name="authoring-disk-prompt-messages"></a>Creazione di messaggi di richiesta del disco

Usare le linee guida seguenti per creare un'installazione di Windows Installer che visualizza una finestra di messaggio che richiede all'utente di inserire un disco.

**Per visualizzare una finestra di messaggio che richiede all'utente di inserire un disco**

1.  Utilizzare le funzionalità di creazione del programma di installazione per impostare la stringa di proprietà [**DiskPrompt**](diskprompt.md) nella tabella delle [Proprietà](property-table.md) . Deve includere il nome del prodotto da installare e un parametro segnaposto nella stringa per il titolo stampato sul disco. Per Microsoft Publisher, ad esempio, la proprietà **DiskPrompt** potrebbe essere "Microsoft Publisher: disk \[ 1 \] ", dove \[ 1 \] è il segnaposto per il titolo del disco.
2.  Immettere i titoli di ogni disco richiesto in righe separate della colonna DiskPrompt della tabella [media](media-table.md) . Ad esempio, la prima e unica voce nella tabella media potrebbe essere "1 – Install".
3.  Durante l'azione [InstallFiles](installfiles-action.md) , il valore della colonna DiskPrompt della tabella [supporti](media-table.md) sostituisce il segnaposto nella stringa della proprietà [**DiskPrompt**](diskprompt.md) .
4.  Il messaggio visualizzato dalla finestra di messaggio viene creato da una stringa di modello predefinita nella tabella degli [errori](error-table.md). Si tratta dell'errore 1302 e della stringa di modello: "inserire il disco: \[ 2 \] " e \[ 2 \] rappresenta un segnaposto per la proprietà [**DiskPrompt**](diskprompt.md) .

Nell'esempio viene visualizzato il messaggio seguente all'utente: "inserire il disco: Microsoft Publisher: disco 1 – install."

Si noti che i messaggi di richiesta del disco vengono visualizzati da tutti i [livelli di interfaccia utente](user-interface-levels.md) tranne nessuno.

 

 



