---
description: Il metodo Rename Rinomina il file o la directory logica specificata nel percorso dell'oggetto.
ms.assetid: 3eaf9f4f-270e-41d0-86ae-c5edb1850ef5
ms.tgt_platform: multiple
title: Rinominare il metodo della classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: aea061990a6d3bd52a98dc9101102059767ecf9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127375"
---
# <a name="rename-method-of-the-cim_datafile-class"></a>Rinominare il metodo della classe di file di \_ DataFile CIM

Il metodo **Rename Rinomina** il file o la directory logica specificata nel percorso dell'oggetto. Una ridenominazione non è supportata se la destinazione si trova in un'altra unità o se è necessario sovrascrivere un file logico esistente. Questo metodo viene ereditato da [**\_ LogicalFile CIM**](cim-logicalfile.md).

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome file* \[ in\]
</dt> <dd>

Nome completo del nuovo file (o directory).

Esempio: "c: \\ temp \\newfile.txt"

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 in caso di esito positivo e qualsiasi altro numero per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

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

Il metodo **Rename** in [**CIM \_ DataFile**](cim-datafile.md) viene implementato da WMI.

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

[File di \_ DataFile CIM](rename-method-in-class-cim-datafile.md)
</dt> <dt>

[**File di \_ DataFile CIM**](cim-datafile.md)
</dt> <dt>

[Attività WMI: file e cartelle](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Costanti dei diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

