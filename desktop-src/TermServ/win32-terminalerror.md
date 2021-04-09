---
title: Classe Win32_TerminalError
description: Rappresenta un errore del terminale.
ms.assetid: d3f622cd-e4ce-4c7e-999e-940b67fd116c
ms.tgt_platform: multiple
keywords:
- Classe Win32_TerminalError Servizi Desktop remoto
- Classe Win32_TerminalError Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TerminalError
- Win32_TerminalError.Description
- Win32_TerminalError.Operation
- Win32_TerminalError.ParameterInfo
- Win32_TerminalError.ProviderName
- Win32_TerminalError.StatusCode
- Win32_TerminalError.TerminalName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99724badc6c1ca7a2e4168e5c062b4dd1495ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119251"
---
# <a name="win32_terminalerror-class"></a>Win32 \_ TerminalError (classe)

Rappresenta un errore del terminale.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_TerminalError : __ExtendedStatus
{
  string Description;
  string Operation;
  string ParameterInfo;
  string ProviderName;
  uint32 StatusCode;
  string TerminalName;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TerminalError** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TerminalError** dispone di queste proprietà.

<dl> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualsiasi stringa definita dall'utente che descrive un errore o uno stato operativo.

Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).

</dd> <dt>

**Operazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Operazione che viene eseguita al momento di un errore o di un'anomalia. In genere, WMI imposta questa proprietà sul nome di un'API COM per un metodo WMI come il seguente: [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenum).

Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).

</dd> <dt>

**ParameterInfo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Parametri che coinvolgono un errore o una modifica dello stato. Se, ad esempio, un'applicazione tenta di recuperare una classe che non esiste, questa proprietà viene impostata sul nome della classe che ha causato l'errore.

Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).

</dd> <dt>

**ProviderName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica il provider che causa o segnala un errore o una modifica dello stato. Se un provider non è necessario, questa stringa è impostata su "Windows Management".

Questa proprietà viene ereditata da [**\_ \_ ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus).

</dd> <dt>

**StatusCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Contiene un codice di errore o informazioni per un'operazione. Può trattarsi di qualsiasi valore definito dal provider, ma il valore 0 (zero) è in genere riservato per indicare l'esito positivo. Questa proprietà viene ereditata da [**\_ \_ NotifyStatus**](/windows/desktop/WmiSdk/--notifystatus).

</dd> <dt>

**Terminale**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del vizio del terminale in cui si è verificato l'errore.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_ExtendedStatus**](/windows/desktop/WmiSdk/--extendedstatus)
</dt> </dl>

 

