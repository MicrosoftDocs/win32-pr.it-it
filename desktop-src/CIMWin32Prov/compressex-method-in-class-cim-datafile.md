---
description: Usa la compressione NTFS per comprimere il file o la directory logica specificata nel percorso dell'oggetto. Questo metodo viene ereditato da \_ LOGICALFILE CIM.
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
ms.openlocfilehash: 070a15a0fb134c92e7c436e071e09b7cc09fa5dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225553"
---
# <a name="compressex-method-of-the-cim_datafile-class"></a>Metodo CompressEx della classe del file di \_ DataFile CIM

Il metodo **CompressEx** utilizza la compressione NTFS per comprimere il file o la directory logica specificata nel percorso dell'oggetto. Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md). Questo metodo è una versione estesa del metodo [**Compress**](compress-method-in-class-cim-datafile.md) ed è ereditato da [CIM \_ LogicalFile](/windows/desktop/WmiSdk/calling-a-method).

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

*StopFileName* \[ out\]
</dt> <dd>

Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo. Questo parametro è null se il metodo ha esito positivo.

</dd> <dt>

*StartFileName* \[ in\]
</dt> <dd>

Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per questo metodo. In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente. Se questo parametro è null, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata **ExecMethod** .

Se si usa *StartFileName* , è necessario impostare *ricorsivo* su true.

</dd> <dt>

*Ricorsivo* \[ in\]
</dt> <dd>

Se **true**, il metodo viene anche applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza di [**\_ DataFile DataFile**](cim-datafile.md) . Per le istanze di file, questo parametro viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**0**
</dt> <dd>

Esito positivo.

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

File System non NTFS.

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

Il metodo **CompressEx** nel file di [**\_ DataFile CIM**](cim-datafile.md) viene implementato da WMI.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

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

[File di \_ DataFile CIM](compressex-method-in-class-cim-datafile.md)
</dt> <dt>

[**File di \_ DataFile CIM**](cim-datafile.md)
</dt> <dt>

[Attività WMI: file e cartelle](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Costanti dei diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

