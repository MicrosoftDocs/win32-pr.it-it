---
description: Il metodo DeleteEx Elimina il file o la directory logica specificata nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo Delete ed è ereditato da CIM \_ LogicalFile.
ms.assetid: 5f924327-248c-47e2-b42e-50c83defce17
ms.tgt_platform: multiple
title: Metodo DeleteEx della classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: aa6427adcc2cf87923b2b76b298cc47373231b56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966069"
---
# <a name="deleteex-method-of-the-cim_directory-class"></a>Metodo DeleteEx della classe di \_ directory CIM

Il metodo **DeleteEx** Elimina il file o la directory logica specificata nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo [**Delete**](delete-method-in-class-cim-directory.md) ed è ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md).

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 DeleteEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName
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

Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per questo metodo. In genere, questo parametro è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente. Se questo parametro è null, l'operazione viene eseguita sul file o sulla directory specificati nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.

<dl> <dt>


</dt> <dd>

0

Esito positivo.

</dd> <dt>


</dt> <dd>

2

Accesso negato.

</dd> <dt>


</dt> <dd>

8

Errore non specificato.

</dd> <dt>


</dt> <dd>

9

Oggetto non valido.

</dd> <dt>


</dt> <dd>

10

Oggetto già esistente.

</dd> <dt>


</dt> <dd>

11

File System non NTFS.

</dd> <dt>


</dt> <dd>

12

Piattaforma non Windows.

</dd> <dt>


</dt> <dd>

13

L'unità non è la stessa.

</dd> <dt>


</dt> <dd>

14

Directory non vuota.

</dd> <dt>


</dt> <dd>

15

Violazione di condivisione.

</dd> <dt>


</dt> <dd>

16

File di avvio non valido.

</dd> <dt>


</dt> <dd>

17

Privilegio non mantenuto.

</dd> <dt>


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

[\_Directory CIM](deleteex-method-in-class-cim-directory.md)
</dt> <dt>

[**\_Directory CIM**](cim-directory.md)
</dt> </dl>

 

