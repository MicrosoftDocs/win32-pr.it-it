---
description: Costruisce un comando APDU (Application Protocol Data Unit) che avvia il calcolo dei dati di autenticazione dalla scheda usando i dati di richiesta di verifica inviati dal dispositivo di interfaccia e un segreto pertinente, ad esempio una chiave, archiviati nella scheda.
ms.assetid: cb0b2535-6e5b-4fb2-b540-cd037259baab
title: 'Metodo ISCardISO7816:: InternalAuthenticate (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.InternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1e30dbb06373907c5cea07e45d4f7a390b773349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049823"
---
# <a name="iscardiso7816internalauthenticate-method"></a>Metodo ISCardISO7816:: InternalAuthenticate

\[Il metodo **InternalAuthenticate** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **InternalAuthenticate** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che avvia il calcolo dei dati di autenticazione dalla scheda usando i dati di richiesta di verifica inviati dal dispositivo di interfaccia e un segreto pertinente, ad esempio una chiave, archiviati nella scheda.

Quando il segreto pertinente è collegato a MF, il comando può essere usato per autenticare la scheda nel suo complesso.

Quando il segreto pertinente è collegato a un altro DF, il comando può essere usato per autenticare tale DF.

## <a name="syntax"></a>Sintassi


```C++
HRESULT InternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in]      LONG         lReplyBytes,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byAlgorithmRef* \[ in\]
</dt> <dd>

Riferimento dell'algoritmo nella scheda.

Se questo valore è zero, indica che non viene fornita alcuna informazione. Il riferimento dell'algoritmo è noto prima di emettere il comando o viene fornito nel campo dati.

</dd> <dt>

*bySecretRef* \[ in\]
</dt> <dd>

Riferimento del segreto.



| Valore                                                                                                                                                                                    | Significato                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Nessuna informazione**</dt> </dl>                     | Posizione bit: 00000000 <br/> Non viene fornita alcuna informazione. Il riferimento del segreto è noto prima di emettere il comando o viene fornito nel campo dati.<br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Riferimento globale**</dt> </dl>         | Posizione bit: 0------- <br/> Dati di riferimento globali (chiave specifica MF).<br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Riferimento specifico**</dt> </dl> | Posizione bit: 1-------<br/> Dati di riferimento specifici (chiave specifica DF).<br/>                                                                                       |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | Posizione bit:-XX-----<br/> 00 (gli altri valori sono RFU).<br/>                                                                                                         |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**Segreto**</dt> </dl>                         | Posizione bit:---xxxxx<br/> Numero del segreto.<br/>                                                                                                              |



 

</dd> <dt>

*pChallenge* \[ in\]
</dt> <dd>

Puntatore ai dati correlati all'autenticazione (ad esempio, Challenge).

</dd> <dt>

*lReplyBytes* \[ in\]
</dt> <dd>

Numero massimo di byte previsti nella risposta.

</dd> <dt>

*ppCmd* \[ in uscita\]
</dt> <dd>

In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.

Al ritorno, viene compilato con il comando APDU creato da questa operazione. Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente utilizzando il puntatore *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

La corretta esecuzione del comando può essere soggetta a un completamento corretto dei comandi precedenti (ad esempio, VERIFY o SELECT FILE) o Selects (ad esempio, il segreto pertinente).

Se durante l'esecuzione del comando sono attualmente selezionati una chiave e un algoritmo, il comando può usare in modo implicito la chiave e l'algoritmo.

Il numero di volte in cui il comando viene emesso può essere registrato nella scheda per limitare il numero di tentativi successivi di utilizzo del segreto pertinente o dell'algoritmo.

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
