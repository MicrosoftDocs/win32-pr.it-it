---
description: Consente di modificare il nome del gruppo.
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Rinominare il metodo della classe Win32_Group
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c111a0c12d0fdc1ce3f6d6bcaa0e7b0f57831054
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304436"
---
# <a name="rename-method-of-the-win32_group-class"></a>Rinominare il metodo della \_ classe del gruppo Win32

Il metodo **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) consente di modificare il nome del gruppo.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ in\]
</dt> <dd>

Nome dell'account utente di Windows nel dominio specificato dalla proprietà del **dominio** di questa classe.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo **Rename** può restituire i codici di errore elencati nell'elenco seguente. Per i valori integer diversi da quelli elencati, fare riferimento ai [ \_ codici restituiti di WMI](/windows/desktop/WmiSdk/wmi-return-codes).

<dl> <dt>

**Success**
</dt> <dd>

0

Esito positivo.

</dd> <dt>

**Istanza non trovata**
</dt> <dd>

1

</dd> <dt>

**Istanza obbligatoria**
</dt> <dd>

2

</dd> <dt>

**Parametro non valido**
</dt> <dd>

3

</dd> <dt>

**Il gruppo non è stato trovato**
</dt> <dd>

4

</dd> <dt>

**Dominio non trovato**
</dt> <dd>

5

</dd> <dt>

**L'operazione è consentita solo sul controller di dominio primario del dominio**
</dt> <dd>

6

</dd> <dt>

**Operazione non consentita per gruppi speciali specificati. utente, amministratore, locale o Guest.**
</dt> <dd>

7

</dd> <dt>

**Altro errore API**
</dt> <dd>

8

</dd> <dt>

**Errore interno**
</dt> <dd>

9

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

[**\_Gruppo Win32**](win32-group.md)
</dt> <dt>

[**\_LogicalFileSecuritySetting Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

