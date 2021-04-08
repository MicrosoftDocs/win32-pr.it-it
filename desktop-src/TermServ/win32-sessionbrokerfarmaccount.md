---
title: Classe Win32_SessionBrokerFarmAccount
description: La \_ classe Win32 SessionBrokerFarmAccount non è più disponibile per l'uso in Windows Server 2012. | Classe Win32_SessionBrokerFarmAccount
ms.assetid: a76ade0f-cd94-438c-bc07-30dc4b4ee6c8
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionBrokerFarmAccount Servizi Desktop remoto
- Classe Win32_SessionBrokerFarmAccount Servizi Desktop remoto, descritta
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
ms.openlocfilehash: a31f076ddc6f9361be12a57dc60ada24ed75e4bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103761849"
---
# <a name="win32_sessionbrokerfarmaccount-class"></a>Win32 \_ SessionBrokerFarmAccount (classe)

\[La classe **Win32 \_ SessionBrokerFarmAccount** non è più disponibile per l'uso in Windows Server 2012.\]

Definisce un account farm Broker di sessione.

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

La classe **Win32 \_ SessionBrokerFarmAccount** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ SessionBrokerFarmAccount** presenta questi metodi.



| Metodo                                                      | Descrizione                          |
|:------------------------------------------------------------|:-------------------------------------|
| [**DeleteEx**](deleteex-win32-sessionbrokerfarmaccount.md) | Elimina l'account farm.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SessionBrokerFarmAccount** dispone di queste proprietà.

<dl> <dt>

**AccountDomain**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Nome del dominio a cui appartiene l'account farm.

</dd> <dt>

**AccountName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Nome dell'account farm.

</dd> <dt>

**AccountPassword**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Password dell'account farm.

</dd> <dt>

**AccountSPN1**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Primo nome dell'entità servizio (SPN) associato all'account farm.

</dd> <dt>

**AccountSPN2**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Secondo SPN associato all'account della farm.

</dd> <dt>

**ComputerDNSName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Nome DNS del computer associato all'account della farm.

</dd> <dt>

**Farmname**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome della farm di broker di sessione.

</dd> <dt>

**Manuale**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
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
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

