---
description: Indica un errore specifico della piattaforma Machine Check Architecture (MCA). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: 409641d5-3451-4d26-88d1-bfd0e55db257
title: MSMCAEvent_PlatformSpecificError classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PlatformSpecificError
- MSMCAEvent_PlatformSpecificError.Active
- MSMCAEvent_PlatformSpecificError.AdditionalErrors
- MSMCAEvent_PlatformSpecificError.Cpu
- MSMCAEvent_PlatformSpecificError.ErrorSeverity
- MSMCAEvent_PlatformSpecificError.InstanceName
- MSMCAEvent_PlatformSpecificError.OEM_COMPONENT_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_BUS_SPECIFIC_DATA
- MSMCAEvent_PlatformSpecificError.PLATFORM_ERROR_STATUS
- MSMCAEvent_PlatformSpecificError.PLATFORM_REQUESTOR_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_RESPONDER_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_TARGET_ID
- MSMCAEvent_PlatformSpecificError.RawRecord
- MSMCAEvent_PlatformSpecificError.RecordId
- MSMCAEvent_PlatformSpecificError.Size
- MSMCAEvent_PlatformSpecificError.Type
- MSMCAEvent_PlatformSpecificError.VALIDATION_BITS
- MSMCAEvent_PlatformSpecificError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 0f85a0828b46826566c406d90b851cec3bbe39ee07a1456065e93542edcda35c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120971"
---
# <a name="msmcaevent_platformspecificerror-class"></a>Classe MSMCAEvent \_ PlatformSpecificError

La **classe MSMCAEvent \_ PlatformSpecificError** indica un errore specifico della piattaforma Machine Check Architecture (MCA). Questa classe è disponibile solo nei sistemi Windows a 64 bit.

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MSMCAEvent_PlatformSpecificError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   OEM_COMPONENT_ID;
  uint64  PLATFORM_BUS_SPECIFIC_DATA;
  uint64  PLATFORM_ERROR_STATUS;
  uint64  PLATFORM_REQUESTOR_ID;
  uint64  PLATFORM_RESPONDER_ID;
  uint64  PLATFORM_TARGET_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Members

La **classe MSMCAEvent \_ PlatformSpecificError** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MSMCAEvent \_ PlatformSpecificError** ha queste proprietà.

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

Numero di errori aggiuntivi nel record.

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

**ID COMPONENTE OEM \_ \_**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore univoco del componente che segnala l'errore.

</dd> <dt>

**DATI \_ SPECIFICI DEL BUS DI \_ \_ PIATTAFORMA**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dati dipendenti dal bus specifici dell'OEM.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**STATO \_ DEGLI ERRORI DELLA \_ PIATTAFORMA**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato di errore generico della piattaforma.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**ID \_ RICHIEDENTE \_ PIATTAFORMA**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del richiedente al momento dell'evento.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_ID RISPONDITORE \_ PIATTAFORMA**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del risponditore al momento dell'evento.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_ID DESTINAZIONE \_ PIATTAFORMA**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore di destinazione al momento dell'evento.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

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

Tipo di messaggio del registro eventi. Questi messaggi corrispondono ai codici dei messaggi del registro eventi usati per inserire i messaggi del log eventi dal provider consumer del registro eventi Windows quando riceve uno degli eventi.

</dd> <dt>

**BIT \_ DI CONVALIDA**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Bit di convalida usati per indicare la validità dei campi successivi.



| Valore                                                                                                                                         | Significato                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <dt>**1 0x1**</dt> </dl>          | **PIATTAFORMA \_ ERROR \_ STATUS** è valido.<br/>            |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <dt>**2 0x2**</dt> </dl>          | **PIATTAFORMA \_ \_ \_ L'ID RICHIEDENTE ERRORE** è valido.<br/>     |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <dt>**4 0x4**</dt> </dl>          | **PIATTAFORMA \_ \_ \_ L'ID RISPONDITORE ERRORI** è valido.<br/>     |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <dt>**8 0x8**</dt> </dl>          | **PIATTAFORMA \_ \_ \_ L'ID DESTINAZIONE ERRORE** è valido.<br/>        |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <dt>**16 0x10**</dt> </dl>    | **PIATTAFORMA \_ I \_ DATI SPECIFICI \_ DELL'ERRORE** sono validi.<br/>    |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <dt>**32 0x20**</dt> </dl>    | **PIATTAFORMA \_ ERRORE \_ \_ L'ID OEM** è valido.<br/>           |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <dt>**64 0x40**</dt> </dl>    | **PIATTAFORMA \_ ERRORE \_ OEM \_ DATA \_ STRUCT** valido.<br/> |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <dt>**128 0x80**</dt> </dl> | **PIATTAFORMA \_ ERRORE \_ OEM \_ DEVICE \_ PATH** valido.<br/> |



 

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe MSMCAEvent \_ PlatformSpecificError** è derivata da [**WMIEvent**](wmievent.md).

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

 

