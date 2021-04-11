---
description: Il metodo Rename Rinomina il file o la directory logica specificata nel percorso dell'oggetto. La ridenominazione non è supportata se la destinazione si trova in un'altra unità o se è necessario sovrascrivere un file logico esistente.
ms.assetid: 5a62ff64-d1d2-43a2-997c-0ad46896b31f
ms.tgt_platform: multiple
title: Rinominare il metodo della classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0da38020d7b22dceb6f1d061f8feaf858eeb5f04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127366"
---
# <a name="rename-method-of-the-cim_logicalfile-class"></a>Rinominare il metodo della \_ classe CIM LogicalFile

Il metodo **Rename Rinomina** il file o la directory logica specificata nel percorso dell'oggetto. La ridenominazione non è supportata se la destinazione si trova in un'altra unità o se è necessario sovrascrivere un file logico esistente.

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

Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.

<dl> <dt>

**Success**
</dt> <dd>

0

Esito positivo.

</dd> <dt>

**Accesso negato**
</dt> <dd>

2

Accesso negato.

</dd> <dt>

**Errore non specificato**
</dt> <dd>

8

Errore non specificato.

</dd> <dt>

**Oggetto non valido**
</dt> <dd>

9

Oggetto non valido.

</dd> <dt>

**Oggetto già esistente**
</dt> <dd>

10

Oggetto già esistente.

</dd> <dt>

**File System non NTFS**
</dt> <dd>

11

File System non NTFS.

</dd> <dt>

**Piattaforma non NT/Windows 2000**
</dt> <dd>

12

Piattaforma non Windows.

</dd> <dt>

**Unità non uguale**
</dt> <dd>

13

L'unità non è la stessa.

</dd> <dt>

**Directory non vuota**
</dt> <dd>

14

Directory non vuota.

</dd> <dt>

**Violazione di condivisione**
</dt> <dd>

15

Violazione di condivisione.

</dd> <dt>

**File di avvio non valido**
</dt> <dd>

16

File di avvio non valido.

</dd> <dt>

**Privilegio non mantenuto**
</dt> <dd>

17

Privilegio non mantenuto.

</dd> <dt>

**Parametro non valido**
</dt> <dd>

21

Parametro non valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo metodo non è attualmente implementato da WMI. Per usare questo metodo, è necessario implementarlo nel proprio provider.

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

[\_LOGICALFILE CIM](rename-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> </dl>

 

