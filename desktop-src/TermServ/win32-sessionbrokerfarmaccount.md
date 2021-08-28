---
title: Win32_SessionBrokerFarmAccount classe
description: La classe \_ Win32 SessionBrokerFarmAccount non è più disponibile per l'uso a Windows Server 2012. | Win32_SessionBrokerFarmAccount classe
ms.assetid: a76ade0f-cd94-438c-bc07-30dc4b4ee6c8
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerFarmAccount classe Servizi Desktop remoto
- Win32_SessionBrokerFarmAccount classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount
- Win32_SessionBrokerFarmAccount.FarmName
- Win32_SessionBrokerFarmAccount.Manual
- Win32_SessionBrokerFarmAccount.AccountName
- Win32_SessionBrokerFarmAccount.AccountDomain
- Win32_SessionBrokerFarmAccount.AccountPassword
- Win32_SessionBrokerFarmAccount.AccountSPN1
- Win32_SessionBrokerFarmAccount.AccountSPN2
- Win32_SessionBrokerFarmAccount.ComputerDNSName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8b7d55f973dc19c03182a4199b64f91f9de5a0774cc8c8f9d77d67eeb715c24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422491"
---
# <a name="win32_sessionbrokerfarmaccount-class"></a>Classe \_ SessionBrokerFarmAccount Win32

\[La **classe \_ Win32 SessionBrokerFarmAccount** non è più disponibile per l'uso a Windows Server 2012.\]

Definisce un account della farm del broker di sessione.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARMACCOUNT_Prov"), AMENDMENT]
class Win32_SessionBrokerFarmAccount
{
  string  FarmName;
  boolean Manual;
  string  AccountName;
  string  AccountDomain;
  string  AccountPassword;
  string  AccountSPN1;
  string  AccountSPN2;
  string  ComputerDNSName;
};
```

## <a name="members"></a>Members

La **classe \_ Win32 SessionBrokerFarmAccount** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ Win32 SessionBrokerFarmAccount** dispone di questi metodi.



| Metodo                                                      | Descrizione                          |
|:------------------------------------------------------------|:-------------------------------------|
| [**DeleteEx**](deleteex-win32-sessionbrokerfarmaccount.md) | Elimina l'account della farm.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ Win32 SessionBrokerFarmAccount** ha queste proprietà.

<dl> <dt>

**AccountDomain**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Nome del dominio a cui appartiene l'account della farm.

</dd> <dt>

**AccountName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Nome dell'account della farm.

</dd> <dt>

**AccountPassword**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Password dell'account della farm.

</dd> <dt>

**AccountSPN1**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Primo nome dell'entità servizio (SPN) associato all'account della farm.

</dd> <dt>

**AccountSPN2**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Secondo nome SPN associato all'account della farm.

</dd> <dt>

**ComputerDNSName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Nome DNS del computer associato all'account della farm.

</dd> <dt>

**FarmName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome della farm del broker di sessione.

</dd> <dt>

**Manuale**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Indica se la password per l'account viene aggiornata manualmente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                              |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

