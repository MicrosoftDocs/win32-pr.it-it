---
description: L'oggetto View rappresenta un set di risultati ottenuto durante l'elaborazione di una query utilizzando il metodo OpenView dell'oggetto di database.
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
ms.openlocfilehash: c26cfa3c4873913d70fca63537f1d25532648a42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329231"
---
# <a name="view-object"></a>Oggetto View

L'oggetto **View** rappresenta un set di risultati ottenuto durante l'elaborazione di una query utilizzando il metodo [**OpenView**](database-openview.md) dell'oggetto di [**database**](database-object.md) . Prima di poter trasferire i dati, la query deve essere eseguita utilizzando il metodo [**Execute**](view-execute.md) , passandogli tutti i parametri sostituibili designati all'interno della stringa di query SQL. La query può essere eseguita di nuovo, con parametri diversi, se necessario, ma solo dopo avere liberato il set di risultati recuperando tutti i record o chiamando il metodo [**Close**](view-close.md) .

## <a name="members"></a>Membri

L'oggetto **View** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **View** presenta questi metodi.



| Metodo                            | Descrizione                                                                                                                                                                     |
|:----------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Chiudi**](view-close.md)       | Termina l'esecuzione della query e rilascia le risorse di database.<br/>                                                                                                          |
| [**Execute**](view-execute.md)   | Usa il token punto interrogativo per rappresentare i parametri in una query SQL. I valori di questi parametri vengono passati come campi corrispondenti di un record di parametri.<br/> |
| [**Prendere**](view-fetch.md)       | Restituisce un oggetto [**record**](record-object.md) contenente i dati della colonna richiesta se nel set di risultati sono disponibili più righe. in caso contrario, restituisce null.<br/>      |
| [**GetError**](view-geterror.md) | Restituisce l'errore di convalida e il nome della colonna per cui si è verificato l'errore.<br/>                                                                                           |
| [**Modificare**](view-modify.md)     | Modifica una riga di database con un oggetto [**record**](record-object.md) modificato ottenuto dal metodo [**Fetch**](view-fetch.md) .<br/>                                   |



 

### <a name="properties"></a>Proprietà

L'oggetto **View** dispone di queste proprietà.



| Proprietà                                         | Descrizione                                                                                                                           |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**ColumnInfo**](view-columninfo.md)<br/> | Restituisce un oggetto [**record**](record-object.md) contenente le informazioni richieste su ogni colonna nel set di risultati.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView è definito come 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




