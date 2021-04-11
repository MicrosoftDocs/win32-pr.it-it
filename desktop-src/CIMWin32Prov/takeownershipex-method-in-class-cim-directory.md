---
description: Ottiene la proprietà del file di voce della directory logica specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo TakeOwnerShip e viene ereditato da CIM \_ LogicalFile.
ms.assetid: a13acaa2-2203-470a-b989-15f8276e46c6
ms.tgt_platform: multiple
title: Metodo TakeOwnerShipEx della classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b02a6c40e99405c150a372f8eb15fe648f2df60a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126003"
---
# <a name="takeownershipex-method-of-the-cim_directory-class"></a>Metodo TakeOwnerShipEx della classe di \_ directory CIM

Il metodo **TakeOwnerShipEx** ottiene la proprietà del file di voce della directory logica specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo [**TakeOwnership**](takeownership-method-in-class-cim-directory.md) e viene ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md). Se il file logico è una directory, questo metodo agisce in modo ricorsivo, assumendo la proprietà di tutti i file e le sottodirectory contenuti nella directory.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

*StopFileName* \[ out\]
</dt> <dd>

Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo. Questo parametro è null se il metodo ha esito positivo.

</dd> <dt>

*StartFileName* \[ in\]
</dt> <dd>

Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per questo metodo. In genere, questo parametro è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente. Se questo parametro è null, l'operazione viene eseguita sul file o sulla directory specificati nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

</dd> <dt>

*Ricorsivo* \[ in\]
</dt> <dd>

Se **true**, il metodo viene applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza di [**\_ directory CIM**](cim-directory.md) . Per le istanze di file, questo parametro viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 in caso di esito positivo e qualsiasi altro numero per indicare un errore.

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

La piattaforma non è Windows.

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

## <a name="examples"></a>Esempio

Il codice di script seguente Visual Basic chiama il metodo **TakeOwnerShipEx** per assumere la proprietà della cartella C: \\ Temp.


```VB
strComputer = "." 
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\CIMV2") 
' Obtain the definition of the class.
Set objShare = objWMIService.Get("Win32_Directory")
' Obtain an InParameters object specific
' to the method.
Set objInParam = objShare.Methods_("TakeOwnerShipEx"). _
    inParameters.SpawnInstance_()

' Add the input parameters.
objInParam.Properties_.Item("Recursive") =  true

' Execute the method and obtain the return status.
' The OutParameters object in objOutParams
' is created by the provider.
Set objOutParams = objWMIService.ExecMethod( _
    "Win32_Directory.Name='C:\Temp'", "TakeOwnerShipEx", objInParam)
wscript.echo objOutParams.ReturnValue
```



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

[\_Directory CIM](takeownershipex-method-in-class-cim-directory.md)
</dt> <dt>

[**\_Directory CIM**](cim-directory.md)
</dt> </dl>

 

