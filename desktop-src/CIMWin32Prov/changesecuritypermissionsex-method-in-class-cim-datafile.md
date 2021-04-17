---
description: Modifica le autorizzazioni di sicurezza per il file di dati logico specificato nel percorso dell'oggetto. questo metodo è una versione estesa del metodo ChangeSecurityPermissions.
ms.assetid: baf50a6e-f624-464e-946d-975aeba88ac2
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissionsEx della classe CIM_DataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DataFile.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3c97f9b17fd148a0686a96fb46f77694a2b78b21
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523794"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_datafile-class"></a>Metodo ChangeSecurityPermissionsEx della classe del file di \_ DataFile CIM

Il metodo **ChangeSecurityPermissionsEx** modifica le autorizzazioni di sicurezza per il file di dati logico specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-datafile.md) ). Se il file logico è effettivamente una directory, questo metodo agirà in modo ricorsivo, modificando le autorizzazioni di sicurezza per tutti i file e le sottodirectory contenute nella directory.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

*SecurityDescriptor* \[ in\]
</dt> <dd>

Specifica le informazioni di sicurezza.

> [!Note]  
> Un ACL **null** nella struttura [**del \_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede un accesso illimitato. Per ulteriori informazioni sulle implicazioni dell'accesso illimitato, vedere [creazione di un descrittore di sicurezza per un nuovo oggetto](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

*Opzione* \[ in\]
</dt> <dd>

Privilegi di sicurezza da modificare. Per modificare, ad esempio, la sicurezza del proprietario e del DACL, usare:

`Option = 1 + 4` o `Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

<dt>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>

<span id="CHANGE_OWNER_SECURITY_INFORMATION"></span><span id="change_owner_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza del proprietario** (1)


</dt> <dd>

Modificare il proprietario del file logico.

</dd> <dt>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>

<span id="CHANGE_GROUP_SECURITY_INFORMATION"></span><span id="change_group_security_information"></span>**Modifica \_ di \_ \_ Informazioni sulla sicurezza del gruppo** (2)


</dt> <dd>

Modificare il gruppo del file logico.

</dd> <dt>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>

<span id="CHANGE_DACL_SECURITY_INFORMATION"></span><span id="change_dacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza DACL** (4)


</dt> <dd>

Modificare l'ACL del file logico.

</dd> <dt>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>

<span id="CHANGE_SACL_SECURITY_INFORMATION"></span><span id="change_sacl_security_information"></span>**Modifica \_ di \_ \_ Informazioni di sicurezza SACL** (8)


</dt> <dd>

Modificare l'ACL di sistema del file logico.

</dd> </dl> </dd> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo. Questo parametro è **null** se il metodo ha esito positivo.

</dd> <dt>

*StartFileName* \[ in, facoltativo\]
</dt> <dd>

Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per questo metodo. In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente. Se questo parametro è **null**, l'operazione viene eseguita sul file o sulla directory specificati nella chiamata **ExecMethod** .

Se si usa *StartFileName* , è necessario impostare *ricorsivo* su true.

</dd> <dt>

*Ricorsivo* \[ in, facoltativo\]
</dt> <dd>

Se **true**, il metodo viene anche applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza di [**\_ DataFile DataFile**](cim-datafile.md) . Per le istanze di file, questo parametro viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore. Per ulteriori codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

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

Il nome di oggetto specificato non è valido.

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

Il file di avvio non è valido.

</dd> <dt>

**Privilegio non mantenuto**
</dt> <dd>

17

Privilegio non mantenuto.

</dd> <dt>

**Parametro non valido**
</dt> <dd>

21

Un parametro non è valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il metodo **ChangeSecurityPermissionsEx** nel file di [**\_ DataFile CIM**](cim-datafile.md) viene implementato da WMI.

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

[**File di \_ DataFile CIM**](changesecuritypermissionsex-method-in-class-cim-datafile.md)
</dt> <dt>

[**File di \_ DataFile CIM**](cim-datafile.md)
</dt> <dt>

[Attività WMI: file e cartelle](/windows/desktop/WmiSdk/wmi-tasks--files-and-folders)
</dt> <dt>

[**Costanti dei diritti di accesso a file e directory**](/windows/desktop/WmiSdk/file-and-directory-access-rights-constants)
</dt> </dl>

 

