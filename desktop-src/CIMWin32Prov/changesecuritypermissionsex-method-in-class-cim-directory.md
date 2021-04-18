---
description: Modifica le autorizzazioni di sicurezza per il file di voce della directory logica specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo ChangeSecurityPermissions e viene ereditato da CIM \_ LogicalFile).
ms.assetid: 5c1f66ba-9aa1-47ca-8fcf-7663782544cd
ms.tgt_platform: multiple
title: Metodo ChangeSecurityPermissionsEx della classe CIM_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Directory.ChangeSecurityPermissionsEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2d8ddf4c6ffdbd016db1e8c08d89f2dd6476ccf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304786"
---
# <a name="changesecuritypermissionsex-method-of-the-cim_directory-class"></a>Metodo ChangeSecurityPermissionsEx della classe di \_ directory CIM

Il metodo **ChangeSecurityPermissionsEx** modifica le autorizzazioni di sicurezza per il file di voce della directory logica specificato nel percorso dell'oggetto (questo metodo è una versione estesa del metodo [**ChangeSecurityPermissions**](changesecuritypermissions-method-in-class-cim-directory.md) ed è ereditato da [**CIM \_ LogicalFile**](cim-logicalfile.md)). Se il file logico è una directory, questo metodo agirà in modo ricorsivo, modificando le autorizzazioni di sicurezza per tutti i file e le sottodirectory presenti nella directory.

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
> Un ACL **null** nella struttura [**del \_ descrittore di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) concede un accesso illimitato.

 

</dd> <dt>

*Opzione* \[ in\]
</dt> <dd>

Privilegi di sicurezza da modificare. Per modificare, ad esempio, la sicurezza del proprietario e del DACL, utilizzare

`Option = 1 + 4`

oppure

`Option = CHANGE_OWNER_SECURITY_INFORMATION | CHANGE_DACL_SECURITY_INFORMATION`

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

Stringa che rappresenta il nome del file o della directory in cui il metodo ha avuto esito negativo. Se il metodo ha esito positivo, il valore di questo parametro è **null** .

</dd> <dt>

*StartFileName* \[ in, facoltativo\]
</dt> <dd>

Stringa che rappresenta il file o la directory figlio da utilizzare come punto di partenza per questo metodo. In genere, il parametro *StartFileName* è il parametro *StopFileName* che specifica il file o la directory in cui si è verificato un errore dalla chiamata al metodo precedente. Se il valore del parametro è **null**, l'operazione viene eseguita nel file o nella directory specificata nella chiamata [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .

</dd> <dt>

*Ricorsivo* \[ in, facoltativo\]
</dt> <dd>

Se è **true**, anche il metodo viene applicato in modo ricorsivo a file e directory all'interno della directory specificata dall'istanza di [**\_ directory CIM**](cim-directory.md) . Per le istanze di file, questo parametro viene ignorato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.

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

[\_Directory CIM](changesecuritypermissionsex-method-in-class-cim-directory.md)
</dt> <dt>

[**\_Directory CIM**](cim-directory.md)
</dt> </dl>

 

