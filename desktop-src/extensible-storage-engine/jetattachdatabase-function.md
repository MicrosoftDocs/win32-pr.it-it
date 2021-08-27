---
description: 'Altre informazioni su: Funzione JetAttachDatabase'
title: Funzione JetAttachDatabase
TOCTitle: JetAttachDatabase Function
ms:assetid: bc4c9a76-203c-424a-ac17-f096e3a6e04e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294074(v=EXCHG.10)
ms:contentKeyID: 32765689
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase
- JetAttachDatabaseW
- JetAttachDatabaseA
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b07312cbfce36b450fe39a39810813adc2d0fd4
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987704"
---
# <a name="jetattachdatabase-function"></a>Funzione JetAttachDatabase


_**Si applica a:** Windows | Windows Server_

## <a name="jetattachdatabase-function"></a>Funzione JetAttachDatabase

La **funzione JetAttachDatabase collega** un file di database da usare con un'istanza del database. Per usare il database, sarà necessario aprire il database in un secondo tempo [con JetOpenDatabase](./jetopendatabase-function.md).

```cpp
    JET_ERR JET_API JetAttachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Parametri

*sesid*

Contesto della sessione di database da usare per la chiamata API.

*szFilename*

Nome del database da collegare.

*grbit*

Gruppo di bit che specificano zero o più delle opzioni seguenti.


| <p>Valore</p> | <p>Significato</p> | 
|--------------|----------------|
| <p>JET_bitDbDeleteCorruptIndexes</p> | <p>Se <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> è stato impostato, verranno eliminati tutti gli indici sui dati Unicode. Per altre informazioni, vedere le sezione Osservazioni.</p> | 
| <p>JET_bitDbDeleteUnicodeIndexes</p> | <p>Tutti gli indici sui dati Unicode verranno eliminati, indipendentemente dall'impostazione <a href="gg269337(v=exchg.10).md">di JET_paramEnableIndexChecking</a>. Per altre informazioni, vedere le sezione Osservazioni.</p> | 
| <p>JET_bitDbUpgrade</p> | <p>Obsoleta. Non usare.</p> | 
| <p>JET_bitDbReadOnly</p> | <p>Impedisce modifiche al database.</p> | 



### <a name="return-value"></a>Valore restituito

Questa funzione restituisce il [JET_ERR](./jet-err.md) dati con uno dei codici restituiti seguenti. Per altre informazioni sui possibili errori ESE, vedere [Extensible Archiviazione Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Codice restituito</p> | <p>Descrizione</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Operazione riuscita.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Il collegamento di un database non è consentito durante un backup.</p> | 
| <p>JET_errDatabaseFileReadOnly</p> | <p>Il file di database specificato <em>da szFilename</em> deve essere scrivibile. LRead-Only attribuito non deve essere impostato e il processo in esecuzione deve avere privilegi sufficienti per scrivere nel file.</p> | 
| <p>JET_errDatabaseInUse</p> | <p>Il file di database è già aperto da un altro processo.</p> | 
| <p>JET_errDatabaseInvalidPath</p> | <p>È stato specificato un percorso non valido in <em>szFilename</em>. <em>szFilename deve</em> essere diverso da NULL e fare riferimento a un percorso valido.</p> | 
| <p>JET_errDatabaseSharingViolation</p> | <p>Il file di database è già stato collegato da una sessione diversa.</p> | 
| <p>JET_errFileAccessDenied</p> | <p>Il motore di database non è in grado di aprire il file di database. Il file può essere utilizzato da un altro processo o il chiamante potrebbe non disporre di privilegi sufficienti per aprire il file.</p> | 
| <p>JET_errFileNotFound</p> | <p>Il file specificato in <em>szFilename</em> non esiste.</p> | 
| <p>JET_errPrimaryIndexCorrupted</p> | <p>Si è verificato un errore con l'indice primario. Può trattarsi di un danneggiamento fisico, ad esempio il danneggiamento del disco o della memoria. Può anche essere restituito quando si collega un database per l'ultima modifica in un sistema operativo precedente e l'indice primario si trova su una colonna con dati Unicode. Per altre informazioni sugli indici sui dati Unicode, vedere le osservazioni.</p> | 
| <p>JET_errSecondaryIndexCorrupted</p> | <p>Si è verificato un errore con un indice secondario. Può trattarsi di un danneggiamento fisico, ad esempio il danneggiamento del disco o della memoria. Può anche essere restituito quando si collega un database per l'ultima modifica in un sistema operativo precedente e un indice secondario si trova su una colonna con dati Unicode. Per altre informazioni sugli indici sui dati Unicode, vedere le osservazioni. Gli indici secondari vengono completamente ricompilati quando un database viene deframmentato con un'utilità offline usando il comando <strong>seguente: esentutl -d</strong>.</p> | 
| <p>JET_errTooManyAttachedDatabases</p> | <p>È possibile collegare solo un numero finito di database per ogni istanza. Il limite è attualmente di sette database per istanza.</p> | 
| <p>JET_wrnDatabaseAttached</p> | <p>Avviso non irreversibile che indica che il file di database è già stato collegato da questa sessione.</p> | 



#### <a name="remarks"></a>Commenti

Chiamare **JetAttachDatabase** equivale a chiamare [JetAttachDatabase2](./jetattachdatabase2-function.md) e a passare un valore pari a zero, ovvero non esiste alcun limite, per il *parametro cpgDatabaseSizeMax.*

Collegando un database scrivibile, ovvero se JET_bitDbReadOnly non è stato specificato nel parametro *grbit,* il file verrà aperto esclusivamente a livello di sistema operativo. Nessun altro processo sarà in grado di aprire il file. È possibile che più processi collegano un singolo database aprendoli in modalità di sola lettura.

Il file di database viene scollegato [tramite JetDetachDatabase](./jetdetachdatabase-function.md) o [JetDetachDatabase2.](./jetdetachdatabase2-function.md)

Parametri di controllo dell'indice

Versioni diverse di Windows normalizzare il testo Unicode in modi diversi. Ciò significa che gli indici compilati in una versione di Windows potrebbero non funzionare in altre versioni.

Prima di Windows Server 2003, quando la versione del sistema operativo cambiava (inclusa l'installazione di un Service Pack), ogni indice sui dati Unicode era potenzialmente danneggiato.

Gli indici creati in Windows Server 2003 e versioni successive sono contrassegnati con la versione di normalizzazione Unicode con cui sono stati compilati. Gli indici meno recenti non contengono informazioni sulla versione. La maggior parte delle modifiche alla normalizzazione Unicode consiste nell'aggiunta di nuovi caratteri. I punti di codice precedentemente non definiti sono ora definiti e normalizzano in modo diverso. Pertanto, se i dati binari vengono archiviati in una colonna Unicode, verranno normalizzati in modo diverso quando vengono definiti nuovi punti di codice.

A Windows Server 2003, il motore di database ESE tiene traccia delle voci di indice Unicode che contengono punti di codice non definiti. Possono essere usati per correggere un indice quando viene modificato il set di caratteri Unicode definiti.

Questi parametri controllano cosa accade quando il motore di database ESE si collega a un database usato per l'ultima volta in una build diversa del sistema operativo. La versione del sistema operativo viene contrassegnata nell'intestazione del database.

Se [JET_paramEnableIndexChecking](./database-parameters.md) è impostato su **TRUE** e il database contiene indici potenzialmente danneggiati:

  - **JetAttachDatabase** eliminerà gli indici potenzialmente danneggiati se *grbit* contiene JET_bitDbDeleteCorruptIndexes

  - **JetAttachDatabase** restituirà un errore se *grbit* non contiene JET_bitDbDeleteCorruptIndexes e sono presenti indici che devono essere eliminati.

Se [JET_paramEnableIndexChecking](./database-parameters.md) è impostato su **FALSE**:

  - **JetAttachDatabase** ignorerà gli indici potenzialmente danneggiati e restituirà JET_errSuccess (presupponendo che non siano presenti altri errori).

Windows Server 2003 e versioni successive: se [JET_paramEnableIndexChecking](./database-parameters.md) non è stato reimpostato, la tabella di correzione interna verrà usata per correggere le voci di indice. Questa operazione potrebbe non correggere tutti i danneggiamenti degli indici, ma sarà trasparente per l'applicazione.

Se il database è stato collegato come di sola lettura, l'indice non può essere corretto o eliminato. In questo caso, l'API restituirà invece un errore, ad esempio JET_errSecondaryIndexCorrupted o JET_errPrimaryIndexCorrupted.

#### <a name="requirements"></a>Requisiti


| Requisito | Valore |
|------------|----------|
| <p><strong>Client</strong></p> | <p>Richiede Windows Vista, Windows XP o Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</p> | 
| <p><strong>Intestazione</strong></p> | <p>Dichiarato in Esent.h.</p> | 
| <p><strong>Libreria</strong></p> | <p>Usare ESENT.lib.</p> | 
| <p><strong>DLL</strong></p> | <p>Richiede ESENT.dll.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implementato come <strong>JetAddColumnW</strong> (Unicode) e <strong>JetAddColumnA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Vedere anche

[File extensible Archiviazione Engine](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetDetachDatabase2](./jetdetachdatabase2-function.md)  
[JetOpenDatabase](./jetopendatabase-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
