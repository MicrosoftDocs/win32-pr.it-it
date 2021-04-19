---
description: L'azione InstallODBC installa driver, traduttori e origini dati nella tabella ODBCDriver, nella tabella ODBCTranslator e nella tabella ODBCDataSource.
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: Azione InstallODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5ac9becd2a528646805f4201cfb415a6bc61bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317757"
---
# <a name="installodbc-action"></a>Azione InstallODBC

L'azione InstallODBC installa driver, traduttori e origini dati nella tabella [ODBCDriver](odbcdriver-table.md), nella tabella [ODBCTranslator](odbctranslator-table.md)e nella [tabella ODBCDataSource](odbcdatasource-table.md). Se un driver o un convertitore esiste già, l'azione InstallODBC esegue le chiamate SQL necessarie per l'installazione.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione InstallODBC non copia o rimuove i file e deve essere eseguita in seguito a azioni che copiano o rimuovono i file.

## <a name="actiondata-messages"></a>Messaggi ActionData

Nella tabella seguente vengono identificati i messaggi ActionData per ogni driver installato.



| Campo       | Descrizione                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Descrizione del driver. Chiave del driver ODBC.                                 |
| \[2\]       | ComponentID.                                                             |
| \[3\]       | cartella.                                                                  |
| \[4, 5,...\] | Coppie di attributi e valori da [ODBCAttribute](odbcattribute-table.md). |



 

Nella tabella seguente vengono identificati i messaggi ActionData per ogni traduttore installato.



| Campo       | Descrizione                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Descrizione del driver. Chiave del driver ODBC.                                 |
| \[2\]       | ComponentID.                                                             |
| \[3\]       | cartella.                                                                  |
| \[4, 5,...\] | Coppie di attributi e valori da [ODBCAttribute](odbcattribute-table.md). |



 

Nella tabella seguente vengono identificati i messaggi ActionData per ogni origine dati installata.



| Campo       | Descrizione                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Descrizione del driver. Chiave del driver ODBC.                                 |
| \[2\]       | ComponentID.                                                             |
| \[3\]       | Registrazione: ODBC \_ Add \_ DSN o ODBC \_ Add \_ sys \_ DSN.                     |
| \[4, 5,...\] | Coppie di attributi e valori da [ODBCAttribute](odbcattribute-table.md). |



 

## <a name="remarks"></a>Commenti

È necessario che Gestione driver ODBC sia stato creato nel pacchetto di Microsoft Installer e che sia incluso un componente denominato ODBCDriverManager. Se necessario, il gestore viene installato.

Per rinominare il componente, impostare una proprietà denominata ODBCDriverManager sul nuovo nome del componente. Se è necessario installare una gestione driver ODBC a 64 bit, il componente che lo trasporta dovrebbe essere denominato ODBCDriverManager64.

-   L'azione InstallODBC esegue una query sulla [tabella ODBCDataSource](odbcdatasource-table.md) e sulla [tabella ODBCSourceAttribute](odbcsourceattribute-table.md) per ogni origine dati da installare e sugli attributi dell'origine dati.
-   L'azione InstallODBC esegue una query sulla [tabella ODBCDriver](odbcdriver-table.md) e sulla [tabella ODBCTranslator](odbctranslator-table.md) per ogni driver e convertitore selezionato per l'installazione.
-   L'azione InstallODBC esegue una query sulla [tabella ODBCAttribute](odbcattribute-table.md) per gli attributi dei driver e dei convertitori.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempi di Windows Installer](windows-installer-examples.md)
</dt> </dl>

 

 



