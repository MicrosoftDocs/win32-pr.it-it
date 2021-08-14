---
description: Copia il file di voce di directory logica o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input.
ms.assetid: 038e23d7-71db-4db6-8fb1-e84e972510c9
ms.tgt_platform: multiple
title: Metodo Copy della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 85a16d3e63ef46ad2c536103a4e462a3e830e17f56f83cdcf39bbad5a33ebb23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118419756"
---
# <a name="copy-method-of-the-win32_directory-class"></a>Metodo Copy della classe Directory Win32 \_

Il **metodo copia** [la](/windows/desktop/WmiSdk/retrieving-a-class) voce di directory logica o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro di input. Una copia non è supportata se è necessario sovrascrivere un file logico esistente.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FileName* 
</dt> <dd>

Nome completo della copia del file (o directory). Esempio: c: \\ temp \\ newdirectory

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) se il file è stato copiato correttamente e qualsiasi altro numero per indicare un errore.

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

Le cartelle devono spesso essere copiate da un percorso a un altro. Ad esempio, è possibile copiare una cartella da un server a un altro per creare una copia di backup di tale cartella. Oppure si potrebbe avere una cartella templates che deve essere copiata nelle workstation utente o una cartella di script che deve essere copiata in tutti i server DNS.

Il metodo Win32 Directory Copy consente di copiare una cartella da un percorso a un altro, nello stesso computer (ad esempio, copiando una cartella dall'unità C all'unità D) o in un \_ computer remoto. Per copiare una cartella, si restituisce un'istanza della cartella da copiare e quindi si chiama il metodo Copy, passando come parametro il percorso di destinazione per la nuova copia della cartella. Ad esempio, questa riga di codice copia una cartella nella cartella Scripts nell'unità F:

`objFolder.Copy("F:\Scripts")`

WMI non sovrascriverà una cartella esistente durante l'esecuzione del metodo Copy. Ciò significa che l'operazione di copia ha esito negativo se la cartella di destinazione esiste. Si supponga, ad esempio, di avere una cartella denominata Scripts e di provare a copiare tale cartella in una condivisione remota denominata \\ \\ atl-fs-01 \\ archive. Se nella condivisione esiste già una cartella denominata Scripts, l'operazione di copia non riesce.

## <a name="examples"></a>Esempio

L'esempio di codice seguente, tratto da Copia una cartella tramite [WMI,](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2)usa il metodo Copy per copiare la cartella C: \\ Scripts in D: \\ Archive.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery( _ 
    "Select * from Win32_Directory where Name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy("D:\Archive") 
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

 

