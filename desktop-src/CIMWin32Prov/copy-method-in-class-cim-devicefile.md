---
description: "Metodo Copy della classe CIM_DeviceFile: il metodo Copy copia il file logico (o la directory) specificato nel percorso dell'oggetto nel percorso specificato dal parametro di input."
ms.assetid: 6c1c6172-80a2-4779-903a-935f8c7091a5
ms.tgt_platform: multiple
title: Metodo Copy della classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 09c6d0f9400a04cc6e5a8ed4bd49ec7075b3c190
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089802"
---
# <a name="copy-method-of-the-cim_devicefile-class"></a>Metodo Copy della classe CIM \_ DeviceFile

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

Nome completo della copia del file o della directory di destinazione.

Esempio: "c: \\ temp \\ newdirectory"

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.

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

Questo metodo non è attualmente implementato da WMI. Per usare questo metodo, è necessario implementarlo nel proprio provider.

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

[CIM \_ DeviceFile](copy-method-in-class-cim-devicefile.md)
</dt> <dt>

[**CIM \_ DeviceFile**](cim-devicefile.md)
</dt> </dl>

 

