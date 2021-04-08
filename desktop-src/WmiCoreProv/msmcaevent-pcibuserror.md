---
description: Rappresenta un errore del bus PCI MCA (Machine Check Architecture). Questa classe è disponibile solo per i computer che eseguono un sistema operativo Windows a 64 bit.
ms.assetid: d8995909-a91b-4fcc-a37f-011d8df95ce8
title: Classe MSMCAEvent_PCIBusError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIBusError
- MSMCAEvent_PCIBusError.Active
- MSMCAEvent_PCIBusError.AdditionalErrors
- MSMCAEvent_PCIBusError.Cpu
- MSMCAEvent_PCIBusError.ErrorSeverity
- MSMCAEvent_PCIBusError.InstanceName
- MSMCAEvent_PCIBusError.PCI_BUS_ADDRESS
- MSMCAEvent_PCIBusError.PCI_BUS_CMD
- MSMCAEvent_PCIBusError.PCI_BUS_DATA
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_STATUS
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_TYPE
- MSMCAEvent_PCIBusError.PCI_BUS_ID_BusNumber
- MSMCAEvent_PCIBusError.PCI_BUS_ID_SegmentNumber
- MSMCAEvent_PCIBusError.PCI_BUS_REQUESTOR_ID
- MSMCAEvent_PCIBusError.PCI_BUS_RESPONDER_ID
- MSMCAEvent_PCIBusError.RawRecord
- MSMCAEvent_PCIBusError.RecordId
- MSMCAEvent_PCIBusError.Size
- MSMCAEvent_PCIBusError.Type
- MSMCAEvent_PCIBusError.VALIDATION_BITS
- MSMCAEvent_PCIBusError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 7f2b800a07c0b979468a5df5a8be67e6adee39de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751383"
---
# <a name="msmcaevent_pcibuserror-class"></a>\_Classe MSMCAEvent PCIBusError

La classe **MSMCAEvent \_ PCIBusError** rappresenta un errore del bus PCI MCA (Machine Check Architecture). Questa classe è disponibile solo per i computer che eseguono un sistema operativo Windows a 64 bit.

La sintassi seguente è semplificata dal codice Managed Object Format (MOF) e include tutte le relative proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MSMCAEvent_PCIBusError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_BUS_ADDRESS;
  uint64  PCI_BUS_CMD;
  uint64  PCI_BUS_DATA;
  uint64  PCI_BUS_ERROR_STATUS;
  uint16  PCI_BUS_ERROR_TYPE;
  uint8   PCI_BUS_ID_BusNumber;
  uint8   PCI_BUS_ID_SegmentNumber;
  uint64  PCI_BUS_REQUESTOR_ID;
  uint64  PCI_BUS_RESPONDER_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Members

La **classe \_ PCIBusError di MSMCAEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ PCIBusError di MSMCAEvent** dispone di queste proprietà.

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

**\_indirizzo bus \_ PCI**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Memoria o indirizzo di I/O sul bus PCI al momento dell'evento.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_cmd bus \_ PCI**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Comando o operazione del bus al momento dell'evento.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_dati bus \_ PCI**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dati sul bus PCI al momento dell'evento.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_ \_ stato errore bus \_ PCI**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato del bus al momento dell'errore.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_tipo di \_ errore \_ bus PCI**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di errore del bus PCI.



| Valore                                                                                                | Significato                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Errore specifico di sistema sconosciuto o OEM.<br/>            |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Errore di parità dei dati.<br/>                               |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Errore di sistema.<br/>                                    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Interruzione principale.<br/>                                    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Timeout del bus o nessun dispositivo disponibile (nessun DEVSEL \# ).<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Errore di parità dei dati master.<br/>                        |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Errore di parità degli indirizzi.<br/>                            |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Errore di parità del comando.<br/>                            |



 

</dd> <dt>

**\_ID bus \_ PCI \_ BusNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore designato per il bus PCI che ha rilevato l'errore.

</dd> <dt>

**\_ID bus \_ PCI \_ SegmentNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore di segmento designato per il bus PCI che ha rilevato l'errore.

</dd> <dt>

**\_ \_ ID richiedente bus \_ PCI**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del richiedente del bus PCI al momento dell'evento.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**\_ \_ ID risponditore bus \_ PCI**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del risponditore del bus PCI al momento dell'evento.

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**RawRecord**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di byte che contiene il record di errore non elaborato presentato a Windows da System Abstraction Layer (SAL). Il numero di elementi nella matrice è specificato dalla proprietà **size** .

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

Bit di convalida usati per indicare la validità dei campi successivi.



| Valori                                                                                  | Significato                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>1 (0x1)</dt> </dl>      | \_Lo stato di errore del bus PCI \_ \_ è valido.<br/>     |
| <dl> <dt>2 (0x2)</dt> </dl>      | Il \_ tipo di errore del bus PCI \_ \_ è valido.<br/>       |
| <dl> <dt>4 (0x4)</dt> </dl>      | \_ID bus PCI \_ valido.<br/>                |
| <dl> <dt>8 (0x8)</dt> </dl>      | \_Indirizzo bus PCI \_ valido.<br/>           |
| <dl> <dt>16 (0x10)</dt> </dl>    | \_I dati del bus PCI \_ sono validi.<br/>              |
| <dl> <dt>32 (0x20)</dt> </dl>    | Il valore \_ cmd del bus PCI \_ è valido.<br/>               |
| <dl> <dt>64 (0x40)</dt> </dl>    | \_ \_ ID richiedente bus PCI \_ valido.<br/>     |
| <dl> <dt>128 (0x80)</dt> </dl>   | \_ \_ ID risponditore bus PCI \_ valido.<br/>     |
| <dl> <dt>256 (0x100)</dt> </dl>  | \_ \_ ID destinazione bus PCI \_ valido.<br/>        |
| <dl> <dt>512 (0x200)</dt> </dl>  | \_ID OEM del bus PCI \_ \_ valido.<br/>           |
| <dl> <dt>1024 (0x400)</dt> </dl> | Lo \_ struct di dati OEM del bus PCI \_ \_ \_ è valido.<br/> |



 

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **MSMCAEvent \_ PCIBusError** è derivata da [**WmiEvent**](wmievent.md).

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

 

