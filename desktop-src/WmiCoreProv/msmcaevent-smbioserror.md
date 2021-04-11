---
description: Indica un errore BIOS del sistema MCA (computer Check Architecture). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: b451ca45-6208-4445-b9f1-b4e3174837a4
title: Classe MSMCAEvent_SMBIOSError
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
ms.openlocfilehash: 709d480e8865c5d5bde2a9f5e8de45f138e66548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233115"
---
# <a name="msmcaevent_smbioserror-class"></a>\_Classe MSMCAEvent SMBIOSError

La classe **MSMCAEvent \_ SMBIOSError** indica un errore BIOS del sistema MCA (Machine Check Architecture). Questa classe è disponibile solo nei sistemi Windows a 64 bit.

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

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

La **classe \_ SMBIOSError di MSMCAEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SMBIOSError di MSMCAEvent** dispone di queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se questa istanza della classe è attiva; in caso contrario, **false**.

</dd> <dt>

**AdditionalErrors**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di errori aggiuntivi nel record.

</dd> <dt>

**CPU**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

CPU che ha segnalato l'errore. Questa proprietà si applica solo a un sistema multiprocessore in cui al primo processore viene assegnato il numero 0, al secondo processore viene assegnato il numero 1 e così via.

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

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificatore univoco di questa istanza della classe.

</dd> <dt>

**LogToEventlog**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se è 0 (zero), questo evento non viene registrato nel registro eventi di sistema.

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di byte che contiene il record di errore non elaborato. Numero di elementi nella matrice specificata dalla proprietà **size** .

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

**Dimensioni**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni del record di errore non elaborato.

</dd> <dt>

**\_tipo di evento SMBIOS \_**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di evento.



| Valore                                                                                                  | Significato                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl>   | Riservato.<br/>                                                                                                        |
| <span id="1"></span><dl> <dt>**1**</dt> </dl>   | Errore di memoria ECC a bit singolo.<br/>                                                                                     |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>   | Errore di memoria a più bit ECC.<br/>                                                                                   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>   | Errore di memoria di parità.<br/>                                                                                             |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>   | Timeout del bus.<br/>                                                                                                    |
| <span id="5"></span><dl> <dt>**5**</dt> </dl>   | Controllo del canale di I/O.<br/>                                                                                               |
| <span id="6"></span><dl> <dt>**6**</dt> </dl>   | NMI software.<br/>                                                                                                    |
| <span id="7"></span><dl> <dt>**7**</dt> </dl>   | Ridimensionamento post-memoria.<br/>                                                                                              |
| <span id="8"></span><dl> <dt>**8**</dt> </dl>   | MESSAGGIO di errore.<br/>                                                                                                      |
| <span id="9"></span><dl> <dt>**9**</dt> </dl>   | Errore di parità PCI.<br/>                                                                                                |
| <span id="10"></span><dl> <dt>**10**</dt> </dl> | Errore di sistema PCI.<br/>                                                                                                |
| <span id="11"></span><dl> <dt>**11**</dt> </dl> | Errore CPU.<br/>                                                                                                     |
| <span id="12"></span><dl> <dt>**12**</dt> </dl> | Timeout del timer di failsafe per EISA.<br/>                                                                                    |
| <span id="13"></span><dl> <dt>**13**</dt> </dl> | Registro memoria correggibile disabilitato.<br/>                                                                                 |
| <span id="14"></span><dl> <dt>**14**</dt> </dl> | Registrazione disabilitata per un tipo di evento specifico. Troppi errori dello stesso tipo ricevuti in un breve periodo di tempo.<br/> |
| <span id="15"></span><dl> <dt>**15**</dt> </dl> | Riservato.<br/>                                                                                                        |
| <span id="16"></span><dl> <dt>**16**</dt> </dl> | È stato superato il limite di sistema (ad esempio, soglia di tensione o temperatura superata).<br/>                                  |
| <span id="17"></span><dl> <dt>**17**</dt> </dl> | Timer hardware asincrono scaduto ed è stato emesso un ripristino del sistema.<br/>                                                   |
| <span id="18"></span><dl> <dt>**18**</dt> </dl> | Informazioni sulla configurazione di sistema.<br/>                                                                                |
| <span id="19"></span><dl> <dt>**19**</dt> </dl> | Informazioni sul disco rigido.<br/>                                                                                           |
| <span id="20"></span><dl> <dt>**20**</dt> </dl> | Sistema riconfigurato.<br/>                                                                                             |
| <span id="21"></span><dl> <dt>**21**</dt> </dl> | Errore complesso della CPU non correggibile.<br/>                                                                                 |
| <span id="22"></span><dl> <dt>**22**</dt> </dl> | Reimpostazione o cancellazione dell'area log.<br/>                                                                                       |
| <span id="23"></span><dl> <dt>**23**</dt> </dl> | Avvio del sistema. Se implementata, questa voce di log è sicuramente la prima scritta in un qualsiasi avvio del sistema.<br/>        |



 

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di messaggio del log eventi. Questi messaggi corrispondono ai codici dei messaggi del registro eventi utilizzati per inserire i messaggi del registro eventi dal provider di consumer del registro eventi di Windows quando riceve uno degli eventi.

</dd> <dt>

**bit di convalida \_**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Bit di convalida usati per indicare la validità dei campi successivi. Il valore 1 (0x1) indica che l' **\_ evento SMBIOS** è valido.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **MSMCAEvent \_ SMBIOSError** è derivata da [**WmiEvent**](wmievent.md).

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

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

