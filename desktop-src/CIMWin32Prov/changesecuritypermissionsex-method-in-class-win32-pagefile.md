---
description: Modifica le autorizzazioni di sicurezza per il file di paging logico specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo ChangeSecurityPermissions).
ms.assetid: a852a7e6-f26a-4bd9-bb15-e4cdd577697c
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissionsEx della Win32_PageFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c22aaa6552a9879eb08a6e65ce7d5a0651df458252a2a228d7d5acd8b5fb1d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081035"
---
# <a name="changesecuritypermissionsex-method-of-the-win32_pagefile-class"></a>Metodo ChangeSecurityPermissionsEx della classe PageFile Win32 \_

Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissionsEx** modifica le autorizzazioni di sicurezza per il file di paging logico specificato nel percorso dell'oggetto (questo metodo è una versione estesa del [**metodo ChangeSecurityPermissions).**](changesecuritypermissions-method-in-class-win32-directory.md) Se il file logico è una directory, questo metodo è ricorsivo e modifica le autorizzazioni di sicurezza di tutti i file e le sottodirectory contenuti nella directory.

In questo argomento viene Managed Object Format sintassi MOF (Managed Object Format). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

Espressione che si risolve in un'istanza di [**Win32 \_ SecurityDescriptor.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Questo parametro contiene nuove autorizzazioni di sicurezza per l'istanza di [**\_ Win32 PageFile**](win32-pagefile.md).

</dd> <dt>

*Opzione* \[ Pollici\]
</dt> <dd>

Privilegi di sicurezza da modificare. Ad esempio, per modificare la sicurezza dell'elenco di controllo di accesso discrezionale (DACL) e del proprietario, usare quanto segue:

`Option = 1 + 4`

-oppure-

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**MODIFICA \_ INFORMAZIONI \_ DI SICUREZZA DEL \_ PROPRIETARIO** (1)


</dt> <dd>

Modificare il proprietario del file logico.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**MODIFICA \_ INFORMAZIONI \_ SULLA SICUREZZA DEI \_ GRUPPI** (2)


</dt> <dd>

Modificare il gruppo del file logico.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**MODIFICA \_ INFORMAZIONI DI \_ SICUREZZA DACL \_** (4)


</dt> <dd>

Modificare l'elenco DACL del file logico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**MODIFICA \_ INFORMAZIONI DI \_ SICUREZZA SACL \_** (8)


</dt> <dd>

Modificare l'elenco di controllo di accesso di sistema (SACL) del file logico.

</dd> </dl> </dd> <dt>

*StopFileName* \[ Cambio\]
</dt> <dd>

Nome del file o della directory in cui il **metodo ChangeSecurityPermissionsEx** non è riuscito. Questo parametro è **NULL** se il metodo ha esito positivo.

</dd> <dt>

*StartFileName* \[ in, facoltativo\]
</dt> <dd>

Specifica il file o la directory figlio da usare come punto di partenza **per ChangeSecurityPermissionsEx.** In genere, il *parametro StartFileName* è il parametro *StartFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente. Se questo parametro è **Null,** l'operazione viene eseguita sul file o sulla directory specificata nella [**chiamata a ExecMethod.**](/windows/desktop/WmiSdk/swbemservices-execmethod)

</dd> <dt>

*Ricorsivo* \[ in, facoltativo\]
</dt> <dd>

Se **true,** la modifica della proprietà viene applicata in modo ricorsivo ai file e alle directory nella directory specificata [**dall'istanza di \_ CiM LogicalFile.**](cim-logicalfile.md)

> [!Note]  
> Per le istanze di file, *il parametro Recursive* viene ignorato.

 

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

La piattaforma non è Windows.

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

Il file di avvio specificato non è valido.

</dd> <dt>

**Privilegio non mantenuto**
</dt> <dd>

17

Privilegio necessario per l'operazione mancante.

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

[**Win32 \_ PageFile**](win32-pagefile.md)
</dt> </dl>

 

