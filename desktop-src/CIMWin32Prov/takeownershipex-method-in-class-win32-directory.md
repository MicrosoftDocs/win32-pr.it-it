---
description: Ottiene la proprietà del file di voci di directory logico specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo TakeOwnerShip.
ms.assetid: 73726207-e885-4957-bff8-6903c4b99278
ms.tgt_platform: multiple
title: Metodo TakeOwnerShipEx della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3893b7acef182005603f4a80a51caf159b54dd31cc2a966d5dc9940a5164681d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118418514"
---
# <a name="takeownershipex-method-of-the-win32_directory-class"></a>Metodo TakeOwnerShipEx della classe Directory Win32 \_

Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** ottiene la proprietà del file di voce di directory logica specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del [**metodo TakeOwnerShip.**](takeownership-method-in-class-win32-directory.md) Se il file logico è effettivamente una directory, questo metodo agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenuti nella directory.

In questo argomento viene Managed Object Format sintassi MOF (Managed Object Format). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StopFileName* \[ Cambio\]
</dt> <dd>

Nome del file o della directory in cui il **metodo TakeOwnerShipEx non** è riuscito. Questo parametro è **NULL** se il metodo ha esito positivo.

</dd> <dt>

*StartFileName* \[ in, facoltativo\]
</dt> <dd>

Nome del file o della directory figlio da usare come punto di partenza per **TakeOwnerShipEx.** Il *parametro StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente. Se questo parametro è **NULL,** l'operazione viene eseguita sul file o sulla directory specificata nella [**chiamata a ExecMethod.**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod)

Se *si usa StartFileName,* *anche Recursive* deve essere impostato su true.

</dd> <dt>

*Ricorsivo* \[ in, facoltativo\]
</dt> <dd>

Se **True,** la modifica della proprietà viene applicata in modo ricorsivo ai file e alle directory all'interno della directory specificata [**dall'istanza di \_ CiM LogicalFile.**](cim-logicalfile.md)

> [!Note]  
> Per le istanze di file, *il parametro di* input Ricorsivo viene ignorato.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore intero pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.

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

## <a name="examples"></a>Esempio

Il codice Visual Basic script seguente chiama il [**metodo TakeOwnerShipEx**](takeownershipex-method-in-class-cim-directory.md) per assumere la proprietà della cartella \\ C: temp.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx").inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod("Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
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

 

