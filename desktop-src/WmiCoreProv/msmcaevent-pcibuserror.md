---
description: Rappresenta un errore del bus PCI di Machine Check Architecture (MCA). Questa classe è disponibile solo per i computer in esecuzione in un sistema operativo Windows a 64 bit.
ms.assetid: d8995909-a91b-4fcc-a37f-011d8df95ce8
title: MSMCAEvent_PCIBusError classe
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
ms.openlocfilehash: 4b3ae66c684ab6a0e2573e2c82d6087a3405ce3d8bef5704bb392337699daaea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051279"
---
# <a name="msmcaevent_pcibuserror-class"></a>Classe MSMCAEvent \_ PCIBusError

La **classe MSMCAEvent \_ PCIBusError** rappresenta un errore del bus PCI machine check architecture (MCA). Questa classe è disponibile solo per i computer in esecuzione in un sistema operativo Windows a 64 bit.

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

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

La **classe MSMCAEvent \_ PCIBusError** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MSMCAEvent \_ PCIBusError** ha queste proprietà.

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

**INDIRIZZO BUS PCI \_ \_**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Memoria o indirizzo di I/O nel bus PCI al momento dell'evento.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**COMANDO DEL BUS PCI \_ \_**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Comando o operazione del bus al momento dell'evento.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**DATI DEL BUS PCI \_ \_**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dati sul bus PCI al momento dell'evento.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**STATO ERRORE BUS PCI \_ \_ \_**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato del bus al momento dell'errore.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**TIPO DI ERRORE DEL BUS PCI \_ \_ \_**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di errore del bus PCI.



| Valore                                                                                                | Significato                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Errore sconosciuto o specifico del sistema OEM.<br/>            |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Errore di parità dei dati.<br/>                               |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Errore di sistema.<br/>                                    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Interruzione master.<br/>                                    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Timeout del bus o nessun dispositivo presente (NO \# DEVSEL).<br/> |
| <span id="5"></span><dl> <dt>**5**</dt> </dl> | Errore di parità dei dati master.<br/>                        |
| <span id="6"></span><dl> <dt>**6**</dt> </dl> | Errore di parità degli indirizzi.<br/>                            |
| <span id="7"></span><dl> <dt>**7**</dt> </dl> | Errore di parità del comando.<br/>                            |



 

</dd> <dt>

**PCI \_ BUS \_ ID \_ BusNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore designato per il bus PCI che ha rilevato l'errore.

</dd> <dt>

**PCI \_ BUS \_ ID \_ SegmentNumber**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore di segmento designato per il bus PCI che ha rilevato l'errore.

</dd> <dt>

**ID RICHIEDENTE BUS PCI \_ \_ \_**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del richiedente del bus PCI al momento dell'evento.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> <dt>

**ID \_ RISPONDITORE BUS PCI \_ \_**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore del risponditore del bus PCI al momento dell'evento.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

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

Bit di convalida utilizzati per indicare la validità dei campi successivi.



| Valori                                                                                  | Significato                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>1 (0x1)</dt> </dl>      | LO STATO DI ERRORE DEL BUS PCI \_ \_ è \_ valido.<br/>     |
| <dl> <dt>2 (0x2)</dt> </dl>      | IL TIPO DI ERRORE DEL BUS PCI \_ \_ è \_ valido.<br/>       |
| <dl> <dt>4 (0x4)</dt> </dl>      | L'ID BUS PCI \_ \_ è valido.<br/>                |
| <dl> <dt>8 (0x8)</dt> </dl>      | L'INDIRIZZO DEL BUS PCI \_ \_ è valido.<br/>           |
| <dl> <dt>16 (0x10)</dt> </dl>    | I DATI DEL BUS PCI \_ \_ sono validi.<br/>              |
| <dl> <dt>32 (0x20)</dt> </dl>    | IL COMANDO DEL BUS PCI \_ \_ è valido.<br/>               |
| <dl> <dt>64 (0x40)</dt> </dl>    | L'ID RICHIEDENTE DEL BUS PCI \_ \_ è \_ valido.<br/>     |
| <dl> <dt>128 (0x80)</dt> </dl>   | L'ID RISPONDITORE BUS PCI \_ \_ è \_ valido.<br/>     |
| <dl> <dt>256 (0x100)</dt> </dl>  | L'ID DI DESTINAZIONE DEL BUS PCI \_ \_ è \_ valido.<br/>        |
| <dl> <dt>512 (0x200)</dt> </dl>  | L'ID OEM del bus PCI \_ \_ è \_ valido.<br/>           |
| <dl> <dt>1024 (0x400)</dt> </dl> | LO \_ STRUCT DI DATI OEM DEL BUS PCI \_ \_ è \_ valido.<br/> |



 

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI.](/previous-versions//aa393262(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe MSMCAEvent \_ PCIBusError** è derivata da [**WMIEvent**](wmievent.md).

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

 

