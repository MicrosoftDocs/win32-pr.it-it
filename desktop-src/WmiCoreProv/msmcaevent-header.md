---
description: Rappresenta l'intestazione comune utilizzata da tutte le classi MSMCAEvent. Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: ff20522c-f805-47dc-bef2-4176211de698
title: Classe MSMCAEvent_Header
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_Header
- MSMCAEvent_Header.AdditionalErrors
- MSMCAEvent_Header.Cpu
- MSMCAEvent_Header.ErrorSeverity
- MSMCAEvent_Header.RecordId
- MSMCAEvent_Header.Type
- MSMCAEvent_Header.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 426f943014f3b6cfbdba5a25d331c0ea621048cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315745"
---
# <a name="msmcaevent_header-class"></a>\_Classe di intestazione MSMCAEvent

La classe di **\_ intestazione MSMCAEvent** rappresenta l'intestazione comune utilizzata da tutte le [classi MSMCA](msmca-classes.md) . I file di intestazione vengono usati in modo che il codice C e C++ possa avere una struttura di dati che descrive l'intestazione comune per tutti gli eventi. Questa classe è riservata per uso interno. Questa classe è disponibile solo nei sistemi Windows a 64 bit.

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MSMCAEvent_Header
{
  uint32 AdditionalErrors;
  uint32 Cpu;
  uint8  ErrorSeverity;
  uint64 RecordId;
  uint32 Type;
  uint32 LogToEventlog;
};
```

## <a name="members"></a>Members

La classe dell' **\_ intestazione MSMCAEvent** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe dell' **\_ intestazione MSMCAEvent** include queste proprietà.

<dl> <dt>

**AdditionalErrors**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di errori aggiuntivi nel record MCA.

</dd> <dt>

**CPU**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

CPU che segnala l'errore. Questa proprietà si applica solo a un sistema multiprocessore in cui al primo processore viene assegnato il numero 0, al secondo processore viene assegnato il numero 1 e così via.

</dd> <dt>

**ErrorSeverity**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Livello di gravità dell'errore segnalato.



| Valore                                                                                                | Significato                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Recuperabile<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Fatal<br/>       |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Correggibile<br/> |



 

</dd> <dt>

**LogToEventlog**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se è 0 (zero), questo evento non viene registrato nel registro eventi di sistema.

</dd> <dt>

**RecordId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del record di errore per l'errore.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di messaggio del log eventi. Questi messaggi corrispondono ai codici dei messaggi del registro eventi utilizzati per inserire i messaggi del registro eventi dal provider di consumer del registro eventi di Windows quando riceve uno degli eventi.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                         |
| Spazio dei nomi<br/>                | \\WMI radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi MSMCA](msmca-classes.md)
</dt> <dt>

[Classi C++ WMI](/windows/desktop/WmiSdk/wmi-c-classes)
</dt> </dl>

 

