---
description: Rappresenta un evento di errore di memoria mca (Machine Check Architecture). Questa classe è disponibile solo nei sistemi Windows a 64 bit.
ms.assetid: 0db1d526-e2c3-4e48-90c8-cbcd9121040e
title: MSMCAEvent_MemoryError classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryError
- MSMCAEvent_MemoryError.Active
- MSMCAEvent_MemoryError.AdditionalErrors
- MSMCAEvent_MemoryError.BUS_SPECIFIC_DATA
- MSMCAEvent_MemoryError.Cpu
- MSMCAEvent_MemoryError.ErrorSeverity
- MSMCAEvent_MemoryError.InstanceName
- MSMCAEvent_MemoryError.MEM_BANK
- MSMCAEvent_MemoryError.MEM_BIT_POSITION
- MSMCAEvent_MemoryError.MEM_CARD
- MSMCAEvent_MemoryError.MEM_COLUMN
- MSMCAEvent_MemoryError.MEM_ERROR_STATUS
- MSMCAEvent_MemoryError.MEM_MODULE
- MSMCAEvent_MemoryError.MEM_NODE
- MSMCAEvent_MemoryError.MEM_PHYSICAL_ADDR
- MSMCAEvent_MemoryError.MEM_PHYSICAL_MASK
- MSMCAEvent_MemoryError.MEM_ROW
- MSMCAEvent_MemoryError.RawRecord
- MSMCAEvent_MemoryError.RecordId
- MSMCAEvent_MemoryError.REQUESTOR_ID
- MSMCAEvent_MemoryError.RESPONDER_ID
- MSMCAEvent_MemoryError.Size
- MSMCAEvent_MemoryError.TARGET_ID
- MSMCAEvent_MemoryError.Type
- MSMCAEvent_MemoryError.VALIDATION_BITS
- MSMCAEvent_MemoryError.MEM_DEVICE
- MSMCAEvent_MemoryError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f93ac9ddda978a56ceb0e258766c2e60703acc94e92c551e673a9294e2cb984c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120981"
---
# <a name="msmcaevent_memoryerror-class"></a>Classe \_ MemoryError MSMCAEvent

La **classe MSMCAEvent \_ MemoryError** rappresenta un evento di errore di memoria mca (Machine Check Architecture). Questa classe è disponibile solo nei sistemi Windows a 64 bit.

