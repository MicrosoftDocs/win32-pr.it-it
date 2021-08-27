---
description: L'oggetto Database accede a un database del programma di installazione.
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
ms.openlocfilehash: 3dcdb2c4098905d7e6a410e786d4af254732bc80cee4b760870a7c1c44a8ec26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086201"
---
# <a name="database-object"></a>Oggetto di database

**L'oggetto Database** accede a un database del programma di installazione.

**L'oggetto Database** viene rilasciato quando viene esmesso dall'ambito o quando la variabile oggetto associata è impostata su Null. Il [**metodo Commit**](database-commit.md) deve essere chiamato prima del rilascio dell'oggetto **Database** per scrivere tutte le modifiche persistenti. Se il **metodo Commit non** viene chiamato, il programma di installazione esegue un rollback implicito in caso di distruzione degli oggetti.

Il client può usare la procedura seguente per l'accesso ai dati.

**Per eseguire query sulla sequenziazione dell'API**

1.  Ottenere un **oggetto Database** chiamando l'oggetto [**OpenDatabase**](installer-opendatabase.md) o [**Installer.**](installer-object.md)
2.  Avviare una query usando SQL stringa chiamando il [**metodo OpenView**](database-openview.md) dell'oggetto **Database.**
3.  Impostare i parametri di query in [**un oggetto Record**](record-object.md) ed eseguire la query di database chiamando il metodo [**Execute**](view-execute.md) dell'oggetto [**View.**](view-object.md) Ciò produce un risultato che può essere recuperato o aggiornato.
4.  Chiamare ripetutamente [**il metodo Fetch**](view-fetch.md) dell'oggetto [**View**](view-object.md) per restituire [**oggetti Record.**](record-object.md)
5.  Aggiornare le righe di [**database di un oggetto Record**](record-object.md) ottenute dal metodo [**Fetch**](view-fetch.md) usando il [**metodo Modify**](view-modify.md) dell'oggetto [**View.**](view-object.md)
6.  Rilasciare la query e tutti i record non rilasciati chiamando il [**metodo Close**](view-close.md) dell'oggetto [**View.**](view-object.md)
7.  Rendere persistenti gli aggiornamenti del database chiamando il [**metodo Commit**](database-commit.md) dell'oggetto **Database.**

## <a name="members"></a>Membri

**L'oggetto Database** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Database** dispone di questi metodi.



| Metodo                                                                    | Descrizione                                                                                                                                                               |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplyTransform**](database-applytransform.md)                         | Applica la trasformazione a questo database.<br/>                                                                                                                        |
| [**Eseguire il commit**](database-commit.md)                                         | Finalizza la forma persistente del database.<br/>                                                                                                                 |
| [**CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md) | Crea e popola il flusso di informazioni di riepilogo di un file di trasformazione esistente.<br/>                                                                            |
| [**EnableUIPreview**](database-enableuipreview.md)                       | Facilita la creazione di finestre di dialogo e manifesti fornendo il supporto necessario per visualizzare le finestre di dialogo dell'interfaccia utente archiviate nel database del programma di installazione.<br/> |
| [**Esportazione**](database-export.md)                                         | Copia la struttura e i dati da una tabella specificata in un file di archivio di testo.<br/>                                                                                   |
| [**GenerateTransform**](database-generatetransform.md)                   | Crea una trasformazione.<br/>                                                                                                                                           |
| [**Importa**](database-import.md)                                         | Importa una tabella di database da un file di archivio di testo.<br/>                                                                                                             |
| [**Unione**](database-merge.md)                                           | Unisce il database di riferimento al database di base.<br/>                                                                                                          |
| [**Openview**](database-openview.md)                                     | Restituisce un [**oggetto View**](view-object.md) che rappresenta la query specificata da una SQL stringa.<br/>                                                                 |



 

### <a name="properties"></a>Proprietà

**L'oggetto Database** ha queste proprietà.



| Proprietà                                                                               | Descrizione                                                                                                                                                      |
|:---------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DatabaseState**](database-databasestate.md)<br/>                             | Restituisce lo stato di persistenza del database.<br/>                                                                                                        |
| [**PrimaryKeys**](database-primarykeys.md)<br/>                                 | Restituisce un [**oggetto Record**](record-object.md) contenente il nome della tabella e i nomi delle colonne (che comprendono le chiavi primarie).<br/>                        |
| [**SummaryInformation (oggetto Database)**](database-summaryinformation.md)<br/> | Restituisce un [**oggetto SummaryInfo**](summaryinfo-object.md) che può essere usato per esaminare, aggiornare e aggiungere proprietà al flusso di informazioni di riepilogo.<br/> |
| [**TablePersistent**](database-tablepersistent.md)<br/>                         | Restituisce lo stato di persistenza della tabella.<br/>                                                                                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IDatabase è definito come \_ 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Windows Esempi di scripting del programma di installazione](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




