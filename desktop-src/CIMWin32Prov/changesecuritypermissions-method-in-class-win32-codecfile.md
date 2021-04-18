---
description: Modifica le autorizzazioni di sicurezza per il file di codec logico specificato nel percorso dell'oggetto.
ms.assetid: d7945666-e514-4bfc-81bc-8e98aa90bcf0
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissions della classe Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b0789164b2bb28b5c3c84e907cf7ae2acb96e01
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304445"
---
# <a name="changesecuritypermissions-method-of-the-win32_codecfile-class"></a>Metodo ChangeSecurityPermissions della \_ classe Sqlcfile Win32

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** modifica le autorizzazioni di sicurezza per il file di codec logico specificato nel percorso dell'oggetto. Se il file logico è una directory, **ChangeSecurityPermissions** è ricorsivo e modifica le autorizzazioni di sicurezza di tutti i file e le sottodirectory in essa contenuti. **ChangeSecurityPermissions** restituisce un valore intero pari a 0 (zero) se le autorizzazioni vengono modificate e un numero diverso per indicare un errore.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SecurityDescriptor* \[ in\]
</dt> <dd>

Espressione che viene risolta in un'istanza di [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Questo descrittore contiene nuove autorizzazioni di sicurezza per l'istanza di [**Win32 \_ codecfile**](win32-codecfile.md).

</dd> <dt>

*Opzione* \[ in\]
</dt> <dd>

Privilegio di sicurezza da modificare. Ad esempio, per modificare la sicurezza del proprietario e dell'elenco di controllo di accesso discrezionale (DACL), usare:

`Option = 1 + 4`

-oppure-

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del proprietario** (1 (0x1))


</dt> <dd>

Modificare il proprietario del file logico.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2 (0x2))


</dt> <dd>

Modificare il gruppo del file logico.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4 (0x4))


</dt> <dd>

Modificare l'elenco di controllo di accesso discrezionale (DACL) del file logico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8 (0x8))


</dt> <dd>

Modificare l'elenco di controllo di accesso di sistema (SACL) del file logico.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) se le autorizzazioni vengono modificate e un numero diverso per indicare un errore.

<dl> <dt>

**Success**
</dt> <dd>

0

La richiesta ha avuto esito positivo.

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

**Oggetto già esistente**
</dt> <dd>

10

L'oggetto specificato esiste già.

</dd> <dt>

**File System non NTFS**
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

Un privilegio necessario per l'operazione non viene mantenuto.

</dd> <dt>

**Parametro non valido**
</dt> <dd>

21

Parametro specificato non valido.

</dd> </dl>

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

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Codecfile Win32 \_**](win32-codecfile.md)
</dt> </dl>

 

