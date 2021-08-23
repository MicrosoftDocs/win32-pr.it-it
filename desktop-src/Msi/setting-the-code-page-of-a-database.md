---
description: Impostare sempre la tabella codici di un database prima di aggiungere informazioni di localizzazione.
ms.assetid: 0d8aee30-989a-4093-8718-1bb90029c0fb
title: Impostazione della tabella codici di un database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c9ac1840b624b821dff6a85bee94607cd9568dcd6bb9b01025cb02f87c5c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628541"
---
# <a name="setting-the-code-page-of-a-database"></a>Impostazione della tabella codici di un database

Impostare sempre la tabella codici di un database prima di aggiungere informazioni di localizzazione. Il tentativo di impostare la tabella codici dopo l'immissione di dati nel database non è consigliato perché potrebbe danneggiare i caratteri estesi. La localizzazione può essere notevolmente facilitata iniziando con un database indipendente dalla tabella codici. Per informazioni dettagliate, vedere [Creazione di un database con una tabella codici neutra.](creating-a-database-with-a-neutral-code-page.md) È possibile determinare la tabella codici corrente di un database come descritto in Determinazione della tabella codici di [un database di installazione.](determining-an-installation-database-s-code-page.md) Vedere [Localizzazione delle tabelle Error e ActionText per](localizing-the-error-and-actiontext-tables.md) un elenco di tabelle codici numeriche.

È possibile impostare la tabella codici di un database vuoto o di un database con una tabella codici neutra importando un file di archivio di testo con una tabella codici non neutra con [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). In questo modo la tabella codici del database viene impostata sulla tabella codici del file importato. Tutti i file di archivio successivamente importati nel database devono avere la stessa tabella codici del primo file. Se un file di archivio di testo viene esportato da un database, la tabella codici del file di archivio corrisponde al database padre. Vedere [Gestione delle tabelle codici delle tabelle importate ed esportate](code-page-handling-of-imported-and-exported-tables.md).

La tabella codici di qualsiasi database può essere impostata su una tabella codici numerica specificata usando [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) per importare un file di archivio di testo con il formato seguente: Due righe vuote; seguito da una riga contenente la tabella codici numerica, un delimitatore di tabulazione e la stringa esatta: \_ ForceCodepage. Si noti che con Windows 2000, tutte le stringhe nel database vengono convertite nella tabella codici \_ di ForceCodepage. Questa operazione può essere utile quando si localizza un database esistente e si traslano tutte le stringhe non neutre nella nuova tabella codici. Tuttavia, ciò causa un errore se il database contiene stringhe non neutre che non devono essere convertite.

L'WiLangId.vbs fornisce un esempio di come impostare la tabella codici di un pacchetto usando il [**metodo Import**](database-import.md). Una copia del WiLangId.vbs è disponibile in Windows Installer SDK. È possibile usare questa utilità per determinare le versioni della lingua supportate dal database (pacchetto), la lingua utilizzata dal programma di installazione per tutte le stringhe nell'interfaccia utente non scritte nel database (Product) o la singola tabella codici ANSI per il pool di stringhe (tabella codici). Per informazioni sull'uso WiLangId.vbs vedere la pagina della Guida: [Gestire la lingua e la tabella codici.](manage-language-and-codepage.md)

Per determinare i valori di Product, Package e Codepage, eseguire WiLangId.vbs come indicato di seguito.

**cscript wilangid.vbs** *\[ percorso del \] database*

Per impostare la tabella codici del pacchetto, eseguire la riga di comando seguente.

**cscript wilangid.vbs** *\[ percorso del \] valore* della **tabella codici del** *\[ database \]*

Ad esempio, per impostare la tabella codici di test.msi sul valore numerico della tabella codici ANSI 1252, eseguire la riga di comando seguente.

**cscript wilangid.vbs c: \\ temp \\test.msi Codepage 1252**

 

 



