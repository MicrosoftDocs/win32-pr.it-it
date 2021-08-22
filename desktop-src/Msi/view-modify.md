---
description: Il metodo Modify dell'oggetto View modifica una riga del database con un oggetto Record modificato ottenuto dal metodo Fetch.
ms.assetid: c3c500aa-070f-41d7-90f7-db979452d24f
title: Metodo View.Modify
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
ms.openlocfilehash: e4149afb638c01b31d51c45f5d55c6f43fe50b4a85b77c25b4f6a5e0ed5993fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498861"
---
# <a name="viewmodify-method"></a>Metodo View.Modify

Il **metodo Modify** dell'oggetto [**View**](view-object.md) modifica una riga del database con un [**oggetto Record**](record-object.md) modificato ottenuto dal [**metodo Fetch.**](view-fetch.md)

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

Azione richiesta da eseguire sulla riga del database. Questa azione è una di quelle illustrate nella tabella seguente.



| Nome azione                                                                                                                                                                                                                                                                                                     | Significato                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiViewModifySeek"></span><span id="msiviewmodifyseek"></span><span id="MSIVIEWMODIFYSEEK"></span><dl> <dt>**msiViewModifySeek**</dt> <dt>-1</dt> </dl>                                            | Aggiorna le informazioni nel record fornito senza modificare la posizione nel set di risultati e senza influire sulle operazioni di recupero successive. Il record può quindi essere usato per i successivi aggiornamenti, eliminazione e aggiornamento. Tutte le colonne chiave primaria della tabella devono essere presenti nella query e il record deve avere almeno il numero di campi della query. Non è possibile usare Seek con query multitable. Vedere le osservazioni. Questa modalità non può essere usata con una vista contenente join.<br/>                                                                             |
| <span id="msiViewModifyRefresh"></span><span id="msiviewmodifyrefresh"></span><span id="MSIVIEWMODIFYREFRESH"></span><dl> <dt>**msiViewModifyRefresh**</dt> <dt>0</dt> </dl>                                 | Aggiorna le informazioni nel record. È necessario chiamare prima [**il metodo Fetch**](view-fetch.md) con lo stesso record. Non riesce per una riga eliminata. Funziona sia con i record di lettura/scrittura che con i record di sola lettura.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyInsert"></span><span id="msiviewmodifyinsert"></span><span id="MSIVIEWMODIFYINSERT"></span><dl> <dt>**msiViewModifyInsert**</dt> <dt>1</dt> </dl>                                     | Inserisce un record. Ha esito negativo se esiste una riga con le stesse chiavi primarie. Non riesce con un database di sola lettura. Questa modalità non può essere usata con una vista contenente join.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="msiViewModifyUpdate"></span><span id="msiviewmodifyupdate"></span><span id="MSIVIEWMODIFYUPDATE"></span><dl> <dt>**msiViewModifyUpdate**</dt> <dt>2</dt> </dl>                                     | Aggiorna un record esistente. Solo chiavi non primarie. È necessario chiamare prima [**il metodo Fetch**](view-fetch.md) con lo stesso record. Non riesce con un record eliminato. Funziona solo con i record di lettura/scrittura.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="msiViewModifyAssign"></span><span id="msiviewmodifyassign"></span><span id="MSIVIEWMODIFYASSIGN"></span><dl> <dt>**msiViewModifyAssign**</dt> <dt>3</dt> </dl>                                     | Scrive i dati correnti nel cursore in una riga di tabella. Aggiorna il record se le chiavi primarie corrispondono a una riga esistente e inserisce se non corrispondono. Non riesce con un database di sola lettura. Questa modalità non può essere usata con una vista contenente join.<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiViewModifyReplace"></span><span id="msiviewmodifyreplace"></span><span id="MSIVIEWMODIFYREPLACE"></span><dl> <dt>**msiViewModifyReplace**</dt> <dt>4</dt> </dl>                                 | Aggiorna o elimina e inserisce un record in una tabella. È necessario chiamare prima [**il metodo Fetch**](view-fetch.md) con lo stesso record. Aggiorna il record se le chiavi primarie rimangono invariate. Elimina la riga precedente e ne inserisce una nuova se le chiavi primarie sono state modificate. Non riesce con un database di sola lettura. Questa modalità non può essere usata con una vista contenente join.<br/>                                                                                                                                                                                                           |
| <span id="msiViewModifyMerge"></span><span id="msiviewmodifymerge"></span><span id="MSIVIEWMODIFYMERGE"></span><dl> <dt>**msiViewModifyMerge**</dt> <dt>5</dt> </dl>                                         | Inserisce o convalida un record in una tabella. Inserisce se le chiavi primarie non corrispondono ad alcuna riga e convalida se esiste una corrispondenza. Ha esito negativo se il record non corrisponde ai dati nella tabella. Ha esito negativo se è presente un record con una chiave duplicata che non è identica. Funziona solo con i record di lettura/scrittura. Questa modalità non può essere usata con una vista contenente join.<br/>                                                                                                                                                                                                |
| <span id="msiViewModifyDelete"></span><span id="msiviewmodifydelete"></span><span id="MSIVIEWMODIFYDELETE"></span><dl> <dt>**msiViewModifyDelete**</dt> <dt>6</dt> </dl>                                     | Rimuove una riga dalla tabella. È necessario chiamare prima [**il metodo Fetch**](view-fetch.md) con lo stesso record. Ha esito negativo se la riga è stata eliminata. Funziona solo con i record di lettura/scrittura. Questa modalità non può essere usata con una vista contenente join.<br/>                                                                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyInsertTemporary"></span><span id="msiviewmodifyinserttemporary"></span><span id="MSIVIEWMODIFYINSERTTEMPORARY"></span><dl> <dt>**msiViewModifyInsertTemporary**</dt> <dt>7</dt> </dl> | Inserisce un record temporaneo. Le informazioni non sono persistenti. Ha esito negativo se esiste una riga con la stessa chiave primaria. Funziona solo con i record di lettura/scrittura. Questa modalità non può essere usata con una vista contenente join.<br/>                                                                                                                                                                                                                                                                                                                                           |
| <span id="msiViewModifyValidate"></span><span id="msiviewmodifyvalidate"></span><span id="MSIVIEWMODIFYVALIDATE"></span><dl> <dt>**msiViewModifyValidate**</dt> <dt>8</dt> </dl>                             | Convalida un record. Non esegue la convalida tra join. È necessario chiamare prima [**il metodo Fetch**](view-fetch.md) con lo stesso record. Ottenere gli errori di convalida [**con il metodo GetError.**](view-geterror.md) Funziona con i record di lettura/scrittura e di sola lettura. Questa modalità non può essere usata con una vista contenente join.<br/>                                                                                                                                                                                                                                         |
| <span id="msiViewModifyValidateNew"></span><span id="msiviewmodifyvalidatenew"></span><span id="MSIVIEWMODIFYVALIDATENEW"></span><dl> <dt>**msiViewModifyValidateNuovo**</dt> <dt>9</dt> </dl>                 | Convalida un nuovo record. Non esegue la convalida tra join. Verifica la presenza di chiavi duplicate. Ottiene gli errori di convalida chiamando [**il metodo GetError.**](view-geterror.md) Richiede la chiamata [**al metodo MsiDatabase.OpenView**](database-openview.md) con un valore di modifica. Funziona con i record di lettura/scrittura e di sola lettura. Questa modalità non può essere usata con una vista contenente join.<br/>                                                                                                                                                                                 |
| <span id="msiViewModifyValidateField"></span><span id="msiviewmodifyvalidatefield"></span><span id="MSIVIEWMODIFYVALIDATEFIELD"></span><dl> <dt>**msiViewModifyValidateField**</dt> <dt>10</dt> </dl>        | Convalida i campi di un record recuperato o nuovo. Può convalidare uno o più campi di un record incompleto. Ottiene gli errori di convalida chiamando [**il metodo GetError.**](view-geterror.md) Funziona con i record di lettura/scrittura e di sola lettura. Questa modalità non può essere usata con una vista contenente join.<br/>                                                                                                                                                                                                                                                             |
| <span id="msiViewModifyValidateDelete"></span><span id="msiviewmodifyvalidatedelete"></span><span id="MSIVIEWMODIFYVALIDATEDELETE"></span><dl> <dt>**msiViewModifyValidateDelete**</dt> <dt>11</dt> </dl>    | Convalida un record che verrà eliminato in un secondo momento. È necessario chiamare prima [**il metodo Fetch**](view-fetch.md) con lo stesso record. Ha esito negativo se un'altra riga fa riferimento alle chiavi primarie di questa riga. La convalida non verifica l'esistenza delle chiavi primarie di questa riga nelle proprietà o nelle stringhe. Non verifica se una colonna è una chiave esterna per più tabelle. Ottenere gli errori di convalida chiamando il [**metodo GetError.**](view-geterror.md) Funziona con i record di lettura/scrittura e di sola lettura. Questa modalità non può essere usata con una vista contenente join.<br/> |



 

