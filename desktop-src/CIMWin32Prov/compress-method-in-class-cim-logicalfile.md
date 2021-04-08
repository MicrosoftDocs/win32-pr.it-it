---
description: Il metodo Compress comprime il file o la directory logica specificata nel percorso dell'oggetto.
ms.assetid: 4a26beaf-388b-4f37-b4ee-ef3a7d15d2b6
ms.tgt_platform: multiple
title: Metodo Compress della classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 12938001d62920916e75d70ad632170c3e92bd51
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877373"
---
# <a name="compress-method-of-the-cim_logicalfile-class"></a>Metodo Compress della classe CIM \_ LogicalFile

Il metodo **Compress comprime** il file o la directory logica specificata nel percorso dell'oggetto.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Compress();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

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

[\_LOGICALFILE CIM](compress-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> </dl>

 

