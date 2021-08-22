---
description: Il metodo Copy copia il file logico (o la directory) specificato nel percorso dell'oggetto nel percorso specificato dal parametro di input.
ms.assetid: 13bd7da8-a562-414b-8d23-6f58e1c55878
ms.tgt_platform: multiple
title: Metodo Copy della classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a3f232c35f43cf2baeae3130c115b37c7f47b5c62959523c52b5e7e2a02009e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505041"
---
# <a name="copy-method-of-the-cim_datafile-class"></a>Metodo Copy della classe CIM \_ DataFile

Il **metodo Copy** copia il file logico (o la directory) specificato nel percorso dell'oggetto nel percorso specificato dal parametro di input. Una copia non è supportata se richiede la sovrascrittura di un file logico esistente. Questo metodo viene ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md).

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FileName* \[ Pollici\]
</dt> <dd>

Nome completo del file di destinazione (o directory).

Esempio: "c: \\ temp \\ newdirectory"

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 in caso di esito positivo e qualsiasi altro numero per indicare un errore. Per altri codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

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

Il **metodo Copy** in [**CIM \_ DataFile**](cim-datafile.md) viene implementato da WMI.

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

[CIM \_ DataFile](copy-method-in-class-cim-datafile.md)
</dt> <dt>

[**CIM \_ DataFile**](cim-datafile.md)
</dt> <dt>

[Attività WMI: File e cartelle](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Costanti dei diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

