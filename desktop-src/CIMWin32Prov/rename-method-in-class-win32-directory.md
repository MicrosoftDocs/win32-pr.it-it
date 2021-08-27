---
description: Rinomina il file di voci di directory specificato nel percorso dell'oggetto.
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Metodo Rename della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 86b6bd35b14ee2a342dee27615c1ff21d9274a5f3020c4f804df5065f430813f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077441"
---
# <a name="rename-method-of-the-win32_directory-class"></a>Metodo Rename della classe Directory Win32 \_

Il **metodo rinomina** la classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) rinomina il file di voci di directory specificato nel percorso dell'oggetto. La ridenominazione non è supportata se la destinazione si trova in un'altra unità o se è necessario sovrascrivere un file logico esistente.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, [vedere Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FileName* 
</dt> <dd>

Nuovo nome completo del file (o directory). Esempio: c: \\ temp \\newfile.txt.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) se il file è stato rinominato correttamente e qualsiasi altro numero per indicare un errore.

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

Il file system non è NTFS.

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

Per rinominare una cartella, eseguire prima l'associazione alla cartella in questione e quindi chiamare il metodo Rename. Come unico parametro per il metodo , passare il nuovo nome per la cartella come nome di percorso completo. Ad esempio, se la cartella in C: Scripts Logs Backup deve essere rinominata C: Scripts Archive, è necessario passare C: Scripts Archive come nome completo \\ \\ della \\ \\ \\ \\ \\ cartella. Se si passa solo il nome della cartella Archive, viene generato un errore di percorso non valido.

La classe Directory Win32 non fornisce un metodo in un unico passaggio per \_ lo spostamento di cartelle. Al contrario, lo spostamento di una cartella comporta in genere due passaggi:

<dl> 1. Copia della cartella nel nuovo percorso  
2. Eliminazione della cartella originale  
</dl>

L'unica eccezione a questo processo in due passaggi prevede lo spostamento di una cartella in un nuovo percorso nella stessa unità. Si supponga, ad esempio, di voler spostare C: \\ Temp in C: \\ Scripts Temporary \\ Files \\ Archive. Se il percorso corrente e il nuovo percorso sono nella stessa unità, è possibile spostare la cartella semplicemente chiamando il metodo Rename e passando il nuovo percorso come parametro del metodo . Questo approccio consente di spostare la cartella in un unico passaggio. Tuttavia, lo script ha esito negativo se l'unità corrente e la nuova unità sono diverse. Un tentativo di rinominare C: Temp in D: Temp ha esito negativo e viene visualizzato l'errore \\ \\ "Drive not the same" (Unità non uguale).

## <a name="examples"></a>Esempio

Il codice seguente, dall'esempio di spostamento di una cartella tramite [WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript nella raccolta TechNet, usa il metodo Rename per spostare la cartella C: \\ Scripts in C: \\ Admins Documents Archive \\ \\ \\ VBScript.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery _ 
    ("Select * from Win32_Directory where name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename("C:\Admins\Documents\Archive\VBScript") 
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
</dt> </dl>

 

