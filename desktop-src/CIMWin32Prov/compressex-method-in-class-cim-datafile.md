---
description: "Metodo CompressEx della classe CIM_DataFile : usa la compressione NTFS per comprimere il file logico (o la directory) specificato nel percorso dell'oggetto. Questo metodo viene ereditato da CIM \\_ LogicalFile."
ms.assetid: 553b6a90-d16c-4abb-9015-66fe8e1606f6
ms.tgt_platform: multiple
title: Metodo CompressEx della classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ccc155c04c6c25f38050bd37827eb0c2e2e0e73e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089789"
---
# <a name="compressex-method-of-the-cim_datafile-class"></a>Metodo CompressEx della classe \_ CiM DataFile

Il **metodo CompressEx** usa la compressione NTFS per comprimere il file logico (o la directory) specificato nel percorso dell'oggetto. Questo metodo viene ereditato da [**CIM \_ LogicalFile.**](cim-logicalfile.md) Questo metodo è una versione estesa del [**metodo Compress**](compress-method-in-class-cim-datafile.md) ed è ereditato da [CIM \_ LogicalFile.](/windows/desktop/WmiSdk/calling-a-method)

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 CompressEx(
  [out] string  StopFileName,
  [in]  string  StartFileName,
  [in]  boolean Recursive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StopFileName* \[ Cambio\]
</dt> <dd>

Stringa che rappresenta il nome del file (o directory) in cui il metodo non è riuscito. Questo parametro è Null se il metodo ha esito positivo.

</dd> <dt>

*StartFileName* \[ Pollici\]
</dt> <dd>

Stringa che rappresenta il file figlio (o la directory) da usare come punto di partenza per questo metodo. In genere, il *parametro StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente. Se questo parametro è Null, l'operazione viene eseguita sul file o sulla directory specificata nella **chiamata a ExecMethod.**

Se *si usa StartFileName,* *anche Recursive* deve essere impostato su true.

</dd> <dt>

*Ricorsivo* \[ Pollici\]
</dt> <dd>

Se **TRUE,** il metodo viene applicato in modo ricorsivo anche ai file e alle directory all'interno della directory specificata [**dall'istanza di CIM \_ DataFile.**](cim-datafile.md) Per le istanze di file, questo parametro viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore. Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Operazione completata.

</dd> <dt>

**2**
</dt> <dd>

Accesso negato.

</dd> <dt>

**8**
</dt> <dd>

Errore non specificato.

</dd> <dt>

**9**
</dt> <dd>

Oggetto non valido.

</dd> <dt>

**10**
</dt> <dd>

Oggetto già esistente.

</dd> <dt>

**11**
</dt> <dd>

File system non NTFS.

</dd> <dt>

**12**
</dt> <dd>

Piattaforma non Windows.

</dd> <dt>

**13**
</dt> <dd>

L'unità non è la stessa.

</dd> <dt>

**14**
</dt> <dd>

Directory non vuota.

</dd> <dt>

**15**
</dt> <dd>

Violazione di condivisione.

</dd> <dt>

**16**
</dt> <dd>

File di avvio non valido.

</dd> <dt>

**17**
</dt> <dd>

Privilegio non mantenuto.

</dd> <dt>

**21**
</dt> <dd>

Parametro non valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **metodo CompressEx** in [**CIM \_ DataFile**](cim-datafile.md) viene implementato da WMI.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

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

[CIM \_ DataFile](compressex-method-in-class-cim-datafile.md)
</dt> <dt>

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dt>

[Attività WMI: File e cartelle](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Costanti dei diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

