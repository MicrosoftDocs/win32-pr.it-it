---
description: Comprime il file di codec logico (o directory) specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo Compress).
ms.assetid: e1ecf0de-3b81-443e-9936-326d7d2d9210
ms.tgt_platform: multiple
title: Metodo CompressEx della classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ce8e659aba52bc04173aab450be2c6cd03e47ccbf2b9f3476ce55ddbe315ab90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547531"
---
# <a name="compressex-method-of-the-win32_codecfile-class"></a>Metodo CompressEx della classe CodecFile Win32 \_

Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CompressEx** comprime il file di codec logico (o directory) specificato nel percorso dell'oggetto (questo metodo è una versione estesa del [**metodo Compress).**](compress-method-in-class-win32-directory.md)

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StopFileName* \[ Cambio\]
</dt> <dd>

Nome del file o della directory in cui il **metodo CompressEx non** è riuscito. Questo parametro sarà **Null se** il metodo ha esito positivo.

</dd> <dt>

*StartFileName* \[ in, facoltativo\]
</dt> <dd>

Denota il file o la directory figlio da usare come punto di partenza per **CompressEx.** Il *parametro StartFileName* è in genere il *parametro StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente. Se questo parametro è **NULL,** l'operazione viene eseguita sul file o sulla directory specificata nella chiamata **ExecMethod.**

</dd> <dt>

*Ricorsivo* \[ in, facoltativo\]
</dt> <dd>

Se **true,** la modifica della proprietà verrà applicata in modo ricorsivo ai file e alle directory all'interno della directory specificata [**dall'istanza di CIM \_ LogicalFile.**](cim-logicalfile.md) Nota: per le istanze di file, *il parametro di* input ricorsivo viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) se il file è stato compresso correttamente e qualsiasi altro numero per indicare un errore.

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

[**Win32 \_ CodecFile**](win32-codecfile.md)
</dt> </dl>

 

