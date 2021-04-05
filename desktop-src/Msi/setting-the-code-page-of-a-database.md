---
description: Impostare sempre la tabella codici di un database prima di aggiungere informazioni di localizzazione.
ms.assetid: 0d8aee30-989a-4093-8718-1bb90029c0fb
title: Impostazione della tabella codici di un database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef04c2969d0933c4601bbca2f3897d86de43a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753007"
---
# <a name="setting-the-code-page-of-a-database"></a>Impostazione della tabella codici di un database

Impostare sempre la tabella codici di un database prima di aggiungere informazioni di localizzazione. Il tentativo di impostare la tabella codici dopo l'immissione dei dati nel database non è consigliato perché potrebbe danneggiare i caratteri estesi. La localizzazione può essere molto semplificata iniziando con un database indipendente dalla tabella codici. Per informazioni dettagliate, vedere la pagina relativa alla [creazione di un database con una tabella codici indipendente](creating-a-database-with-a-neutral-code-page.md). È possibile determinare la tabella codici corrente di un database, come descritto in [determinazione della tabella codici di un database di installazione](determining-an-installation-database-s-code-page.md). Vedere [la pagina relativa alla localizzazione delle tabelle Error e ActionText](localizing-the-error-and-actiontext-tables.md) per un elenco di tabelle codici numeriche.

È possibile impostare la tabella codici di un database vuoto o di un database con una tabella codici neutra, importando un file di archivio di testo con una tabella codici non neutra con [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Questa operazione consente di impostare la tabella codici del database sulla tabella codici del file importato. Tutti i file di archivio successivamente importati nel database devono quindi avere la stessa tabella codici del primo file. Se un file di archivio di testo viene esportato da un database, la tabella codici del file di archivio corrisponde al database padre. Vedere [gestione di tabelle codici per le tabelle importate ed esportate](code-page-handling-of-imported-and-exported-tables.md).

La tabella codici di qualsiasi database può essere impostata su una tabella codici numerica specificata usando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) per importare un file di archivio di testo con il formato seguente: due righe vuote. seguito da una riga contenente la tabella codici numerici, un delimitatore di tabulazione e la stringa esatta: \_ ForceCodepage. Si noti che con Windows 2000, in questo modo tutte le stringhe nel database vengono convertite nella tabella codici di \_ ForceCodepage. Questa operazione può essere prevista durante la localizzazione di un database esistente e la conversione di tutte le stringhe non neutre nella nuova tabella codici. Tuttavia, questo genera un errore se il database contiene stringhe non neutre che non devono essere convertite.

L'utilità WiLangId.vbs fornisce un esempio di come impostare la tabella codici di un pacchetto usando il [**Metodo Import**](database-import.md). In Windows Installer SDK viene fornita una copia di WiLangId.vbs. È possibile utilizzare questa utilità per determinare le versioni della lingua supportate dal database (pacchetto), il linguaggio utilizzato dal programma di installazione per tutte le stringhe dell'interfaccia utente che non sono state create nel database (prodotto) o la singola tabella codici ANSI per il pool di stringhe (tabella codici). Per informazioni sull'utilizzo di WiLangId.vbs, vedere la pagina della Guida relativa alla [gestione della lingua e](manage-language-and-codepage.md)della tabella codici.

Per determinare i valori di Product, Package e CodePage, eseguire WiLangId.vbs come indicato di seguito.

percorso **wilangid.vbscscript** *\[ al database \]*

Per impostare la tabella codici del pacchetto, eseguire la riga di comando seguente.

**cscript wilangid.vbs** il *\[ percorso \]* del *\[ valore \]* della tabella **codici** del database

Ad esempio, per impostare la tabella codici di test.msi sul valore numerico ANSI 1252, eseguire la riga di comando seguente.

**cscript wilangid.vbs c: \\ temp \\test.msi tabella codici 1252**

 

 



