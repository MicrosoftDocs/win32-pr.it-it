---
description: Modifica le autorizzazioni di sicurezza per il file codec specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo ChangeSecurityPermissions).
ms.assetid: 3eac4ae1-3c0e-4e81-8b23-9ad8698f723c
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissionsEx della Win32_CodecFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3a025bd9be527237b16022d6544f024e6aa10d294637b16de1df31e43cfa830b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119323081"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_codecfile-class"></a>Metodo ChangeSecurityPermissionsEx della classe CodecFile Win32 \_

Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** modifica le autorizzazioni di sicurezza per il file codec specificato nel percorso dell'oggetto (questo metodo è una versione estesa del [**metodo ChangeSecurityPermissions).**](changesecuritypermissions-method-in-class-win32-directory.md) Se il file logico è una directory, questo metodo è ricorsivo e modifica le autorizzazioni di sicurezza di tutti i file e le sottodirectory contenuti nella directory.

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

*SecurityDescriptor* \[ Pollici\]
</dt> <dd>

Espressione che viene risolta in un'istanza di [**Win32 \_ SecurityDescriptor.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Questo descrittore contiene nuove autorizzazioni di sicurezza per l'istanza di [**\_ CodecFile Win32.**](win32-codecfile.md)

</dd> <dt>

*Opzione* \[ Pollici\]
</dt> <dd>

Privilegi di sicurezza effettivi da modificare. Ad esempio, per modificare la sicurezza dell'elenco di controllo di accesso discrezionale (DACL) e del proprietario, usare quanto segue:

`Option = 1 + 4`

-oppure-

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**MODIFICA \_ INFORMAZIONI \_ DI \_ SICUREZZA DEL** PROPRIETARIO (1 (0x1))


</dt> <dd>

Modificare il proprietario del file logico.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**MODIFICA \_ INFORMAZIONI \_ SULLA \_ SICUREZZA DEI** GRUPPI (2 (0x2))


</dt> <dd>

Modificare il gruppo del file logico.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**MODIFICA \_ INFORMAZIONI DI SICUREZZA DACL \_ \_** (4 (0x4))


</dt> <dd>

Modificare l'elenco di controllo di accesso discrezionale (DACL) del file logico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**MODIFICA \_ INFORMAZIONI DI \_ SICUREZZA SACL \_** (8 (0x8))


</dt> <dd>

Modificare l'elenco di controllo di accesso di sistema (SACL) del file logico.

</dd> </dl> </dd> <dt>

*StopFileName* \[ Cambio\]
</dt> <dd>

Nome del file o della directory in cui il **metodo ChangeSecurityPermissionsEx** non è riuscito. Questo parametro è Null quando il metodo ha esito positivo.

</dd> <dt>

*StartFileName* \[ in, facoltativo\]
</dt> <dd>

Specifica il file o la directory figlio da usare come punto di partenza **per ChangeSecurityPermissionsEx.** In genere, il *parametro StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente. Se questo parametro è Null, l'operazione viene eseguita sul file o sulla directory specificata nella [**chiamata a ExecMethod.**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-execmethod)

</dd> <dt>

*Ricorsivo* \[ in, facoltativo\]
</dt> <dd>

Se **true,** le modifiche di proprietà vengono applicate in modo ricorsivo ai file e alle directory nella directory specificata [**dall'istanza \_ LogicalFile di CIM.**](cim-logicalfile.md) Per le istanze di file, *il parametro di* input Ricorsivo viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) se le autorizzazioni vengono modificate e un numero diverso per indicare un errore.

<dl> <dt>

**Success**
</dt> <dd>

0

La richiesta ha esito positivo.

</dd> <dt>

**Accesso negato**
</dt> <dd>

2

Accesso negato.

</dd> <dt>

**Errore non specificato**
</dt> <dd>

8

Si è verificato un errore non specificato.

</dd> <dt>

**Oggetto non valido**
</dt> <dd>

9

Il nome specificato non è valido.

</dd> <dt>

**L'oggetto esiste già**
</dt> <dd>

10

L'oggetto specificato esiste già.

</dd> <dt>

**File system non NTFS**
</dt> <dd>

11

Il file system non è un file system NTFS.

</dd> <dt>

**Piattaforma non NT/Windows 2000**
</dt> <dd>

12

La piattaforma non è Windows NT o Windows 2000.

</dd> <dt>

**Unità non uguale**
</dt> <dd>

13

L'unità non è la stessa.

</dd> <dt>

**Directory non vuota**
</dt> <dd>

14

La directory non è vuota.

</dd> <dt>

**Violazione di condivisione**
</dt> <dd>

15

Si è verificata una violazione di condivisione.

</dd> <dt>

**File di avvio non valido**
</dt> <dd>

16

Il file iniziale specificato non è valido.

</dd> <dt>

**Privilegio non mantenuto**
</dt> <dd>

17

Un privilegio necessario per l'operazione non viene mantenuto.

</dd> <dt>

**Parametro non valido**
</dt> <dd>

21

Un parametro specificato non è valido.

</dd> </dl>

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

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ CodecFile**](win32-codecfile.md)
</dt> </dl>

 

