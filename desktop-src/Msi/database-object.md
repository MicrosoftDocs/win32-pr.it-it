---
description: L'oggetto di database accede a un database del programma di installazione.
ms.assetid: 97765884-3e1c-486a-932c-6430b113fac8
title: Oggetto di database
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5b47e4678d9475abe90c4b55d6adb514314dcc0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333059"
---
# <a name="database-object"></a>Oggetto di database

L'oggetto di **database** accede a un database del programma di installazione.

L'oggetto di **database** viene rilasciato quando viene ricavato dall'ambito o quando la variabile oggetto associata è impostata su null. È necessario chiamare il metodo [**commit**](database-commit.md) prima che l'oggetto di **database** venga rilasciato per scrivere tutte le modifiche permanenti. Se il metodo **commit** non viene chiamato, il programma di installazione esegue un rollback implicito alla distruzione degli oggetti.

Il client può utilizzare la procedura seguente per l'accesso ai dati.

**Per eseguire query sulla sequenziazione dell'API**

1.  Ottenere un oggetto di **database** chiamando il [**OpenDatabase**](installer-opendatabase.md) o l'oggetto del [**programma di installazione**](installer-object.md) .
2.  Avviare una query utilizzando una stringa SQL chiamando il metodo [**OpenView**](database-openview.md) dell'oggetto di **database** .
3.  Impostare i parametri di query in un oggetto [**record**](record-object.md) ed eseguire la query di database chiamando il metodo [**Execute**](view-execute.md) dell'oggetto [**View**](view-object.md) . Viene generato un risultato che può essere recuperato o aggiornato.
4.  Chiamare ripetutamente il metodo [**Fetch**](view-fetch.md) dell'oggetto [**View**](view-object.md) per restituire gli oggetti [**record**](record-object.md) .
5.  Aggiornare le righe del database di un oggetto [**record**](record-object.md) ottenuto dal metodo [**Fetch**](view-fetch.md) utilizzando il metodo [**Modify**](view-modify.md) dell'oggetto [**View**](view-object.md) .
6.  Rilasciare la query e tutti i record non recuperati chiamando il metodo [**Close**](view-close.md) dell'oggetto [**View**](view-object.md) .
7.  Consente di salvare in modo permanente eventuali aggiornamenti del database chiamando il metodo [**commit**](database-commit.md) dell'oggetto di **database** .

## <a name="members"></a>Membri

L'oggetto di **database** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'oggetto di **database** .



| Metodo                                                                    | Descrizione                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplyTransform**](database-applytransform.md)                         | Applica la trasformazione al database.<br/>                                                                                                                        |
| [**Commit**](database-commit.md)                                         | Completa il form persistente del database.<br/>                                                                                                                 |
| [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) | Crea e popola il flusso di informazioni di riepilogo di un file di trasformazione esistente.<br/>                                                                            |
| [**EnableUIPreview**](database-enableuipreview.md)                       | Semplifica la creazione di finestre di dialogo e cartelloni, fornendo il supporto necessario per visualizzare le finestre di dialogo dell'interfaccia utente archiviate nel database del programma di installazione.<br/> |
| [**Esportazione**](database-export.md)                                         | Copia la struttura e i dati da una tabella specificata in un file di archivio di testo.<br/>                                                                                   |
| [**GenerateTransform**](database-generatetransform.md)                   | Crea una trasformazione.<br/>                                                                                                                                           |
| [**Importa**](database-import.md)                                         | Importa una tabella di database da un file di archivio di testo.<br/>                                                                                                             |
| [**Unione**](database-merge.md)                                           | Unisce il database di riferimento al database di base.<br/>                                                                                                          |
| [**OpenView**](database-openview.md)                                     | Restituisce un oggetto [**visualizzazione**](view-object.md) che rappresenta la query specificata da una stringa SQL.<br/>                                                                 |



 

### <a name="properties"></a>Proprietà

L'oggetto di **database** dispone di queste proprietà.



| Proprietà                                                                               | Descrizione                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DatabaseState**](database-databasestate.md)<br/>                             | Restituisce lo stato di persistenza del database.<br/>                                                                                                        |
| [**PrimaryKeys**](database-primarykeys.md)<br/>                                 | Restituisce un oggetto [**record**](record-object.md) contenente il nome della tabella e i nomi delle colonne (incluse le chiavi primarie).<br/>                        |
| [**SummaryInformation (oggetto di database)**](database-summaryinformation.md)<br/> | Restituisce un oggetto [**SummaryInfo**](summaryinfo-object.md) che può essere utilizzato per esaminare, aggiornare e aggiungere proprietà al flusso di informazioni di riepilogo.<br/> |
| [**TablePersistent**](database-tablepersistent.md)<br/>                         | Restituisce lo stato di persistenza della tabella.<br/>                                                                                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




