---
description: La \_ classe WMI SerialPortConfiguration Win32 rappresenta le impostazioni per la trasmissione dei dati su una porta seriale basata su Windows. Sono incluse le configurazioni per stabilire una connessione e il controllo degli errori.
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Classe Win32_SerialPortConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortConfiguration
- Win32_SerialPortConfiguration.Caption
- Win32_SerialPortConfiguration.Description
- Win32_SerialPortConfiguration.SettingID
- Win32_SerialPortConfiguration.AbortReadWriteOnError
- Win32_SerialPortConfiguration.BaudRate
- Win32_SerialPortConfiguration.BinaryModeEnabled
- Win32_SerialPortConfiguration.BitsPerByte
- Win32_SerialPortConfiguration.ContinueXMitOnXOff
- Win32_SerialPortConfiguration.CTSOutflowControl
- Win32_SerialPortConfiguration.DiscardNULLBytes
- Win32_SerialPortConfiguration.DSROutflowControl
- Win32_SerialPortConfiguration.DSRSensitivity
- Win32_SerialPortConfiguration.DTRFlowControlType
- Win32_SerialPortConfiguration.EOFCharacter
- Win32_SerialPortConfiguration.ErrorReplaceCharacter
- Win32_SerialPortConfiguration.ErrorReplacementEnabled
- Win32_SerialPortConfiguration.EventCharacter
- Win32_SerialPortConfiguration.IsBusy
- Win32_SerialPortConfiguration.Name
- Win32_SerialPortConfiguration.Parity
- Win32_SerialPortConfiguration.ParityCheckEnabled
- Win32_SerialPortConfiguration.RTSFlowControlType
- Win32_SerialPortConfiguration.StopBits
- Win32_SerialPortConfiguration.XOffCharacter
- Win32_SerialPortConfiguration.XOffXMitThreshold
- Win32_SerialPortConfiguration.XOnCharacter
- Win32_SerialPortConfiguration.XOnXMitThreshold
- Win32_SerialPortConfiguration.XOnXOffInFlowControl
- Win32_SerialPortConfiguration.XOnXOffOutFlowControl
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 065d069b261472e3347a115cfbbff652812b6622
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965953"
---
# <a name="win32_serialportconfiguration-class"></a>Win32 \_ SerialPortConfiguration (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SerialPortConfiguration Win32** rappresenta le impostazioni per la trasmissione dei dati su una porta seriale basata su Windows. Sono incluse le configurazioni per stabilire una connessione e il controllo degli errori.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AbortReadWriteOnError;
  uint32  BaudRate;
  boolean BinaryModeEnabled;
  uint32  BitsPerByte;
  boolean ContinueXMitOnXOff;
  boolean CTSOutflowControl;
  boolean DiscardNULLBytes;
  boolean DSROutflowControl;
  boolean DSRSensitivity;
  string  DTRFlowControlType;
  uint32  EOFCharacter;
  uint32  ErrorReplaceCharacter;
  boolean ErrorReplacementEnabled;
  uint32  EventCharacter;
  boolean IsBusy;
  string  Name;
  string  Parity;
  boolean ParityCheckEnabled;
  string  RTSFlowControlType;
  string  StopBits;
  uint32  XOffCharacter;
  uint32  XOffXMitThreshold;
  uint32  XOnCharacter;
  uint32  XOnXMitThreshold;
  uint32  XOnXOffInFlowControl;
  uint32  XOnXOffOutFlowControl;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ SerialPortConfiguration** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ SerialPortConfiguration** dispone di queste proprietà.

<dl> <dt>

**AbortReadWriteOnError**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fAbortOnError")
</dt> </dl>

Se **true**, le operazioni di lettura e scrittura vengono interrotte se si verifica un errore. Se **true**, il driver termina tutte le operazioni di lettura e scrittura con uno stato di errore se si verifica un errore. Il driver non accetterà ulteriori operazioni di comunicazione fino a quando l'errore non verrà riconosciuto dall'applicazione.

</dd> <dt>

**BaudRate**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| baud")
</dt> </dl>

Velocità in baud (bit al secondo) con cui il dispositivo di comunicazione funziona.

Esempio: 9600

</dd> <dt>

**BinaryModeEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary")
</dt> </dl>

Se **true**, i trasferimenti di dati in modalità binaria sono abilitati per la porta seriale. I sistemi di computer che eseguono Windows supportano solo i trasferimenti binari tramite porte seriali, quindi questo valore è sempre **true**.

</dd> <dt>

**BitsPerByte**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ByteSize")
</dt> </dl>

Numero di bit trasmessi e ricevuti per ogni byte di dati per la porta seriale di Windows. Il numero può variare con i bit di controllo e di correzione degli errori, ad esempio i bit di parità.

Esempio: 8

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**ContinueXMitOnXOff**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fTXContinueOnXoff")
</dt> </dl>

Se è **true**, le trasmissioni dei dati continuano quando il buffer di input si trova all'interno di **XOffXMitThreshold** byte di piena e il driver ha trasmesso il valore **XOffChararcter** per interrompere la ricezione dei byte. Se **false**, la trasmissione non continua fino a quando il buffer di input non si trova all'interno di **XOnXMitThreshold** byte di essere vuoto e il driver ha trasmesso il valore **XOnCharacter** per riprendere la ricezione.

</dd> <dt>

**CTSOutflowControl**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxCtsFlow")
</dt> </dl>

Se **true**, il segnale CTS (Clear to Send) viene verificato prima della trasmissione dei dati. CTS segnala che entrambi i dispositivi della connessione seriale sono pronti per il trasferimento dei dati. La trasmissione dei dati viene sospesa fino a quando non viene specificato il segnale CTS.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**DiscardNULLBytes**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fNull")
</dt> </dl>

Se **true**, i byte **null** (caratteri) vengono eliminati quando vengono ricevuti.

</dd> <dt>

**DSROutflowControl**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxDsrFlow")
</dt> </dl>

Se **true**, il controllo del flusso di dati è abilitato quando è presente una condizione del set di dati (DSR). Il DSR segnala che la connessione è stata stabilita dai dispositivi sulla connessione seriale. La trasmissione dei dati DSR viene sospesa fino a quando non viene specificato il segnale DSR.

</dd> <dt>

**Riservatezza DSR**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDsrSensitivity")
</dt> </dl>

Se **true**, il driver di comunicazione è sensibile allo stato del segnale DSR. Il driver ignora tutti i byte ricevuti, a meno che la riga di input del modem DSR non sia alta.

</dd> <dt>

**DTRFlowControlType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDtrControl")
</dt> </dl>

Uso del controllo di flusso Data Terminal Ready (DTR) dopo che è stata stabilita una connessione.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Enable** ("Enable")


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Disabilita** ("Disabilita")


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

**Handshake** ("handshake")


</dt> <dd></dd> </dl>

</dd> <dt>

**Carattere EOF**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EofChar")
</dt> </dl>

Valore del carattere utilizzato per segnalare la fine dei dati.

Esempio: ^ Z

</dd> <dt>

**ErrorReplaceCharacter**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ErrorChar")
</dt> </dl>

Valore del carattere utilizzato per sostituire i byte ricevuti con un errore di parità.

Esempio: ^ C

</dd> <dt>

**ErrorReplacementEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fErrorChar")
</dt> </dl>

Se **true**, i byte ricevuti con errori di parità vengono sostituiti con il valore **ErrorReplaceCharacter** . I caratteri con errori di parità vengono sostituiti solo se questa proprietà è **true** e la parità è abilitata.

</dd> <dt>

**EventCharacter**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EvtChar")
</dt> </dl>

Valore del carattere di controllo utilizzato per segnalare un evento, ad esempio la fine del file.

Esempio: ^ e

</dd> <dt>

**Della proprietà IsBusy**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| file functions \| CreateFile")
</dt> </dl>

Se **true**, la porta seriale è occupata.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ DeviceMap \\ \\ SerialComm")
</dt> </dl>

Nome della porta seriale di Windows.

Esempio: "COM1"

</dd> <dt>

**Parity**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| parità")
</dt> </dl>

Metodo di controllo della parità da usare. La parità viene utilizzata come una tecnica di controllo degli errori in cui è incluso un bit di parità aggiuntivo con ogni unità di dati. Il ricevitore può quindi verificare la validità dei dati contando i bit impostati.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**None** ("None")


