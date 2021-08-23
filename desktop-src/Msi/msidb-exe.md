---
description: Msidb.exe usa MsiDatabaseImport e MsiDatabaseExport per importare ed esportare flussi e tabelle di database.
ms.assetid: 2eee535f-e7f6-4e1a-9667-df4b8067b132
title: Msidb.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71bff646ae3e933be5dbe37a774b72c10a0183fe9c793305292c9a11c4f417be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012930"
---
# <a name="msidbexe"></a>Msidb.exe

Msidb.exe usa [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) e [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) per importare ed esportare flussi e tabelle di [database.](database-tables.md)

Se l'elenco di modalità, cartella, database e tabella viene specificato nella riga di comando, Msidb.exe non attiva alcuna interfaccia utente e opera come utilità della riga di comando invisibile all'utente adatta per lo script di compilazione.

## <a name="syntax"></a>Sintassi

**MsiDb** *{option}***...** _{opzione}_* _..._ * *{table}***...** _{table}_

## <a name="command-line-options"></a>Opzioni da riga di comando

Msidb.exe usa le opzioni della riga di comando seguenti senza distinzione tra maiuscole e minuscole. È anche possibile usare un delimitatore barra al posto di un trattino.



| Opzione | Descrizione                                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -i     | Importare file di archivio di testo dalla cartella nel database. I nomi di tabella per l'importazione sono nomi di file di 8 caratteri con estensione "idt". I nomi più lunghi vengono troncati a 8 caratteri se forniti dal comando per l'importazione. È possibile usare specifiche di caratteri jolly standard.                                                                 |
| -E     | Esportare le tabelle selezionate dal database in file di archivio di testo nella cartella . I nomi di tabella per l'esportazione sono nomi di tabella. È possibile usare solo la specifica \* con caratteri jolly, "". Le tabelle possono essere esportate da un database di sola lettura.                                                                                                               |
| -c     | Crea un nuovo file di database e importa le tabelle. Sovrascrive un file di database esistente.                                                                                                                                                                                                                                               |
| -f     | Specifica la cartella contenente i file di archivio di testo per tabelle e flussi. Se la cartella contenente i file di archivio di testo non è specificata, l'utilità richiede all'utente la cartella.                                                                                                                                       |
| -d     | Percorso completo del file di database.                                                                                                                                                                                                                                                                                          |
| -M     | Percorso completo del database in cui eseguire il merge. Questa opzione è disponibile solo in modalità riga di comando invisibile all'utente. È possibile che si verifichino più istanze di questa opzione fino a un massimo di 10. Se il database non è specificato nella riga di comando, l'utilità richiede all'utente di specificare il database.                                       |
| -T     | Percorso completo della trasformazione da applicare. Questa opzione è disponibile solo in modalità riga di comando invisibile all'utente. È possibile che si verifichino più istanze di questa opzione fino a un massimo di 10.                                                                                                                                                     |
| -j     | Nome dell'archiviazione da rimuovere dal database. Questa opzione è disponibile solo in modalità riga di comando invisibile all'utente. È possibile che si verifichino più istanze di questa opzione fino a un massimo di 10.                                                                                                                                                             |
| -k     | Nome del flusso da rimuovere dal database. Questa opzione è disponibile solo in modalità riga di comando invisibile all'utente. È possibile che si verifichino più istanze di questa opzione fino a un massimo di 10.                                                                                                                                                                 |
| -X     | Nome del flusso da salvare in un file su disco nella directory corrente. Questa opzione è disponibile solo in modalità riga di comando invisibile all'utente. I flussi di dati binari vengono archiviati come file separati con estensione ".ibd". Il nome file binario usato è dati di chiave primaria per la riga contenente il flusso.                                                  |
| -w     | Nome dello spazio di archiviazione da salvare in un file su disco nella directory corrente. Questa opzione è disponibile solo in modalità riga di comando invisibile all'utente.                                                                                                                                                                                                         |
| -a     | Nome del file da aggiungere al database come flusso. Questa opzione è disponibile solo in modalità riga di comando invisibile all'utente. È possibile che si verifichino più istanze di questa opzione fino a un massimo di 10. I flussi di dati binari vengono archiviati come file separati con estensione ".ibd". Il nome file binario usato è dati di chiave primaria per la riga contenente il flusso. |
| -r     | Nome dello spazio di archiviazione da aggiungere al database come archivio secondario. Questa opzione è disponibile solo in modalità riga di comando invisibile all'utente. È possibile che si verifichino più istanze di questa opzione fino a un massimo di 10.                                                                                                                                                     |
| -S     | Tronca i nomi di tabella a 8 caratteri durante l'esportazione in un file con estensione idt. Il nome della tabella viene troncato a 8 caratteri e viene aggiunta l'estensione ".idt".                                                                                                                                                                                           |
| -?     | Visualizza la finestra di dialogo della Guida della riga di comando                                                                                                                                                                                                                                                                                               |



 

> [!Note]  
> Quando si usano nomi file lunghi con spazi, usare le virgolette. Ad esempio, per un database che si trova nella cartella "Documenti", specificarlo come "c: \\ documenti".

 

Questo strumento è disponibile solo in componenti Windows [SDK per sviluppatori Windows Programma di installazione](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Strumenti di sviluppo del programma di installazione](windows-installer-development-tools.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



