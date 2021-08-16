---
description: Decomprime il file di voce di directory logica (o directory) specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del metodo Uncompress ed è ereditato da CIM \_ LogicalFile.
ms.assetid: ef5b7c90-5013-4ec0-bfa6-c32428ffb501
ms.tgt_platform: multiple
title: Metodo UncompressEx della classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 95a4c6e98543afa17e98865463b0dc22cccbd0e43eef9a996f659b6cfce4b510
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117834526"
---
# <a name="uncompressex-method-of-the-cim_directory-class"></a>Metodo UncompressEx della classe Directory CIM \_

Il **metodo UncompressEx** decomprime il file di voce di directory logica (o directory) specificato nel percorso dell'oggetto. Questo metodo è una versione estesa del [**metodo Uncompress**](uncompress-method-in-class-cim-directory.md) ed è ereditato da [**CIM \_ LogicalFile.**](cim-logicalfile.md)

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 UncompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StopFileName* \[ Cambio\]
</dt> <dd>

Stringa che rappresenta il nome del file (o directory) in cui il metodo non è riuscito. Questo parametro è **Null se** il metodo ha esito positivo.

</dd> <dt>

*StartFileName* \[ Pollici\]
</dt> <dd>

Stringa che rappresenta il file figlio (o la directory) da usare come punto di partenza per questo metodo. In genere, questo parametro è il *parametro StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente. Se questo parametro è **Null,** l'operazione viene eseguita sul file o sulla directory specificata nella [**chiamata a ExecMethod.**](/windows/desktop/WmiSdk/swbemservices-execmethod)

</dd> <dt>

*Ricorsivo* \[ Pollici\]
</dt> <dd>

Se **TRUE,** il metodo viene applicato in modo ricorsivo ai file e alle directory all'interno della directory specificata [**dall'istanza della \_ directory CIM.**](cim-directory.md) Per le istanze di file, questo parametro viene ignorato.

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

Unità non uguale.

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

[**CIM \_ Directory**](uncompressex-method-in-class-cim-directory.md)
</dt> <dt>

[**CIM \_ Directory**](cim-directory.md)
</dt> </dl>

 