</dt> <dd>

Controllo della parità non utilizzato.

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Dispari ("dispari"** )


</dt> <dd>

Imposta il bit di parità in modo che il numero di bit sia dispari.

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Even** ("even")


</dt> <dd>

Imposta il bit di parità in modo che il numero di bit sia pari.

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Contrassegno** ("contrassegno")


</dt> <dd>

Lascia il bit di parità impostato su 1.

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Spazio** ("spazio")


</dt> <dd>

Lascia il bit di parità impostato su 0 (zero).

</dd> </dl>

</dd> <dt>

**ParityCheckEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fParity")
</dt> </dl>

Se **true**, il controllo della parità è abilitato.

</dd> <dt>

**RTSFlowControlType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Controllo di flusso RTS (request to Send). RTS viene usato per segnalare che i dati sono disponibili per la trasmissione.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Enable** ("Enable")


</dt> <dd>

La sessione RTS è stata lasciata per la sessione di trasferimento dati.

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disabilita** ("Disabilita")


</dt> <dd>

RTS viene ignorato dopo la ricezione del primo segnale RTS.

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Handshake** ("handshake")


</dt> <dd>

RTS è disattivato se il buffer di trasmissione è pieno di tre trimestri e RTS viene attivato quando il buffer è inferiore a una metà.

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Interruttore** ("interruttore")


</dt> <dd>

RTS viene attivato se sono presenti dati memorizzati nel buffer per la trasmissione.

</dd> </dl>

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificatore con cui è noto l'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**StopBits**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Stop")
</dt> </dl>

Numero di bit di interruzione da usare. I bit stop separano ogni unità di dati in una connessione seriale asincrona. Vengono inoltre inviati continuamente quando non sono disponibili dati per la trasmissione.

<dt>

<span id="1"></span>

**1** ("1")


</dt> <dd></dd> <dt>

<span id="1.5"></span>

**1,5** ("1,5")


</dt> <dd></dd> <dt>

<span id="2"></span>

**2** ("2")


</dt> <dd></dd> </dl>

</dd> <dt>

**XOffCharacter**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffChar")
</dt> </dl>

Valore del carattere XOFF per la trasmissione e la ricezione. XOFF è un controllo software per arrestare la trasmissione dei dati (mentre RTS e CTS sono controlli hardware). XON riprende la trasmissione.

</dd> <dt>

**XOffXMitThreshold**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffLim")
</dt> </dl>

Numero massimo di byte consentiti nel buffer di input prima dell'invio del carattere XOFF.

</dd> <dt>

**XOnCharacter**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonChar")
</dt> </dl>

Valore del carattere XON per la trasmissione e la ricezione. XON è un controllo software per riprendere la trasmissione dei dati (mentre RTS e CTS sono controlli hardware). XOFF interrompe la trasmissione.

</dd> <dt>

**XOnXMitThreshold**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonLim")
</dt> </dl>

Numero minimo di byte consentiti nel buffer di input prima che il carattere XON venga inviato. Questa proprietà funziona insieme a **XOffXMitThreshold** per regolare la velocità di trasferimento dei dati.

</dd> <dt>

**XOnXOffInFlowControl**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fInX")
</dt> </dl>

Se **true**, il controllo di flusso XON/XOFF viene usato durante la ricezione. Se **true**, il valore **XOffCharacter** viene inviato quando il buffer di input si trova all'interno di **XOffXMitThreshold** byte di riempimento e il valore di **XOnCharacter** viene inviato quando il buffer di input rientra in **XOnXMitThreshold** byte di essere vuoto.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

FALSE

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

true

</dd> </dl>

</dd> <dt>

**XOnXOffOutFlowControl**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutX")
</dt> </dl>

**XOnXOffOutFlowControl** specifica se il controllo di flusso XON o XOFF viene usato durante la trasmissione. Se è **true**, la trasmissione si interrompe quando viene ricevuto il valore **XOffCharacter** e viene riavviato quando viene ricevuto il valore **XOnCharacter** .

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ SerialPortConfiguration** deriva dall' [**\_ impostazione CIM**](cim-setting.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Impostazione CIM**](cim-setting.md)
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

 
