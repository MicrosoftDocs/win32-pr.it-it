---
description: Msidb.exe utilizza MsiDatabaseImport e MsiDatabaseExport per importare ed esportare tabelle e flussi di database.
ms.assetid: 2eee535f-e7f6-4e1a-9667-df4b8067b132
title: Msidb.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86f2e1fa6a1cf1a9dc8a01b9f9d6542607dd9275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313809"
---
# <a name="msidbexe"></a>Msidb.exe

Msidb.exe utilizza [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) e [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) per importare ed esportare [tabelle](database-tables.md) e flussi di database.

Se la modalità, la cartella, il database e l'elenco tabella sono specificati nella riga di comando, Msidb.exe non consente di visualizzare alcuna interfaccia utente e funge da utilità da riga di comando invisibile all'utente adatta per lo script di compilazione.

## <a name="syntax"></a>Sintassi

**MsiDb** *{opzione} ***...** _{Option}_* _..._ * * {tabella} ***...** _{Table}_

## <a name="command-line-options"></a>Opzioni da riga di comando

Msidb.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole. Al posto di un trattino, può essere utilizzato anche un delimitatore di barra.



| Opzione | Descrizione                                                                                                                                                                                                                                                                                                                         |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -i     | Importa i file di archivio di testo dalla cartella nel database. I nomi di tabella per l'importazione sono nomi file di 8 caratteri con estensione "IDT". I nomi più lunghi vengono troncati a 8 caratteri se specificati dal comando per l'importazione. È possibile utilizzare le specifiche standard di tipo Wild Card.                                                                 |
| -E     | Esporta le tabelle selezionate dal database in file di archivio di testo nella cartella. I nomi di tabella per l'esportazione sono nomi di tabella. È possibile utilizzare solo la specifica con caratteri jolly " \* ". Le tabelle possono essere esportate da un database di sola lettura.                                                                                                               |
| -c     | Consente di creare un nuovo file di database e di importare le tabelle. Sovrascrive un file di database esistente.                                                                                                                                                                                                                                               |
| -f     | Specifica la cartella che contiene i file di archivio di testo per tabelle e flussi. Se la cartella contenente i file di archivio di testo non è specificata, l'utilità richiede all'utente la cartella.                                                                                                                                       |
| -d     | Percorso completo del file di database.                                                                                                                                                                                                                                                                                          |
| -M     | Percorso completo del database da unire in. Questa opzione è disponibile solo nella modalità riga di comando invisibile all'utente. Più istanze di questa opzione possono verificarsi a un massimo di 10. Se il database non è specificato nella riga di comando, l'utilità richiede all'utente il database.                                       |
| -T     | Percorso completo della trasformazione da applicare. Questa opzione è disponibile solo nella modalità riga di comando invisibile all'utente. Più istanze di questa opzione possono verificarsi a un massimo di 10.                                                                                                                                                     |
| -j     | Nome dello spazio di archiviazione da rimuovere dal database. Questa opzione è disponibile solo nella modalità riga di comando invisibile all'utente. Più istanze di questa opzione possono verificarsi a un massimo di 10.                                                                                                                                                             |
| -k     | Nome del flusso da rimuovere dal database. Questa opzione è disponibile solo nella modalità riga di comando invisibile all'utente. Più istanze di questa opzione possono verificarsi a un massimo di 10.                                                                                                                                                                 |
| -X     | Nome del flusso da salvare in un file su disco nella directory corrente. Questa opzione è disponibile solo nella modalità riga di comando invisibile all'utente. I flussi di dati binari vengono archiviati come file separati con estensione ". IBD". Il nome file binario utilizzato è costituito dai dati di chiave primaria per la riga contenente il flusso.                                                  |
| -w     | Nome dello spazio di archiviazione da salvare in un file su disco nella directory corrente. Questa opzione è disponibile solo nella modalità riga di comando invisibile all'utente.                                                                                                                                                                                                         |
| -a     | Nome del file da aggiungere al database come flusso. Questa opzione è disponibile solo nella modalità riga di comando invisibile all'utente. Più istanze di questa opzione possono verificarsi a un massimo di 10. I flussi di dati binari vengono archiviati come file separati con estensione ". IBD". Il nome file binario utilizzato è costituito dai dati di chiave primaria per la riga contenente il flusso. |
| -r     | Nome dello spazio di archiviazione da aggiungere al database come sottoarchivio. Questa opzione è disponibile solo nella modalità riga di comando invisibile all'utente. Più istanze di questa opzione possono verificarsi a un massimo di 10.                                                                                                                                                     |
| -S     | Troncare i nomi di tabella a 8 caratteri durante l'esportazione in un. IDT. Il nome della tabella è troncato a 8 caratteri e viene aggiunta l'estensione ". IDT".                                                                                                                                                                                           |
| -?     | Visualizza la finestra di dialogo della guida della riga di comando                                                                                                                                                                                                                                                                                               |



 

> [!Note]  
> Quando si usano nomi di file lunghi con spazi, racchiuderli tra virgolette. Per un database che si trova nella cartella "documenti", ad esempio, specificarlo come "c: \\ documenti".

 

Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di sviluppo Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



