---
description: Ottiene la proprietà del file del dispositivo logico specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo TakeOwnerShip ed è ereditato da CIM \_ LogicalFile.
ms.assetid: 084f755a-e837-4d21-8bd2-0f63f80302fc
ms.tgt_platform: multiple
title: Metodo TakeOwnerShipEx della classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e129bfb5347c958e678214de88c740ef194559882be7a6f02378d0af000370cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922891"
---
# <a name="takeownershipex-method-of-the-cim_devicefile-class"></a>Metodo TakeOwnerShipEx della classe \_ CIM DeviceFile

Il **metodo TakeOwnerShipEx** ottiene la proprietà del file del dispositivo logico specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del [**metodo TakeOwnerShip**](takeownership-method-in-class-cim-devicefile.md) ed è ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md). Se il file logico è una directory, questo metodo agisce in modo ricorsivo, assumendo la proprietà di tutti i file e delle sottodirectory contenuti nella directory.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 TakeOwnerShipEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StopFileName* \[ Cambio\]
</dt> <dd>

Stringa che rappresenta il nome del file (o della directory) in cui il metodo ha avuto esito negativo. Questo parametro è **Null se** il metodo ha esito positivo.

</dd> <dt>

*StartFileName* \[ Pollici\]
</dt> <dd>

Stringa che rappresenta il file figlio (o directory) da utilizzare come punto di partenza per questo metodo. In genere, il *parametro StartFileName* è il *parametro StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente. Se questo parametro è **Null,** l'operazione viene eseguita sul file o sulla directory specificata nella chiamata **ExecMethod.**

</dd> <dt>

*Ricorsivo* \[ Pollici\]
</dt> <dd>

Se **TRUE,** il metodo viene applicato in modo ricorsivo anche ai file e alle directory all'interno della directory specificata [**dall'istanza di CIM \_ DeviceFile.**](cim-devicefile.md) Per le istanze di file, questo parametro viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.

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

File system non NTFS.

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

[CIM \_ DeviceFile](takeownershipex-method-in-class-cim-devicefile.md)
</dt> <dt>

[**CIM \_ DeviceFile**](cim-devicefile.md)
</dt> </dl>

 

