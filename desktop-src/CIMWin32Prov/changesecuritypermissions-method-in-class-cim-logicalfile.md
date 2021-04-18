---
description: Modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto.
ms.assetid: a3caa717-ad37-4e4f-9f4e-f37aed382fa4
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissions della classe CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.ChangeSecurityPermissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 929e05047af203d8e2344afa8175228e3bd969fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305046"
---
# <a name="changesecuritypermissions-method-of-the-cim_logicalfile-class"></a>Metodo ChangeSecurityPermissions della classe CIM \_ LogicalFile

Il metodo **ChangeSecurityPermissions** modifica le autorizzazioni di sicurezza per il file logico specificato nel percorso dell'oggetto. Se il file logico è una directory, **ChangeSecurityPermissions** agirà in modo ricorsivo, modificando le autorizzazioni di sicurezza per tutti i file e le sottodirectory contenute nella directory.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

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

Specifica le informazioni di sicurezza.

> [!Note]  
> Un  elenco di controllo di accesso (ACL) null [**nel \_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede un accesso illimitato.

 

</dd> <dt>

*Opzione* \[ in\]
</dt> <dd>

Privilegi di sicurezza da modificare. Per modificare, ad esempio, la sicurezza del proprietario e del DACL, usare:

`Option = 1 + 4`

oppure

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>

<span id="Change_Owner_Security_Information"></span><span id="change_owner_security_information"></span><span id="CHANGE_OWNER_SECURITY_INFORMATION"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza del proprietario** (1)


</dt> <dd>

Modificare il proprietario del file logico.

</dd> <dt>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>

<span id="Change_Group_Security_Information"></span><span id="change_group_security_information"></span><span id="CHANGE_GROUP_SECURITY_INFORMATION"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2)


</dt> <dd>

Modificare il gruppo del file logico.

</dd> <dt>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>

<span id="Change_Dacl_Security_Information"></span><span id="change_dacl_security_information"></span><span id="CHANGE_DACL_SECURITY_INFORMATION"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4)


</dt> <dd>

Modificare l'ACL del file logico.

</dd> <dt>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>

<span id="Change_Sacl_Security_Information"></span><span id="change_sacl_security_information"></span><span id="CHANGE_SACL_SECURITY_INFORMATION"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8)


</dt> <dd>

Modificare l'ACL di sistema del file logico.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 in caso di esito positivo e qualsiasi altro numero per indicare un errore.

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

[**\_LOGICALFILE CIM**](changesecuritypermissions-method-in-class-cim-logicalfile.md)
</dt> <dt>

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> </dl>

 

