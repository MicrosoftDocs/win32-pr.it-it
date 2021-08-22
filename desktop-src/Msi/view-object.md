---
description: L'oggetto View rappresenta un set di risultati ottenuto durante l'elaborazione di una query usando il metodo OpenView dell'oggetto Database.
ms.assetid: d9d6583a-1cf3-4c33-a851-83e862e2338e
title: Oggetto View
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f5025df952ce6e3c5ce43bf3dcb93748a241702b8c4e2f52cd9d0fd00103dc49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145274"
---
# <a name="view-object"></a>Oggetto View

**L'oggetto View** rappresenta un set di risultati ottenuto durante l'elaborazione di una query usando il [**metodo OpenView**](database-openview.md) dell'oggetto [**Database.**](database-object.md) Prima di poter trasferire i dati, è necessario eseguire la query usando il metodo [**Execute,**](view-execute.md) passando alla query tutti i parametri sostituibili designati all'interno SQL stringa di query. La query può essere eseguita nuovamente, con parametri diversi se necessario, ma solo dopo aver liberato il set di risultati recuperando tutti i record o chiamando il [**metodo Close.**](view-close.md)

## <a name="members"></a>Membri

**L'oggetto View** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto View** dispone di questi metodi.



| Metodo                            | Descrizione                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Chiudi**](view-close.md)       | Termina l'esecuzione della query e rilascia le risorse del database.<br/>                                                                                                          |
| [**Eseguire**](view-execute.md)   | Usa il token punto interrogativo per rappresentare i parametri in una query SQL query. I valori di questi parametri vengono passati come campi corrispondenti di un record di parametro.<br/> |
| [**Prendere**](view-fetch.md)       | Restituisce un [**oggetto Record**](record-object.md) contenente i dati della colonna richiesti se sono disponibili più righe nel set di risultati. In caso contrario, restituisce Null.<br/>      |
| [**GetError**](view-geterror.md) | Restituisce l'errore di convalida e il nome della colonna per cui si è verificato l'errore.<br/>                                                                                           |
| [**Modifica**](view-modify.md)     | Modifica una riga del database con un [**oggetto Record**](record-object.md) modificato ottenuto dal [**metodo Fetch.**](view-fetch.md)<br/>                                   |



 

### <a name="properties"></a>Proprietà

**L'oggetto View** ha queste proprietà.



| Proprietà                                         | Descrizione                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**ColumnInfo**](view-columninfo.md)<br/> | Restituisce un [**oggetto Record**](record-object.md) contenente le informazioni richieste su ogni colonna nel set di risultati.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IView è definito come 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Windows Esempi di script del programma di installazione](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




