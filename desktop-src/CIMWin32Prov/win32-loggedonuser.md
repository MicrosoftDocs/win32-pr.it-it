---
description: La classe WMI di associazione Win32 \_ LoggedOnUser mette in relazione una sessione e un account utente.
ms.assetid: b1233f90-4898-4ced-84d2-0858027e935a
ms.tgt_platform: multiple
title: Win32_LoggedOnUser classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoggedOnUser
- Win32_LoggedOnUser.Dependent
- Win32_LoggedOnUser.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73cb34246f7b31393527aef053c0cb8cbd12702217dd7113d5714ac022bc3716
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973446"
---
# <a name="win32_loggedonuser-class"></a>Classe Win32 \_ LoggedOnUser

La classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) di **associazione Win32 \_ LoggedOnUser** mette in relazione una sessione e un account utente.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8BB5B3EC-E1F7-4b39-942A-605D5F55789A}"), AMENDMENT]
class Win32_LoggedOnUser : CIM_Dependency
{
  Win32_LogonSession REF Dependent;
  Win32_Account      REF Antecedent;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ LoggedOnUser** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ LoggedOnUser** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ Account Win32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Account [**Win32 \_ che**](win32-account.md) descrive l'account usato nell'avvio della sessione. L'account può essere un account utente o un account di sistema.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **Win32 \_ LogonSession**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (dipendente), [**chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Oggetto [**\_ LogonSession Win32**](win32-logonsessionmappeddisk.md) che descrive la sessione attualmente in uso dall'account.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe Win32 \_ LoggedOnUser** è derivata da [**CIM \_ Dependency**](cim-dependency.md).

## <a name="examples"></a>Esempio

L'esempio di funzione [get-loggedonuser](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) di PowerShell ottiene gli utenti connessi in un computer locale o remoto, con le informazioni di sessione.

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

[**Dipendenza \_ CIM**](cim-dependency.md)
</dt> <dt>

[Classi del sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

