---
description: Copia il file o la directory logica specificata nel percorso dell'oggetto nel percorso specificato dal parametro FileName.
ms.assetid: 534d8b73-fc22-4a42-b8e6-24a54353bb14
ms.tgt_platform: multiple
title: Metodo CopyEx della classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ec7c44ec3fc01074a0f4af70249236aa366d64bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305294"
---
# <a name="copyex-method-of-the-cim_logicalfile-class"></a>Metodo CopyEx della classe CIM \_ LogicalFile

Il metodo **CopyEx** copia il file logico o la directory specificata nel percorso dell'oggetto nella posizione specificata dal parametro *filename* . Una copia non è supportata se è necessario sovrascrivere un file logico esistente. Questo metodo è una versione estesa del metodo [**Copy**](copy-method-in-class-cim-logicalfile.md) .

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

Nome completo del file di destinazione (o directory).

Esempio: "c: \\ temp \\ NewDirectory"

</dd> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo. Questo parametro è **null** se il metodo ha esito positivo.

</dd> <dt>

*StartFileName* \[ in, facoltativo\]
</dt> <dd>

Stringa che assegna un nome al file figlio (o alla directory) da utilizzare come punto di partenza per questo metodo. In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente. Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificata nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

</dd> <dt>

*Ricorsivo* \[ in, facoltativo\]
</dt> <dd>

Se è TRUE, anche il metodo viene applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza [**CIM \_ LogicalFile**](cim-logicalfile.md) . Per le istanze di file, questo parametro viene ignorato.

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

[\_LOGICALFILE CIM](copyex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> </dl>

 

