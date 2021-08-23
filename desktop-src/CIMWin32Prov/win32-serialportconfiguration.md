---
description: La classe WMI Win32 SerialPortConfiguration rappresenta le impostazioni per la trasmissione dei dati \_ su una Windows seriale basata su una porta seriale. Sono incluse le configurazioni per stabilire una connessione e il controllo degli errori.
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Win32_SerialPortConfiguration classe
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
ms.openlocfilehash: 07052c0366b32904ef6bf6f52b15f3ea98022ba8385120ec60cdefe5714e2c4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079695"
---
# <a name="win32_serialportconfiguration-class"></a>Classe SerialPortConfiguration Win32 \_

La classe [WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ SerialPortConfiguration** rappresenta le impostazioni per la trasmissione dei dati su una Windows seriale basata su una porta seriale. Sono incluse le configurazioni per stabilire una connessione e il controllo degli errori.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

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

La **classe Win32 \_ SerialPortConfiguration** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ SerialPortConfiguration** ha queste proprietà.

<dl> <dt>

**AbortReadWriteOnError**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fAbortOnError")
</dt> </dl>

Se **TRUE,** le operazioni di lettura e scrittura vengono terminate se si verifica un errore. Se **TRUE,** il driver termina tutte le operazioni di lettura e scrittura con uno stato di errore se si verifica un errore. Il driver non accetterà altre operazioni di comunicazione fino a quando l'applicazione non riconosce l'errore.

</dd> <dt>

**Baudrate**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| BaudRate")
</dt> </dl>

Velocità in baud (bit al secondo) alla quale opera il dispositivo di comunicazione.

Esempio: 9600

</dd> <dt>

**BinaryModeEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary")
</dt> </dl>

Se **TRUE,** i trasferimenti di dati in modalità binaria sono abilitati per la porta seriale. I computer che eseguono Windows solo i trasferimenti binari tramite porte seriali, quindi questo valore è sempre **TRUE.**

</dd> <dt>

**BitsPerByte**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione WIN32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ByteSize")
</dt> </dl>

Numero di bit trasmessi e ricevuti per ogni byte di dati per la Windows seriale. Il numero può variare con i bit di controllo e correzione degli errori, ad esempio i bit di parità.

Esempio: 8

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**ContinueXMitOnXOff**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fTXContinueOnXoff")
</dt> </dl>

Se **TRUE,** le trasmissioni di dati continuano quando il buffer di input rientra nei byte **XOffXMitThreshold** di essere pieno e il driver ha trasmesso il **valore XOffChararcter** per arrestare la ricezione dei byte. Se **FALSE,** la trasmissione non continua finché il buffer di input non rientra nei byte **XOnXMitThreshold** di essere vuoto e il driver non ha trasmesso il **valore XOnCharacter** per riprendere la ricezione.

</dd> <dt>

**CTSOutflowControl**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxCtsFlow")
</dt> </dl>

Se **TRUE,** il segnale clear to send (CTS) viene controllato prima della trasmissione dei dati. CTS segnala che entrambi i dispositivi nella connessione seriale sono pronti per il trasferimento dei dati. La trasmissione dei dati viene sospesa fino a quando non viene fornito il segnale CTS.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**DiscardNULLBytes**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fNull")
</dt> </dl>

Se **TRUE,** **i byte NULL** (caratteri) vengono eliminati quando vengono ricevuti.

</dd> <dt>

**DSROutflowControl**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxDsrFlow")
</dt> </dl>

Se **TRUE,** il controllo del flusso di uscita dei dati è abilitato quando è presente una condizione DSR (Data Set Ready). DSR segnala che la connessione è stata stabilita dai dispositivi nella connessione seriale. La trasmissione dei dati DSR viene sospesa fino a quando non viene fornito il segnale DSR.

</dd> <dt>

**DSRSensitivity**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDsrSensitivity")
</dt> </dl>

Se **TRUE,** il driver di comunicazione è sensibile allo stato del segnale DSR. Il driver ignora i byte ricevuti, a meno che la linea di input del modem DSR non sia elevata.

</dd> <dt>

**DTRFlowControlType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDtrControl")
</dt> </dl>

Uso del controllo di flusso pronto per il terminale dati (DTR) dopo che è stata stabilita una connessione.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Abilita** ("Abilita")


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Disabilita** ("Disabilita")


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

**Handshake** ("Handshake")


</dt> <dd></dd> </dl>

</dd> <dt>

**EOFCharacter**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EofChar")
</dt> </dl>

Valore del carattere utilizzato per segnalare la fine dei dati.

Esempio: ^Z

</dd> <dt>

**ErrorReplaceCharacter**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione WIN32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ErrorChar")
</dt> </dl>

Valore del carattere utilizzato per sostituire i byte ricevuti con un errore di parità.

Esempio: ^C

</dd> <dt>

**ErrorReplacementEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fErrorChar")
</dt> </dl>

Se **TRUE,** i byte ricevuti con errori di parità vengono sostituiti con il **valore ErrorReplaceCharacter.** I caratteri con errori di parità vengono sostituiti solo se questa proprietà è **TRUE** e la parità è abilitata.

</dd> <dt>

**EventCharacter**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EvtChar")
</dt> </dl>

Valore del carattere di controllo utilizzato per segnalare un evento, ad esempio la fine del file.

Esempio: ^e

</dd> <dt>

**Isbusy**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funzioni file Win32API \| \| CreateFile")
</dt> </dl>

Se **TRUE,** la porta seriale è occupata.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**key,**](../wmisdk/key-qualifier.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ DeviceMap \\ \\ SerialComm")
</dt> </dl>

Nome della Windows seriale.

Esempio: "COM1"

</dd> <dt>

**Parity**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Parity")
</dt> </dl>

Metodo di controllo della parità da usare. La parità viene usata come tecnica di controllo degli errori in cui un bit di parità aggiuntivo è incluso in ogni unità di dati. Il ricevitore può quindi verificare la validità dei dati contando i bit impostati.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Nessuno** ("None")


</dt> <dd>

Controllo di parità non usato.

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Dispari** ("Dispari")


</dt> <dd>

Imposta il bit di parità in modo che il numero di bit sia dispari.

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Even** ("Even")


</dt> <dd>

Imposta il bit di parità in modo che il numero di bit sia pari.

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Mark** ("Mark")


</dt> <dd>

Lascia il bit di parità impostato su 1.

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Spazio** ("Spazio")


</dt> <dd>

Lascia il bit di parità impostato su 0 (zero).

</dd> </dl>

</dd> <dt>

**ParityCheckEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fParity")
</dt> </dl>

Se **TRUE,** il controllo di parità è abilitato.

</dd> <dt>

**RTSFlowControlType**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Richiesta di invio del controllo di flusso (RTS). RTS viene usato per segnalare che i dati sono disponibili per la trasmissione.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Abilita** ("Abilita")


</dt> <dd>

RTS rimane attiva per la sessione di trasferimento dei dati.

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disabilita** ("Disabilita")


</dt> <dd>

RTS viene ignorato dopo la ricezione del primo segnale RTS.

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Handshake** ("Handshake")


</dt> <dd>

RTS è disattivato se il buffer di trasmissione è pieno più di tre trimestri e RTS è attivato quando il buffer è meno della metà pieno.

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Attivazione/disattivazione** ("Attiva/Disattiva")


</dt> <dd>

RTS è attivato se sono presenti dati memorizzati nel buffer per la trasmissione.

</dd> </dl>

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificatore con cui è noto l'oggetto corrente.

Questa proprietà viene ereditata [**dall'impostazione CIM \_**](cim-setting.md).

</dd> <dt>

**StopBits**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione WIN32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| StopBits")
</dt> </dl>

Numero di bit di arresto da utilizzare. I bit di arresto separano ogni unità di dati in una connessione seriale asincrona. Vengono inoltre inviati in modo continuo quando non sono disponibili dati per la trasmissione.

<dt>

<span id="1"></span>

**1** ("1")


</dt> <dd></dd> <dt>

<span id="1.5"></span>

**1.5** ("1.5")


</dt> <dd></dd> <dt>

<span id="2"></span>

**2** ("2")


</dt> <dd></dd> </dl>

</dd> <dt>

**XOffCharacter**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffChar")
</dt> </dl>

Valore del carattere XOFF sia per la trasmissione che per la ricezione. XOFF è un controllo software per arrestare la trasmissione dei dati (mentre RTS e CTS sono controlli hardware). XON riprende la trasmissione.

</dd> <dt>

**XOffXMitThreshold**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffLim")
</dt> </dl>

Numero massimo di byte consentiti nel buffer di input prima dell'invio del carattere XOFF.

</dd> <dt>

**XOnCharacter**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonChar")
</dt> </dl>

Valore del carattere XON per la trasmissione e la ricezione. XON è un controllo software per riprendere la trasmissione dei dati (mentre RTS e CTS sono controlli hardware). XOFF arresta la trasmissione.

</dd> <dt>

**XOnXMitThreshold**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonLim")
</dt> </dl>

Numero minimo di byte consentiti nel buffer di input prima dell'invio del carattere XON. Questa proprietà funziona in combinazione **con XOffXMitThreshold** per regolare la velocità di trasferimento dei dati.

</dd> <dt>

**XOnXOffInFlowControl**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fInX")
</dt> </dl>

Se **TRUE,** durante la ricezione viene usato il controllo di flusso XON/XOFF. Se **TRUE,** il valore **XOffCharacter** viene inviato quando il buffer di input rientra nei byte **XOffXMitThreshold** per essere pieno e il valore **XOnCharacter** viene inviato quando il buffer di input rientra nei byte **XOnXMitThreshold** di essere vuoto.

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

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Strutture di comunicazione Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutX")
</dt> </dl>

**XOnXOffOutFlowControl** specifica se il controllo di flusso XON o XOFF viene usato durante la trasmissione. Se **TRUE,** la trasmissione si interrompe quando viene ricevuto il valore **XOffCharacter** e viene nuovamente avviata quando viene ricevuto il **valore XOnCharacter.**

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe Win32 \_ SerialPortConfiguration** è derivata dall'impostazione [**CIM \_**](cim-setting.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazione \_ CIM**](cim-setting.md)
</dt> <dt>

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> </dl>

 

 
