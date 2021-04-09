---
description: Win32 \_ PrivilegesStatus&\# 8194; La classe WMI fornisce informazioni sui privilegi necessari per completare un'operazione. Può essere restituito quando un'operazione ha esito negativo o quando è stata restituita un'istanza parzialmente compilata.
ms.assetid: 295ec2bd-7996-4031-8503-d4e869d8368d
ms.tgt_platform: multiple
title: Classe Win32_PrivilegesStatus (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrivilegesStatus
- Win32_PrivilegesStatus.Description
- Win32_PrivilegesStatus.Operation
- Win32_PrivilegesStatus.ParameterInfo
- Win32_PrivilegesStatus.ProviderName
- Win32_PrivilegesStatus.StatusCode
- Win32_PrivilegesStatus.PrivilegesNotHeld
- Win32_PrivilegesStatus.PrivilegesRequired
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ab399ce08374a954b3bbc015cfee7b4d20167b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877813"
---
# <a name="win32_privilegesstatus-class-cimwin32-wmi-providers"></a>Classe Win32_PrivilegesStatus (provider WMI CIMWin32)

La  [classe WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ PrivilegesStatus** fornisce informazioni sui privilegi necessari per completare un'operazione. Può essere restituito quando un'operazione ha esito negativo o quando è stata restituita un'istanza parzialmente compilata.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[UUID("{BE46D060-7A7C-11d2-BC85-00104B2CF71C}"), AMENDMENT]
class Win32_PrivilegesStatus : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string PrivilegesNotHeld[];
  string PrivilegesRequired[];
};
```

## <a name="members"></a>Members

La classe **Win32 \_ PrivilegesStatus** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ PrivilegesStatus** dispone di queste proprietà.

<dl> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualsiasi stringa definita dall'utente che descrive un errore o uno stato operativo.

Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).

</dd> <dt>

**Operazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Operazione che viene eseguita al momento di un errore o di un'anomalia. In genere, Strumentazione gestione Windows (WMI) imposta questa proprietà sul nome di un'API COM per un metodo WMI come il seguente: [**IWbemServices:: CreateInstanceEnum**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).

Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Parametri che coinvolgono un errore o una modifica dello stato. Se, ad esempio, un'applicazione tenta di recuperare una classe che non esiste, questa proprietà viene impostata sul nome della classe che ha causato l'errore.

Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).

</dd> <dt>

**PrivilegesNotHeld**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| AccessControl \| Windows NT Privileges")
</dt> </dl>

Elenco dei privilegi di accesso necessari mancanti per completare un'operazione. I tipi di privilegi di accesso sono disponibili con i privilegi di Windows.

Esempio: "SE \_ Shutdown \_ Name"

</dd> <dt>

**PrivilegesRequired**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| AccessControl \| Windows NT Privileges")
</dt> </dl>

Elenco di tutti i privilegi necessari per eseguire un'operazione. Sono inclusi i valori della proprietà **PrivilegesNotHeld** .

Esempio: "SE \_ Shutdown \_ Name"

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica il provider che causa o segnala un errore o una modifica dello stato. Se un provider non è necessario, questa stringa è impostata su "Windows Management".

Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Contiene un codice di errore o informazioni per un'operazione. Può trattarsi di qualsiasi valore definito dal provider, ma il valore 0 (zero) è in genere riservato per indicare l'esito positivo.

Questa proprietà viene ereditata da [**\_ \_ NotifyStatus**](../wmisdk/--notifystatus.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ PrivilegesStatus** deriva da [**\_ \_ ExtendedStatus**](../wmisdk/--extendedstatus.md).

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

[**\_\_ExtendedStatus**](../wmisdk/--extendedstatus.md)
</dt> </dl>

 

 
