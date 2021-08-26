---
description: Decomprime il file di dati logico (o directory) specificato nel percorso dell'oggetto. Questo metodo viene ereditato da CIM \_ LogicalFile.
ms.assetid: 0966ba13-8bbc-4283-919a-7675444409be
ms.tgt_platform: multiple
title: Decomprimere il metodo della CIM_DataFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c5d2f1a475800506dadc8929079ecb2549d59bfd838f340c56e5f763aa9af24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002891"
---
# <a name="uncompress-method-of-the-cim_datafile-class"></a>Metodo Uncompress della classe \_ CiM DataFile

Il **metodo Uncompress** decomprime il file di dati logico (o directory) specificato nel percorso dell'oggetto. Questo metodo viene ereditato da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene Managed Object Format sintassi MOF (Managed Object Format). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Uncompress();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore. Per altri codici di errore, [**vedere Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)

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

Unità non uguale.

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

Il **metodo Uncompress** in [**CIM \_ DataFile viene**](cim-datafile.md) implementato da WMI.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

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

[**CIM \_ DataFile**](uncompress-method-in-class-cim-datafile.md)
</dt> <dt>

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dt>

[Attività WMI: File e cartelle](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Costanti per i diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

