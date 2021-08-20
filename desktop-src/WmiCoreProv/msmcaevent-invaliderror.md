---
description: Indica un errore di machine check architecture (MCA) non valido. Un errore MCA non valido identifica un formato di errore non conforme Windows specifiche. Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: 476ea558-2e0e-480f-b4ba-8d73fdef3308
title: MSMCAEvent_InvalidError classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_InvalidError
- MSMCAEvent_InvalidError.Active
- MSMCAEvent_InvalidError.AdditionalErrors
- MSMCAEvent_InvalidError.Cpu
- MSMCAEvent_InvalidError.ErrorSeverity
- MSMCAEvent_InvalidError.InstanceName
- MSMCAEvent_InvalidError.RawRecord
- MSMCAEvent_InvalidError.RecordId
- MSMCAEvent_InvalidError.Size
- MSMCAEvent_InvalidError.Type
- MSMCAEvent_InvalidError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 5a42ee7dfcc9864cdd4ca90ba7d66903407352e92224e5ded7a16ace4e053d37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821975"
---
# <a name="msmcaevent_invaliderror-class"></a>Classe \_ InvalidError MSMCAEvent

La **classe MSMCAEvent \_ InvalidError** indica un errore di machine check architecture (MCA) non valido. Un errore MCA non valido identifica un formato di errore non conforme Windows specifiche. Questa classe è disponibile solo nei sistemi Windows a 64 bit.

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MSMCAEvent_InvalidError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Members

La **classe MSMCAEvent \_ InvalidError** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MSMCAEvent \_ InvalidError** ha queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**TRUE** se questa istanza della classe è attiva; in caso contrario, **FALSE.**

</dd> <dt>

**AdditionalErrors**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di errori aggiuntivi nel record MCA.

</dd> <dt>

**Cpu**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

CPU che ha segnalato l'errore. Questa proprietà si applica solo a un sistema multiprocessore in cui al primo processore viene assegnato il numero 0, al secondo processore viene assegnato il numero 1 e così via.

</dd> <dt>

**ErrorSeverity**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
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

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificatore univoco di questa istanza della classe .

</dd> <dt>

**LogToEventlog**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se 0 (zero), questo evento non viene registrato nel registro eventi di sistema.

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di byte che contiene il record di errore non elaborato presentato Windows dal livello di astrazione di sistema (SAL). Il numero di elementi nella matrice viene specificato dalla **proprietà Size.**

</dd> <dt>

**Recordid**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del record di errore per questo errore.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Dimensioni**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni del record di errore non elaborato.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di messaggio del registro eventi. Questi messaggi corrispondono ai codici dei messaggi del registro eventi usati per inserire i messaggi del registro eventi dal provider consumer del registro eventi Windows quando riceve uno degli eventi.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe MSMCAEvent \_ InvalidError** deriva da [**WMIEvent**](wmievent.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2003<br/>                                                         |
| Spazio dei nomi<br/>                | Wmi \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi MSMCA](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

