---
description: Rinomina il file di voce di directory specificato nel percorso dell'oggetto.
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Rinominare il metodo della classe Win32_Directory
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
ms.openlocfilehash: 874151e1ff8c9feca375df3eb441665863d1070d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304437"
---
# <a name="rename-method-of-the-win32_directory-class"></a>Rinominare il metodo della \_ classe di directory Win32

Il metodo **Rinomina** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) Rinomina il file di voce di directory specificato nel percorso dell'oggetto. Una ridenominazione non è supportata se la destinazione si trova in un'altra unità o se è necessario sovrascrivere un file logico esistente.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

Nome completo del nuovo file (o directory). Esempio: c: \\ temp \\newfile.txt.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) se il file è stato rinominato correttamente e qualsiasi altro numero per indicare un errore.

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

Il file di avvio specificato non è valido.

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

Per rinominare una cartella, eseguire prima l'associazione alla cartella in questione, quindi chiamare il metodo Rename. Come unico parametro del metodo, passare il nuovo nome per la cartella come nome di percorso completo. Se, ad esempio, la cartella del backup dei log di C: \\ Scripts deve \\ \\ essere rinominata c: \\ Scripts \\ Archive, è necessario passare c: \\ Scripts \\ Archive come nome completo della cartella. Passando solo il nome della cartella-Archive-viene restituito un errore di percorso non valido.

La \_ classe di directory Win32 non fornisce un metodo in un unico passaggio per lo trasferimento di cartelle. Il trasferimento di una cartella prevede in genere due passaggi:

<dl> 1. Copia della cartella nella nuova posizione  
2. Eliminazione della cartella originale  
</dl>

L'unica eccezione a questo processo in due passaggi prevede lo spostamento di una cartella in una nuova posizione nella stessa unità. Si supponga, ad esempio, di voler spostare l' \\ Archivio c: Temp in c: \\ script per \\ i file temporanei \\ . Fino a quando la posizione corrente e la nuova posizione si trovano nella stessa unità, è possibile spostare la cartella semplicemente chiamando il metodo Rename e passando la nuova posizione come parametro del metodo. Questo approccio consente di spostare la cartella in un unico passaggio. Tuttavia, lo script ha esito negativo se l'unità corrente e la nuova unità sono diverse. Il tentativo di rinominare C: \\ Temp in D: \\ Temp ha esito negativo con un errore "unità non uguale".

## <a name="examples"></a>Esempio

Il codice seguente, dall'esempio [Move a folder using WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript in TechNet Gallery, usa il metodo Rename per spostare la cartella c: \\ Scripts in c: \\ Admins \\ Documents \\ Archive \\ VBScript.


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
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Directory Win32**](win32-directory.md)
</dt> </dl>

 