</dd> <dt>

*Registrazione* 
</dt> <dd>

Obbligatorio. [**Oggetto record**](record-object.md) ottenuto dal [**metodo Fetch**](view-fetch.md) con dati di campo modificati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo deve essere chiamato dopo il [**metodo Execute.**](view-execute.md)

Per eseguire qualsiasi SQL, è necessario creare una vista. Tuttavia, una vista che non crea un set di risultati, ad esempio CREATE TABLE o INSERT INTO, non può essere usata con il metodo **Modify** per aggiornare le tabelle anche se la vista.

I valori msiViewModifyValidate, msiViewModifyValidateNew, msiViewModifyValidateField e msiViewModifyValidateDelete del metodo **Modify** non eseguono aggiornamenti effettivi. assicurano che i dati nel record siano validi. L'uso di queste azioni richiede che il database contenga una [ \_ tabella di convalida](-validation-table.md) .

Non è possibile recuperare un record contenente dati binari da un database e quindi usarlo per inserire i dati in un database completamente diverso. Per spostare dati binari da un database a un altro, è necessario esportare i dati in un file e quindi importarlo nel nuovo database usando il [**metodo SetStream**](record-setstream.md) dell'oggetto [**Record.**](record-object.md) In questo modo si garantisce che ogni database abbia una propria copia dei dati binari.

> [!Note]  
> Le azioni personalizzate possono solo aggiungere, modificare o rimuovere righe, colonne o tabelle temporanee da un database. Le azioni personalizzate non possono modificare i dati persistenti in un database, ad esempio i dati che fanno parte del database archiviato su disco. Per altre informazioni, vedere Accesso alla sessione del programma di [installazione corrente dall'interno di un'azione personalizzata.](accessing-the-current-installer-session-from-inside-a-custom-action.md)

 

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IView è definito come \_ 000C109C-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



 

 




