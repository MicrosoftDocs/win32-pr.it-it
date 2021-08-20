---
description: L'azione InstallODBC installa i driver, i convertitori e le origini dati nella tabella ODBCDriver, nella tabella ODBCTranslator e nella tabella ODBCDataSource.
ms.assetid: fbcf1fdc-5aef-4431-93fe-3ed02748b5ff
title: Azione InstallODBC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a371aed67ec412c46946d7df7fd4775f0a0d4e20d91cbb60d69f894371f203ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142225"
---
# <a name="installodbc-action"></a>Azione InstallODBC

L'azione InstallODBC installa i driver, i convertitori e le origini dati nella tabella [ODBCDriver](odbcdriver-table.md), nella tabella [ODBCTranslator](odbctranslator-table.md)e nella [tabella ODBCDataSource](odbcdatasource-table.md). Se esiste già un driver o un convertitore, l'azione InstallODBC esegue SQL necessarie per l'installazione.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione InstallODBC non copia o rimuove i file e deve essere eseguita dopo le azioni che copiano o rimuovono i file.

## <a name="actiondata-messages"></a>Messaggi ActionData

La tabella seguente identifica i messaggi ActionData per ogni driver installato.



| Campo       | Descrizione                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Descrizione del driver. Tasto del driver ODBC.                                 |
| \[2\]       | Componentid.                                                             |
| \[3\]       | cartella.                                                                  |
| \[4, 5, ...\] | Coppie di attributi e valori da [ODBCAttribute.](odbcattribute-table.md) |



 

La tabella seguente identifica i messaggi ActionData per ogni convertitore installato.



| Campo       | Descrizione                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Descrizione del driver. Tasto del driver ODBC.                                 |
| \[2\]       | Componentid.                                                             |
| \[3\]       | cartella.                                                                  |
| \[4, 5, ...\] | Coppie di attributi e valori da [ODBCAttribute.](odbcattribute-table.md) |



 

La tabella seguente identifica i messaggi ActionData per ogni origine dati installata.



| Campo       | Descrizione                                                              |
|-------------|--------------------------------------------------------------------------|
| \[1\]       | Descrizione del driver. Tasto del driver ODBC.                                 |
| \[2\]       | Componentid.                                                             |
| \[3\]       | Registrazione: ODBC \_ ADD \_ DSN o ODBC \_ ADD SYS \_ \_ DSN.                     |
| \[4, 5, ...\] | Coppie di attributi e valori da [ODBCAttribute.](odbcattribute-table.md) |



 

## <a name="remarks"></a>Commenti

Gestione driver ODBC deve essere creato nel pacchetto di Microsoft Installer e deve essere incluso un componente denominato ODBCDriverManager. Il manager viene installato se necessario.

Per rinominare il componente, impostare una proprietà denominata ODBCDriverManager sul nuovo nome del componente. Se è necessario installare Gestione driver ODBC a 64 bit, il componente che lo contiene deve essere denominato ODBCDriverManager64.

-   L'azione InstallODBC esegue una query sulla tabella [ODBCDataSource](odbcdatasource-table.md) e sulla tabella [ODBCSourceAttribute](odbcsourceattribute-table.md) per ogni origine dati da installare e gli attributi dell'origine dati.
-   L'azione InstallODBC esegue una query sulla tabella [ODBCDriver](odbcdriver-table.md) e sulla tabella [ODBCTranslator](odbctranslator-table.md) per ogni driver e convertitore selezionato per l'installazione.
-   L'azione InstallODBC esegue una query [sulla tabella ODBCAttribute](odbcattribute-table.md) per gli attributi dei driver e dei convertitori.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Esempi di programma di installazione](windows-installer-examples.md)
</dt> </dl>

 

 



