---
description: Modifica le autorizzazioni di sicurezza per il file di collegamento logico specificato nel percorso dell'oggetto.
ms.assetid: abd5aec8-4684-4b8d-8fdf-d3a7a5eec103
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissions della classe Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 43d69f8a04fd937591675fe13fefd9499fe4c0dd59f70da02077cb97f7b06fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010103"
---
# <a name="changesecuritypermissions-method-of-the-win32_shortcutfile-class"></a>Metodo ChangeSecurityPermissions della classe ShortcutFile Win32 \_

Il metodo della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **ChangeSecurityPermissions** modifica le autorizzazioni di sicurezza per il file di collegamento logico specificato nel percorso dell'oggetto. Se il file logico è una directory, **ChangeSecurityPermissions** è ricorsivo e modifica le autorizzazioni di sicurezza di tutti i file e le sottodirectory contenuti nella directory. **ChangeSecurityPermissions restituisce** un valore intero pari a 0 (zero) se le autorizzazioni vengono modificate e un numero diverso per indicare un errore.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 ChangeSecurityPermissions(
  [in] Win32_SecurityDescriptor SecurityDescriptor,
  [in] uint32                   Option
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Descrittore di sicurezza* \[ Pollici\]
</dt> <dd>

Espressione che si risolve in un'istanza di [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Questo descrittore contiene nuove autorizzazioni di sicurezza per l'istanza di [**Win32 \_ PageFile**](win32-pagefile.md).

</dd> <dt>

*Opzione* \[ Pollici\]
</dt> <dd>

Privilegio di sicurezza effettivo da modificare. Ad esempio, per modificare il proprietario e la sicurezza DACL, usare:

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

Modificare l'elenco di controllo di accesso discrezionale (DACL) del file logico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**MODIFICA \_ INFORMAZIONI DI \_ SICUREZZA \_ SACL** (8)


</dt> <dd>

Modificare l'elenco di controllo di accesso di sistema (SACL) del file logico.

</dd> </dl> </dd> </dl>

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

Si verifica una violazione di condivisione.

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

[**File di collegamento Win32 \_**](win32-shortcutfile.md)
</dt> </dl>

 

