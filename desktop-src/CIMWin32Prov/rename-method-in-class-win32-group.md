---
description: Consente di modificare il nome del gruppo.
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Metodo Rename della classe Win32_Group
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
ms.openlocfilehash: cff8f587426b45133716e308ea40785602fea2d5b5d30a99645bfd0c6cc5c4e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003021"
---
# <a name="rename-method-of-the-win32_group-class"></a>Metodo Rename della classe Win32 \_ Group

Il **metodo Rinomina** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) consente di modificare il nome del gruppo.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome* \[ Pollici\]
</dt> <dd>

Nome dell'Windows account utente nel dominio specificato dalla **proprietà Domain** di questa classe.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il **metodo Rename** può restituire i codici di errore elencati nell'elenco seguente. Per valori interi diversi da quelli elencati, vedere [Codici restituiti WMI \_ ](/windows/desktop/WmiSdk/wmi-return-codes).

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

**Gruppo non trovato**
</dt> <dd>

4

</dd> <dt>

**Dominio non trovato**
</dt> <dd>

5

</dd> <dt>

**L'operazione è consentita solo nel controller di dominio primario del dominio**
</dt> <dd>

6

</dd> <dt>

**L'operazione non è consentita nei gruppi speciali specificati. utente, amministratore, locale o guest.**
</dt> <dd>

7

</dd> <dt>

**Altro errore dell'API**
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
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Gruppo \_ Win32**](win32-group.md)
</dt> <dt>

[**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

