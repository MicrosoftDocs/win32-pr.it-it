---
description: Indica un errore del BIOS di sistema di Machine Check Architecture (MCA). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: b451ca45-6208-4445-b9f1-b4e3174837a4
title: MSMCAEvent_SMBIOSError classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SMBIOSError
- MSMCAEvent_SMBIOSError.Active
- MSMCAEvent_SMBIOSError.AdditionalErrors
- MSMCAEvent_SMBIOSError.Cpu
- MSMCAEvent_SMBIOSError.ErrorSeverity
- MSMCAEvent_SMBIOSError.InstanceName
- MSMCAEvent_SMBIOSError.RawRecord
- MSMCAEvent_SMBIOSError.RecordId
- MSMCAEvent_SMBIOSError.Size
- MSMCAEvent_SMBIOSError.SMBIOS_EVENT_TYPE
- MSMCAEvent_SMBIOSError.Type
- MSMCAEvent_SMBIOSError.VALIDATION_BITS
- MSMCAEvent_SMBIOSError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: fccb38a73585db71c6418929a35458f26b9749159e537de47a298d920b318e08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558396"
---
# <a name="msmcaevent_smbioserror-class"></a>Classe MSMCAEvent \_ SMBIOSError

La **classe MSMCAEvent \_ SMBIOSError** indica un errore del BIOS di sistema dell'architettura di controllo del computer. Questa classe è disponibile solo nei sistemi Windows a 64 bit.

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MSMCAEvent_SMBIOSError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint8   SMBIOS_EVENT_TYPE;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Members

La **classe MSMCAEvent \_ SMBIOSError** include i tipi di membri seguenti:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MSMCAEvent \_ SMBIOSError** dispone di queste proprietà.

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

CPU che ha segnalato l'errore. Questa proprietà si applica solo a un sistema multiprocessore in cui al primo processore viene assegnato il numero 0, al secondo viene assegnato il numero 1 e così via.

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

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **Chiave**](/windows/desktop/WmiSdk/standard-qualifiers)
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

Matrice di byte contenente il record di errore non elaborato. Numero di elementi nella matrice specificati **dalla proprietà** Size.

</dd> <dt>

**Recordid**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del record di errore per questo errore.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**Dimensioni**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni del record di errore non elaborato.

</dd> <dt>

**TIPO DI \_ EVENTO \_ SMBIOS**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di evento.



| Valore                                                                                                  | Significato                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl>   | Riservato.<br/>                                                                                                        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl>   | Errore di memoria ECC a bit singolo.<br/>                                                                                     |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>   | Errore di memoria ECC a bit multipli.<br/>                                                                                   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>   | Errore di memoria di parità.<br/>                                                                                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>   | Timeout del bus.<br/>                                                                                                    |
| <span id="5"></span><dl> <dt>**5**</dt> </dl>   | Verifica canale di I/O.<br/>                                                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl>   | NMI software.<br/>                                                                                                    |
| <span id="7"></span><dl> <dt>**7**</dt> </dl>   | Ridimensionamento post-memoria.<br/>                                                                                              |
| <span id="8"></span><dl> <dt>**8**</dt> </dl>   | Errore POST.<br/>                                                                                                      |
| <span id="9"></span><dl> <dt>**9**</dt> </dl>   | Errore di parità PCI.<br/>                                                                                                |
| <span id="10"></span><dl> <dt>**10**</dt> </dl> | Errore di sistema PCI.<br/>                                                                                                |
| <span id="11"></span><dl> <dt>**11**</dt> </dl> | Errore della CPU.<br/>                                                                                                     |
| <span id="12"></span><dl> <dt>**12**</dt> </dl> | Timeout del timer di failsafe EISA.<br/>                                                                                    |
| <span id="13"></span><dl> <dt>**13**</dt> </dl> | Log di memoria correggibile disabilitato.<br/>                                                                                 |
| <span id="14"></span><dl> <dt>**14**</dt> </dl> | Registrazione disabilitata per un tipo di evento specifico. Troppi errori dello stesso tipo ricevuti in un breve periodo di tempo.<br/> |
| <span id="15"></span><dl> <dt>**15**</dt> </dl> | Riservato.<br/>                                                                                                        |
| <span id="16"></span><dl> <dt>**16**</dt> </dl> | Limite di sistema superato (ad esempio, è stata superata la soglia di tensione o temperatura).<br/>                                  |
| <span id="17"></span><dl> <dt>**17**</dt> </dl> | Il timer hardware asincrono è scaduto ed è stata emessa una reimpostazione del sistema.<br/>                                                   |
| <span id="18"></span><dl> <dt>**18**</dt> </dl> | Informazioni di configurazione del sistema.<br/>                                                                                |
| <span id="19"></span><dl> <dt>**19**</dt> </dl> | Informazioni sul disco rigido.<br/>                                                                                           |
| <span id="20"></span><dl> <dt>**20**</dt> </dl> | Sistema riconfigurato.<br/>                                                                                             |
| <span id="21"></span><dl> <dt>**21**</dt> </dl> | Errore complesso della CPU noncorrebile.<br/>                                                                                 |
| <span id="22"></span><dl> <dt>**22**</dt> </dl> | Reimpostazione o cancellata dell'area del log.<br/>                                                                                       |
| <span id="23"></span><dl> <dt>**23**</dt> </dl> | Avvio del sistema. Se implementata, questa voce di log è garantita come la prima scritta in qualsiasi avvio del sistema.<br/>        |



 

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di messaggio del registro eventi. Questi messaggi corrispondono ai codici dei messaggi del registro eventi utilizzati per inserire i messaggi del registro eventi dal provider del consumer del registro eventi di Windows quando riceve uno degli eventi.

</dd> <dt>

**BIT \_ DI CONVALIDA**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Bit di convalida utilizzati per indicare la validità dei campi successivi. Il valore 1 (0x1) indica che **l'EVENTO \_ SMBIOS** è valido.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe MSMCAEvent \_ SMBIOSError** è derivata da [**WMIEvent.**](wmievent.md)

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

 

