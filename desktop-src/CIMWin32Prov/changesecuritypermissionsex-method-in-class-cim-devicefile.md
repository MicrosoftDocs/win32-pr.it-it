---
description: Modifica le autorizzazioni di sicurezza per il file del dispositivo specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo ChangeSecurityPermissions).
ms.assetid: 5ad54470-6961-4c0d-9d2a-d3eaf81d75f4
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissionsEx della classe CIM_DeviceFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6c6d70c11077873154040e30cabfb460546f79b1088ff124884e35f3698aaf78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959140"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_devicefile-class"></a>Metodo ChangeSecurityPermissionsEx della classe \_ CIM DeviceFile

Il **metodo ChangeSecurityPermissionsEx** modifica le autorizzazioni di sicurezza per il file del dispositivo specificato nel percorso dell'oggetto (questo metodo è una versione estesa del [**metodo ChangeSecurityPermissions).**](changesecuritypermissions-method-in-class-cim-devicefile.md) Se il file logico è una directory, questo metodo agisce in modo ricorsivo, modificando le autorizzazioni di sicurezza per tutti i file e le sottodirectory contenuti nella directory. Questo metodo viene ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md).

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 ChangeSecurityPermissionsEx(
  [in]           Win32_SecurityDescriptor SecurityDescriptor,
  [in]           uint32                   Option,
  [out]          string                   StopFileName,
  [in, optional] string                   StartFileName,
  [in, optional] boolean                  Recursive
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Descrittore di sicurezza* \[ Pollici\]
</dt> <dd>

Specifica le informazioni di sicurezza.

> [!Caution]  
> Un ACL **NULL** nella struttura [**SECURITY \_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede l'accesso illimitato.

 

</dd> <dt>

*Opzione* \[ Pollici\]
</dt> <dd>

Privilegio di sicurezza da modificare. Ad esempio, per modificare il proprietario e la sicurezza DACL, usare

`Option = 1 + 4`

oppure

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**MODIFICA \_ INFORMAZIONI \_ DI SICUREZZA DEL \_ PROPRIETARIO** (1)


</dt> <dd>

Modificare il proprietario del file logico.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**MODIFICA \_ INFORMAZIONI \_ SULLA SICUREZZA DEL \_ GRUPPO** (2)


</dt> <dd>

Modificare il gruppo del file logico.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**MODIFICA \_ INFORMAZIONI DI \_ SICUREZZA \_ DACL** (4)


</dt> <dd>

Modificare l'ACL del file logico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**MODIFICA \_ INFORMAZIONI DI \_ SICUREZZA \_ SACL** (8)


</dt> <dd>

Modificare l'ACL di sistema del file logico.

</dd> </dl> </dd> <dt>

*StopFileName* \[ Cambio\]
</dt> <dd>

Stringa che rappresenta il nome del file (o della directory) in cui il metodo ha avuto esito negativo. Questo parametro è **Null se** il metodo ha esito positivo.

</dd> <dt>

*StartFileName* \[ in, facoltativo\]
</dt> <dd>

File figlio (o directory) da utilizzare come punto di partenza per questo metodo. In genere, il *parametro StartFileName* è il *parametro StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente. Se questo parametro è **Null,** l'operazione viene eseguita sul file (o directory) specificato nella [**chiamata ExecMethod.**](/windows/desktop/WmiSdk/swbemservices-execmethod)

</dd> <dt>

*Ricorsivo* \[ in, facoltativo\]
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

[CIM \_ DeviceFile](changesecuritypermissionsex-method-in-class-cim-devicefile.md)
</dt> <dt>

[**CIM \_ DeviceFile**](cim-devicefile.md)
</dt> </dl>

 