La sintassi seguente è semplificata dal Managed Object Format (MOF) e include tutte le proprietà ereditate. Le proprietà e i metodi sono in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class MSMCAEvent_MemoryError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint64  BUS_SPECIFIC_DATA;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint16  MEM_BANK;
  uint16  MEM_BIT_POSITION;
  uint16  MEM_CARD;
  uint16  MEM_COLUMN;
  uint64  MEM_ERROR_STATUS;
  uint16  MEM_MODULE;
  uint16  MEM_NODE;
  uint64  MEM_PHYSICAL_ADDR;
  uint64  MEM_PHYSICAL_MASK;
  uint16  MEM_ROW;
  uint8   RawRecord[];
  uint64  RecordId;
  uint64  REQUESTOR_ID;
  uint64  RESPONDER_ID;
  uint32  Size;
  uint64  TARGET_ID;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint16  MEM_DEVICE;
  uint32  LogToEventlog;
};
```

## <a name="members"></a>Members

La **classe MSMCAEvent \_ MemoryError** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MSMCAEvent \_ MemoryError** ha queste proprietà.

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

**DATI \_ SPECIFICI DEL \_ BUS**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dati dipendenti dal bus specifici dell'OEM.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

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

Se zero, questo evento non viene registrato nel registro eventi di sistema.

</dd> <dt>

**MEM \_ BANK**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero modulo o RANK della posizione dell'errore di memoria.

</dd> <dt>

**POSIZIONE DEI BIT MEM \_ \_**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Posizione in bit nella parola di memoria che contiene l'errore.

</dd> <dt>

**SCHEDA \_ MEM**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di scheda del percorso dell'errore di memoria.

</dd> <dt>

**COLONNA \_ MEM**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di colonna della posizione dell'errore di memoria.

</dd> <dt>

**DISPOSITIVO \_ MEM**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di dispositivo della posizione dell'errore di memoria.

</dd> <dt>

**STATO ERRORE \_ \_ MEM**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato dell'errore di memoria.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**MODULO \_ MEM**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di modulo o di classificazione della posizione dell'errore di memoria.

</dd> <dt>

**NODO \_ MEM**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nodo che contiene l'errore di memoria. Questa proprietà si applica solo in un sistema a più nodi. Questa proprietà è specifica del fornitore.

</dd> <dt>

**COMPONENTE AGGIUNTIVO \_ FISICO \_ MEM**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo fisico dell'errore di memoria.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**MASCHERA \_ FISICA MEM \_**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Bit di indirizzo validi nell'indirizzo fisico a 64 bit dell'errore di memoria.

> [!Note]  
> La maschera fisica specifica la granularità dell'indirizzo fisico. L'indirizzo fisico dell'errore di memoria dipende dai fattori di implementazione dell'hardware.

 

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**RIGA \_ MEM**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di riga della posizione dell'errore di memoria.

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

**ID \_ RICHIEDENTE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo hardware del dispositivo o del componente che avvia la transazione.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**ID \_ RISPONDITORE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo hardware del risponditore alla transazione.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Dimensioni**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensione in byte del record di errore non elaborato.

</dd> <dt>

**ID \_ DESTINAZIONE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indirizzo hardware della destinazione prevista della transazione.

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di messaggio del registro eventi. Questi messaggi corrispondono ai codici dei messaggi del registro eventi usati per inserire i messaggi del registro eventi dal provider consumer del registro eventi Windows quando riceve uno degli eventi.

</dd> <dt>

**BIT \_ DI CONVALIDA**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Bit di convalida usati per indicare la validità dei campi successivi.



| Valori                                                                                     | Significato                                                 |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <dt>1 (0x1)</dt> </dl>         | MEM \_ ERROR STATUS è \_ valido.<br/>                 |
| <dl> <dt>2 (0x2)</dt> </dl>         | MEM \_ PHYSICAL \_ ADDR è valido.<br/>                |
| <dl> <dt>4 (0x4)</dt> </dl>         | MEM \_ ADDR \_ MASK è valido.<br/>                    |
| <dl> <dt>8 (0x8)</dt> </dl>         | IL NODO MEM \_ è valido.<br/>                          |
| <dl> <dt>16 (0x10)</dt> </dl>       | LA SCHEDA MEM \_ è valida.<br/>                          |
| <dl> <dt>32 (0x20)</dt> </dl>       | MEM \_ MODULE è valido.<br/>                        |
| <dl> <dt>64 (0x40)</dt> </dl>       | MEM \_ BANK è valido.<br/>                          |
| <dl> <dt>128 (0x80)</dt> </dl>      | IL DISPOSITIVO MEM \_ è valido.<br/>                        |
| <dl> <dt>256 (0x100)</dt> </dl>     | MEM \_ ROW è valido.<br/>                           |
| <dl> <dt>512 (0x200)</dt> </dl>     | MEM \_ COLUMN è valido.<br/>                        |
| <dl> <dt>1024 (0x400)</dt> </dl>    | MEM \_ BIT POSITION è \_ valido.<br/>                 |
| <dl> <dt>2048 (0x800)</dt> </dl>    | L'ID DEL RICHIEDENTE DELLA PIATTAFORMA MEM \_ \_ è \_ valido.<br/>       |
| <dl> <dt>4096 (0x1000)</dt> </dl>   | L'ID RISPONDITORE PIATTAFORMA MEM \_ \_ è \_ valido.<br/>       |
| <dl> <dt>8192 (0x2000)</dt> </dl>   | MEM \_ PLATFORM TARGET è \_ valido.<br/>              |
| <dl> <dt>16384 (0x4000)</dt> </dl>  | I DATI SPECIFICI DEL BUS DELLA PIATTAFORMA MEM \_ \_ sono \_ \_ validi.<br/> |
| <dl> <dt>32768 (0x8000)</dt> </dl>  | L'ID OEM della piattaforma MEM \_ \_ è \_ valido.<br/>             |
| <dl> <dt>65536 (0x10000)</dt> </dl> | MEM \_ PLATFORM \_ OEM DATA \_ \_ STRUCT è valido.<br/>   |



 

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe MSMCAEvent \_ MemoryError** è derivata da [**WMIEvent**](wmievent.md).

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

 

