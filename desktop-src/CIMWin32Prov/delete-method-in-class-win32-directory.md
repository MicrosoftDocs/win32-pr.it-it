---
description: Il metodo Elimina classe WMI eliminerà il file logico (o la directory) specificato nel percorso dell'oggetto.
ms.assetid: 5663b8a8-3089-475b-8a36-454a7315bfca
ms.tgt_platform: multiple
title: Metodo Delete della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2966751c822213025d7107e4eff055900e6c8102711b66329e6f3c4fcbe1ed02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676697"
---
# <a name="delete-method-of-the-win32_directory-class"></a>Metodo Delete della classe Directory Win32 \_

Il **metodo Elimina** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) eliminerà il file logico (o la directory) specificato nel percorso dell'oggetto.

Questo argomento usa la Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Delete();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) se il file è stato eliminato correttamente e qualsiasi altro numero per indicare un errore.

<dl> <dt>

**0**
</dt> <dd>

La richiesta è stata completata.

</dd> <dt>

**2**
</dt> <dd>

L'accesso è stato negato.

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

Le cartelle non sono necessariamente aggiunte permanenti a un file system. A un certo punto, potrebbe essere necessario eliminare le cartelle, ad esempio perché non sono più necessarie, perché il ruolo del computer è cambiato o perché le cartelle sono state create per errore.

Elimina consente di eliminare le cartelle: è sufficiente eseguire il binding alla cartella in questione e quindi chiamare il metodo Delete. Dopo la chiamata al metodo Delete, la cartella viene rimossa definitivamente dal file system; non viene inviato al Cestino. Non viene inoltre emesso alcun avviso di conferma ("Si è certi di voler eliminare questa cartella?"). Al contrario, la cartella viene rimossa immediatamente.

Non è possibile eliminare cartelle di sola lettura usando FileSystemObject. Tuttavia, questa operazione può essere eseguita tramite WMI. Se lo script usa WMI e non si vuole rimuovere una cartella di sola lettura, è necessario usare la proprietà Leggibile per controllare lo stato della cartella prima di eliminarla.

## <a name="examples"></a>Esempio

L'esempio di codice VBScript seguente elimina la cartella C: \\ Scripts.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Delete
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
</dt> </dl>

 

