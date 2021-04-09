---
description: Copia il file o la directory della voce di directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro FileName. Questo metodo è una versione estesa del metodo Copy.
ms.assetid: c15bd1ae-a60d-4875-a76e-99486820c42c
ms.tgt_platform: multiple
title: Metodo CopyEx della classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55f2fdb0aa4e8306e8ec0aa4f5f265c0a8ee6689
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878401"
---
# <a name="copyex-method-of-the-win32_directory-class"></a>Metodo CopyEx della classe di \_ directory Win32

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CopyEx** copia il file di voce della directory logica o la directory specificata nel percorso dell'oggetto nel percorso specificato dal parametro *filename* . Questo metodo è una versione estesa del metodo [**Copy**](copy-method-in-class-win32-directory.md) . Una copia non è supportata se è necessario sovrascrivere un file logico esistente.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome file* \[ in\]
</dt> <dd>

Nome completo della copia del file (o directory). Esempio: c: \\ temp \\ NewDirectory.

</dd> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Nome del file o della directory in cui il metodo **CopyEx** non è riuscito. Questo parametro sarà **null** se il metodo ha esito positivo.

</dd> <dt>

*StartFileName* \[ in, facoltativo\]
</dt> <dd>

Denomina il file o la directory figlio da utilizzare come punto di partenza per **CopyEx**. Il parametro *StartFileName* è in genere il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente. Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata **ExecMethod** .

Se si usa *StartFileName* , è necessario impostare *ricorsivo* su true.

</dd> <dt>

*Ricorsivo* \[ in, facoltativo\]
</dt> <dd>

Se **true**, i file e le directory vengono copiati in modo ricorsivo all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) .

> [!Note]  
> Per le istanze di file, il parametro di input *ricorsivo* viene ignorato.

 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) se il file è stato copiato correttamente e qualsiasi altro numero per indicare un errore.

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

 

