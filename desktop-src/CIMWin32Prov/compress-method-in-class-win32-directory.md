---
description: Comprime il file di voce di directory logica (o directory) specificato nel percorso dell'oggetto.
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: Metodo Compress della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15d9142abb95998fce803c30c439632775cd8ff807f3b7d99653875d08e534e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020669"
---
# <a name="compress-method-of-the-win32_directory-class"></a>Metodo Compress della classe Directory Win32 \_

Il **metodo compresso** [della classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) comprime il file di voce di directory logica (o directory) specificato nel percorso dell'oggetto.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Compress();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) se il file è stato compresso correttamente e qualsiasi altro numero per indicare un errore.

<dl> <dt>

**0**
</dt> <dd>

La richiesta è stata completata.

</dd> <dt>

**2**
</dt> <dd>

Accesso negato.

</dd> <dt>

**8**
</dt> <dd>

Si è verificato un errore non specificato.

</dd> <dt>

**9**
</dt> <dd>

Il nome specificato non è valido.

</dd> <dt>

**10**
</dt> <dd>

L'oggetto specificato esiste già.

</dd> <dt>

**11**
</dt> <dd>

Il file system non è ntfs.

</dd> <dt>

**12**
</dt> <dd>

La piattaforma non è Windows.

</dd> <dt>

**13**
</dt> <dd>

L'unità non è la stessa.

</dd> <dt>

**14**
</dt> <dd>

La directory non è vuota.

</dd> <dt>

**15**
</dt> <dd>

Si è verificata una violazione di condivisione.

</dd> <dt>

**16**
</dt> <dd>

Il file iniziale specificato non è valido.

</dd> <dt>

**17**
</dt> <dd>

Un privilegio necessario per l'operazione non viene mantenuto.

</dd> <dt>

**21**
</dt> <dd>

Un parametro specificato non è valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

La compressione consente di liberare spazio di archiviazione aggiuntivo in un'unità disco senza acquistare nuovo hardware e senza rimuovere file o cartelle. A seconda delle dimensioni del disco rigido e del tipo di file archiviati su tale disco, potrebbe essere possibile recuperare centinaia di megabyte di spazio su disco e quindi precludere la necessità di acquistare un nuovo disco rigido e di portare offline il computer fino a quando non viene installata la nuova unità.

Il metodo Compress comprime tutti i file e le sottocartelle all'interno di una cartella specificata. Inoltre, la classe include anche un metodo Uncompress che rimuove la compressione da tutti i file e le sottocartelle in una cartella. Metodi simili vengono forniti anche con la classe \_ Datafile CIM. In questo modo è possibile comprimere o decomprimere in modo selettivo file specifici all'interno di una cartella.

Poiché la compressione causa una lieve riduzione delle prestazioni, non è consigliabile per i file o le cartelle a cui si accede regolarmente; Ad esempio, è probabile che non si voglia comprimere i file di database, i file di log o le cartelle dei profili utente. I candidati migliori per la compressione sono i file e le cartelle a cui non si accede molto spesso. Ad esempio, è possibile scrivere uno script per restituire una raccolta di cartelle in un'unità a cui non è stato eseguito l'accesso per un mese o più e quindi comprimere ognuna di queste cartelle.

La quantità di spazio su disco liberata dalla compressione delle cartelle varia a seconda del tipo di file archiviati in tale cartella. Ad esempio, .jpg file sono già compressi e un'ulteriore compressione ha un effetto scarso sulle dimensioni del file. Con altri tipi di file, tuttavia, il risparmio può essere notevole. Ad esempio, è stata creata una nuova cartella in un computer di test basato su Windows 2000 e in tale cartella sono stati copiati 33 documenti Microsoft Word, che occupano in totale 15 megabyte (MB) di spazio su disco. Quando i documenti sono stati compressi, la cartella ha impiegato solo 7 MB di spazio su disco.

## <a name="examples"></a>Esempio

L'esempio VBScript seguente comprime la cartella C: \\ Scripts.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Compress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ Directory**](win32-directory.md)
</dt> <dt>

[**Decomprimere**](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

