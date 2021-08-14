---
description: Costruisce un comando APDU (Application Protocol Data Unit) che avvia il calcolo dei dati di autenticazione tramite la scheda usando i dati di richiesta inviati dal dispositivo di interfaccia e un segreto pertinente (ad esempio, una chiave) archiviato nella scheda.
ms.assetid: cb0b2535-6e5b-4fb2-b540-cd037259baab
title: Metodo ISCardISO7816::InternalAuthenticate (Scardssp.h)
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
ms.openlocfilehash: d4c3385313fb5b9c9c7ba72957244bd81757b0cd1e79bcec906e740c69b66292
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922991"
---
# <a name="iscardiso7816internalauthenticate-method"></a>Metodo ISCardISO7816::InternalAuthenticate

\[Il **metodo InternalAuthenticate** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il metodo **InternalAuthenticate** costruisce un comando APDU [*(Application Protocol Data Unit)*](../secgloss/a-gly.md) che avvia il calcolo dei dati di autenticazione tramite la scheda usando i dati di richiesta inviati dal dispositivo di interfaccia e un segreto pertinente (ad esempio, una chiave) archiviato nella scheda.

Quando il segreto pertinente è collegato all'MF, il comando può essere usato per autenticare l'intera scheda.

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

*byAlgorithmRef* \[ Pollici\]
</dt> <dd>

Riferimento dell'algoritmo nella scheda.

Se questo valore è zero, significa che non vengono fornite informazioni. Il riferimento dell'algoritmo è noto prima di eseguire il comando o viene fornito nel campo dati.

</dd> <dt>

*bySecretRef* \[ Pollici\]
</dt> <dd>

Riferimento del segreto.



| Valore                                                                                                                                                                                    | Significato                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Nessuna informazione**</dt> </dl>                     | Posizione bit: 00000000 <br/> Non vengono fornite informazioni. Il riferimento del segreto è noto prima di eseguire il comando o viene fornito nel campo dati.<br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Riferimento globale**</dt> </dl>         | Posizione bit: 0------- <br/> Dati di riferimento globali (una chiave specifica di MF).<br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Riferimento specifico**</dt> </dl> | Posizione bit: 1-------<br/> Dati di riferimento specifici (una chiave specifica di DF).<br/>                                                                                       |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**Rfu**</dt> </dl>                                                           | Posizione di bit: -xx-----<br/> 00 (gli altri valori sono RFU).<br/>                                                                                                         |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**Segreto**</dt> </dl>                         | Posizione di bit: ---xxxxx<br/> Numero del segreto.<br/>                                                                                                              |



 

</dd> <dt>

*pChallenge* \[ Pollici\]
</dt> <dd>

Puntatore ai dati correlati all'autenticazione , ad esempio challenge.

</dd> <dt>

*lReplyBytes* \[ Pollici\]
</dt> <dd>

Numero massimo di byte previsti nella risposta.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

In input, puntatore a un [**oggetto interfaccia ISCardCmd**](iscardcmd.md) o **NULL.**

In caso di restituzione, viene riempito con il comando APDU costruito da questa operazione. Se *ppCmd è* stato impostato su **NULL,** un [*smart card*](../secgloss/s-gly.md) [**isCardCmd**](iscardcmd.md) viene creato internamente e restituito usando il *puntatore ppCmd.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

L'esecuzione corretta del comando può essere soggetta al corretto completamento di comandi precedenti (ad esempio VERIFY o SELECT FILE) o selezioni (ad esempio, il segreto pertinente).

Se una chiave e un algoritmo sono attualmente selezionati durante l'emissione del comando, il comando può usare in modo implicito la chiave e l'algoritmo.

Il numero di volte in cui il comando viene eseguito può essere registrato nella scheda per limitare il numero di altri tentativi di utilizzo del segreto o dell'algoritmo pertinente.

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore smart card se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
