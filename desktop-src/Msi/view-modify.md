---
description: Il metodo modify dell'oggetto View modifica una riga di database con un oggetto record modificato ottenuto dal metodo fetch.
ms.assetid: c3c500aa-070f-41d7-90f7-db979452d24f
title: View. Modify (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.Modify
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b4dc97f2e3b5f85d472cfcbfad6017ce4e051e4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329240"
---
# <a name="viewmodify-method"></a>View. Modify (metodo)

Il metodo **Modify** dell'oggetto [**View**](view-object.md) modifica una riga di database con un oggetto [**record**](record-object.md) modificato ottenuto dal metodo [**Fetch**](view-fetch.md) .

## <a name="syntax"></a>Sintassi


```JScript
View.Modify(
  action,
  record
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*action* 
</dt> <dd>

Azione obbligatoria da eseguire sulla riga del database. Questa azione è una di quelle illustrate nella tabella seguente.



| Nome azione                                                                                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiViewModifySeek"></span><span id="msiviewmodifyseek"></span><span id="MSIVIEWMODIFYSEEK"></span><dl> <dt>**msiViewModifySeek**</dt> <dt>-1</dt> </dl>                                            | Aggiorna le informazioni nel record fornito senza modificare la posizione nel set di risultati e senza influire sulle operazioni di recupero successive. Il record può quindi essere utilizzato per l'aggiornamento, l'eliminazione e l'aggiornamento successivi. Tutte le colonne chiave primaria della tabella devono trovarsi nella query e il record deve contenere almeno tutti i campi della query. Impossibile utilizzare Seek con query su più tabelle. Vedere la sezione Osservazioni. Questa modalità non può essere utilizzata con una vista contenente join.<br/>                                                                             |
| <span id="msiViewModifyRefresh"></span><span id="msiviewmodifyrefresh"></span><span id="MSIVIEWMODIFYREFRESH"></span><dl> <dt>**msiViewModifyRefresh**</dt> <dt>0</dt> </dl>                                 | Aggiorna le informazioni nel record. Deve prima chiamare il metodo [**Fetch**](view-fetch.md) con lo stesso record. Non riesce per una riga eliminata. Funziona con i record sia di lettura/scrittura che di sola lettura.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyInsert"></span><span id="msiviewmodifyinsert"></span><span id="MSIVIEWMODIFYINSERT"></span><dl> <dt>**msiViewModifyInsert**</dt> <dt>1</dt> </dl>                                     | Inserisce un record. Ha esito negativo se esiste una riga con le stesse chiavi primarie. Ha esito negativo con un database di sola lettura. Questa modalità non può essere utilizzata con una vista contenente join.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="msiViewModifyUpdate"></span><span id="msiviewmodifyupdate"></span><span id="MSIVIEWMODIFYUPDATE"></span><dl> <dt>**msiViewModifyUpdate**</dt> <dt>2</dt> </dl>                                     | Aggiorna un record esistente. Solo chiavi non primarie. Deve prima chiamare il metodo [**Fetch**](view-fetch.md) con lo stesso record. Ha esito negativo con un record eliminato. Funziona solo con i record di lettura/scrittura.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyAssign"></span><span id="msiviewmodifyassign"></span><span id="MSIVIEWMODIFYASSIGN"></span><dl> <dt>**msiViewModifyAssign**</dt> <dt>3</dt> </dl>                                     | Scrive i dati correnti nel cursore in una riga di tabella. Aggiorna il record se le chiavi primarie corrispondono a una riga esistente e vengono inserite se non corrispondono. Ha esito negativo con un database di sola lettura. Questa modalità non può essere utilizzata con una vista contenente join.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiViewModifyReplace"></span><span id="msiviewmodifyreplace"></span><span id="MSIVIEWMODIFYREPLACE"></span><dl> <dt>**msiViewModifyReplace**</dt> <dt>4</dt> </dl>                                 | Aggiorna o Elimina e inserisce un record in una tabella. Deve prima chiamare il metodo [**Fetch**](view-fetch.md) con lo stesso record. Aggiorna il record se le chiavi primarie sono invariate. Elimina la riga precedente e inserisce nuovo se le chiavi primarie sono state modificate. Ha esito negativo con un database di sola lettura. Questa modalità non può essere utilizzata con una vista contenente join.<br/>                                                                                                                                                                                                           |
| <span id="msiViewModifyMerge"></span><span id="msiviewmodifymerge"></span><span id="MSIVIEWMODIFYMERGE"></span><dl> <dt>**msiViewModifyMerge**</dt> <dt>5</dt> </dl>                                         | Inserisce o convalida un record in una tabella. Inserisce se le chiavi primarie non corrispondono ad alcuna riga e ne viene eseguita la convalida in caso di corrispondenza. Ha esito negativo se il record non corrisponde ai dati nella tabella. Ha esito negativo se è presente un record con una chiave duplicata non identica. Funziona solo con i record di lettura/scrittura. Questa modalità non può essere utilizzata con una vista contenente join.<br/>                                                                                                                                                                                                |
| <span id="msiViewModifyDelete"></span><span id="msiviewmodifydelete"></span><span id="MSIVIEWMODIFYDELETE"></span><dl> <dt>**msiViewModifyDelete**</dt> <dt>6</dt> </dl>                                     | Rimuove una riga dalla tabella. Deve prima chiamare il metodo [**Fetch**](view-fetch.md) con lo stesso record. Ha esito negativo se la riga è stata eliminata. Funziona solo con i record di lettura/scrittura. Questa modalità non può essere utilizzata con una vista contenente join.<br/>                                                                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyInsertTemporary"></span><span id="msiviewmodifyinserttemporary"></span><span id="MSIVIEWMODIFYINSERTTEMPORARY"></span><dl> <dt>**msiViewModifyInsertTemporary**</dt> <dt>7</dt> </dl> | Inserisce un record temporaneo. Le informazioni non sono persistenti. Ha esito negativo se esiste una riga con la stessa chiave primaria. Funziona solo con i record di lettura/scrittura. Questa modalità non può essere utilizzata con una vista contenente join.<br/>                                                                                                                                                                                                                                                                                                                                           |
| <span id="msiViewModifyValidate"></span><span id="msiviewmodifyvalidate"></span><span id="MSIVIEWMODIFYVALIDATE"></span><dl> <dt>**msiViewModifyValidate**</dt> <dt>8</dt> </dl>                             | Convalida un record. Non esegue la convalida in join. Deve prima chiamare il metodo [**Fetch**](view-fetch.md) con lo stesso record. Ottenere errori di convalida con il metodo [**GetError**](view-geterror.md) . Funziona con i record di lettura/scrittura e di sola lettura. Questa modalità non può essere utilizzata con una vista contenente join.<br/>                                                                                                                                                                                                                                         |
| <span id="msiViewModifyValidateNew"></span><span id="msiviewmodifyvalidatenew"></span><span id="MSIVIEWMODIFYVALIDATENEW"></span><dl> <dt>**msiViewModifyValidateNew**</dt> <dt>9</dt> </dl>                 | Convalida un nuovo record. Non esegue la convalida in join. Verifica le chiavi duplicate. Ottiene gli errori di convalida chiamando il metodo [**GetError**](view-geterror.md) . Richiede la chiamata al metodo [**MsiDatabase. OpenView**](database-openview.md) con un valore di modifica. Funziona con i record di lettura/scrittura e di sola lettura. Questa modalità non può essere utilizzata con una vista contenente join.<br/>                                                                                                                                                                                 |
| <span id="msiViewModifyValidateField"></span><span id="msiviewmodifyvalidatefield"></span><span id="MSIVIEWMODIFYVALIDATEFIELD"></span><dl> <dt>**msiViewModifyValidateField**</dt> <dt>10</dt> </dl>        | Convalida i campi di un record recuperato o nuovo. Consente di convalidare uno o più campi di un record incompleto. Ottiene gli errori di convalida chiamando il metodo [**GetError**](view-geterror.md) . Funziona con i record di lettura/scrittura e di sola lettura. Questa modalità non può essere utilizzata con una vista contenente join.<br/>                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyValidateDelete"></span><span id="msiviewmodifyvalidatedelete"></span><span id="MSIVIEWMODIFYVALIDATEDELETE"></span><dl> <dt>**msiViewModifyValidateDelete**</dt> <dt>11</dt> </dl>    | Convalida un record che verrà eliminato in un secondo momento. Deve prima chiamare il metodo [**Fetch**](view-fetch.md) con lo stesso record. Ha esito negativo se un'altra riga si riferisce alle chiavi primarie di questa riga. La convalida non verifica l'esistenza delle chiavi primarie di questa riga in proprietà o stringhe. Non verifica se una colonna è una chiave esterna per più tabelle. Ottenere errori di convalida chiamando il metodo [**GetError**](view-geterror.md) . Funziona con i record di lettura/scrittura e di sola lettura. Questa modalità non può essere utilizzata con una vista contenente join.<br/> |



 

</dd> <dt>

*record* 
</dt> <dd>

Obbligatorio. Oggetto [**record**](record-object.md) ottenuto dal metodo [**Fetch**](view-fetch.md) con i dati dei campi modificati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato dopo il metodo [**Execute**](view-execute.md) .

Per eseguire qualsiasi istruzione SQL, è necessario creare una vista. Tuttavia, una vista che non crea un set di risultati, ad esempio CREATE TABLE o INSERT INTO, non può essere utilizzata con il metodo **Modify** per aggiornare le tabelle tramite la vista.

I valori msiViewModifyValidate, msiViewModifyValidateNew, msiViewModifyValidateField e msiViewModifyValidateDelete del metodo **Modify** non eseguono gli aggiornamenti effettivi; assicurano che i dati nel record siano validi. Per l'utilizzo di queste azioni è necessario che il database contenga una [ \_ tabella di convalida](-validation-table.md) .

Non è possibile recuperare un record contenente dati binari da un database e quindi utilizzare tale record per inserire i dati in un database completamente diverso. Per spostare i dati binari da un database a un altro, è necessario esportare i dati in un file e quindi importarli nel nuovo database usando il metodo [**sestream**](record-setstream.md) dell'oggetto [**record**](record-object.md) . In questo modo si garantisce che ogni database disponga di una propria copia dei dati binari.

> [!Note]  
> Le azioni personalizzate possono aggiungere, modificare o rimuovere solo righe, colonne o tabelle temporanee da un database. Le azioni personalizzate non possono modificare i dati persistenti in un database, ad esempio i dati che fanno parte del database archiviato su disco. Per altre informazioni, vedere [accesso alla sessione del programma di installazione corrente dall'interno di un'azione personalizzata](accessing-the-current-installer-session-from-inside-a-custom-action.md).

 

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iView è definito come 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




