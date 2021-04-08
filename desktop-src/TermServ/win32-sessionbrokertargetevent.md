---
title: Classe Win32_SessionBrokerTargetEvent
description: Rappresenta una modifica a una destinazione di Service Broker di sessione.
ms.assetid: ee3ae0ed-eb8b-4777-9b9e-0e50722cf52a
ms.tgt_platform: multiple
keywords:
- Classe Win32_SessionBrokerTargetEvent Servizi Desktop remoto
- Classe Win32_SessionBrokerTargetEvent Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTargetEvent
- Win32_SessionBrokerTargetEvent.SECURITY_DESCRIPTOR
- Win32_SessionBrokerTargetEvent.TIME_CREATED
- Win32_SessionBrokerTargetEvent.ChangeType
- Win32_SessionBrokerTargetEvent.PluginName
- Win32_SessionBrokerTargetEvent.TargetName
- Win32_SessionBrokerTargetEvent.FarmName
- Win32_SessionBrokerTargetEvent.Guid
- Win32_SessionBrokerTargetEvent.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d7f1cf6aab1c4497ce85cb93318c9ca79368853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740703"
---
# <a name="win32_sessionbrokertargetevent-class"></a>Win32 \_ SessionBrokerTargetEvent (classe)

Rappresenta una modifica a una destinazione di Service Broker di sessione.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Win32_SessionBrokerTargetEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint32 ChangeType;
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ SessionBrokerTargetEvent** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SessionBrokerTargetEvent** dispone di queste proprietà.

<dl> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica la modifica che si è verificata. Può corrispondere a uno dei valori seguenti.

<dt>

1 (0x1)
</dt> <dd>

Il tipo di modifica non è specificato.

</dd> <dt>

2 (0x2)
</dt> <dd>

L'indirizzo IP esterno è stato modificato.

</dd> <dt>

4 (0x4)
</dt> <dd>

L'indirizzo IP interno è stato modificato.

</dd> <dt>

8 (0x8)
</dt> <dd>

La destinazione è stata unita in join.

</dd> <dt>

16 (0x10)
</dt> <dd>

La destinazione è stata rimossa.

</dd> <dt>

32 (0x20)
</dt> <dd>

Lo stato della destinazione è stato modificato.

</dd> <dt>

64 (0x40)
</dt> <dd>

La destinazione è inattiva.

</dd> </dl>

</dd> <dt>

**Environment**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'ambiente. Nel caso di una macchina virtuale (VM) destinazione, potrebbe essere il nome host della VM.

**Windows Server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2012

</dd> <dt>

**Farmname**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della farm a cui appartiene la destinazione.

**Windows Server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2012

</dd> <dt>

**GUID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

GUID della destinazione.

**Windows Server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2012

</dd> <dt>

**PluginName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del plug-in.

**Windows Server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2012

</dd> <dt>

**descrittore di sicurezza \_**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento. Questa proprietà viene ereditata dall' [**\_ \_ evento**](/windows/desktop/WmiSdk/--event). Per ulteriori informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere la pagina relativa alle [costanti di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-constants).

</dd> <dt>

**TargetName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome della destinazione.

**Windows Server 2008 R2:** Questa proprietà non è disponibile prima di Windows Server 2012

</dd> <dt>

**ORA di \_ creazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui è stato generato l'evento. Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601. Le informazioni sono nel formato UTC (Coordinated Universal Time). Questa proprietà viene ereditata dall' [**\_ \_ evento**](/windows/desktop/WmiSdk/--event).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

