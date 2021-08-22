---
description: Il metodo ReadRecord costruisce un comando APDU (Application Protocol Data Unit) che legge il contenuto dei record specificati o la parte iniziale di un record di un file elementare.
ms.assetid: b00a3242-93bc-4779-8c62-89157fbcb5d1
title: Metodo ISCardISO7816::ReadRecord (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 16edb529cb5a1cf6e2badd19c3ac37f1e7ec69649fb854f98ff0b515c573f874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141084"
---
# <a name="iscardiso7816readrecord-method"></a>Metodo ISCardISO7816::ReadRecord

\[Il **metodo ReadRecord** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo ReadRecord** costruisce un comando APDU [*(Application Protocol Data Unit)*](../secgloss/a-gly.md) che legge il contenuto dei record specificati o la parte iniziale di un record di un file elementare.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReadRecord(
  [in]      BYTE       byRecordId,
  [in]      BYTE       byRefCtrl,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byRecordId* \[ Pollici\]
</dt> <dd>

Numero di record o ID del primo record da leggere (00 indica il record corrente).

</dd> <dt>

*byRefCtrl* \[ Pollici\]
</dt> <dd>

Codifica del controllo di riferimento.



| Valore                                                                                                                                                                                | Significato                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**EF corrente**</dt> </dl>     | Posizione in bit: 00000---<br/> EF attualmente selezionato.<br/>                    |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**ID EF breve**</dt> </dl> | Posizione di bit: xxxxx---<br/> Identificatore EF breve.<br/>                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**Rfu**</dt> </dl>                                                       | Posizione bit: 11111---<br/>                                                      |
| <span id="Record__"></span><span id="record__"></span><span id="RECORD__"></span><dl> <dt>**Registrazione \#**</dt> </dl>            | Posizione di bit: -----1xx<br/> Utilizzo del numero di record in P1.<br/>             |
| <span id="Read_Record"></span><span id="read_record"></span><span id="READ_RECORD"></span><dl> <dt>**Legge record**</dt> </dl> | Posizione di bit: -----100<br/> Leggere il record P1.<br/>                           |
| <span id="Up_to_Last"></span><span id="up_to_last"></span><span id="UP_TO_LAST"></span><dl> <dt>**Fino all'ultimo**</dt> </dl>     | Posizione di bit: -----101<br/> Leggere tutti i record da P1 fino all'ultimo. <br/> |
| <span id="Up_to_P1"></span><span id="up_to_p1"></span><span id="UP_TO_P1"></span><dl> <dt>**Fino a P1**</dt> </dl>             | Posizione di bit: -----110<br/> Leggere tutti i record dall'ultimo fino a P1. <br/> |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**Rfu**</dt> </dl>                                                       | Posizione di bit: -----111<br/>                                                      |
| <span id="Record_ID"></span><span id="record_id"></span><span id="RECORD_ID"></span><dl> <dt>**ID record**</dt> </dl>         | Posizione di bit: -----0xx<br/> Utilizzo del numero di record in P1.<br/>             |
| <span id="First_Occur"></span><span id="first_occur"></span><span id="FIRST_OCCUR"></span><dl> <dt>**Primo evento**</dt> </dl> | Posizione bit: -----000<br/> Legge la prima occorrenza. <br/>                   |
| <span id="Last_Occur"></span><span id="last_occur"></span><span id="LAST_OCCUR"></span><dl> <dt>**Ultimo evento**</dt> </dl>     | Posizione di bit: -----001<br/> Legge l'ultima occorrenza. <br/>                    |
| <span id="Next_Occur"></span><span id="next_occur"></span><span id="NEXT_OCCUR"></span><dl> <dt>**Verifica successiva**</dt> </dl>     | Posizione di bit: -----010<br/> Leggere l'occorrenza successiva. <br/>                    |
| <span id="Previous"></span><span id="previous"></span><span id="PREVIOUS"></span><dl> <dt>**Indietro**</dt> </dl>             | Posizione di bit: -----011<br/> Leggere l'occorrenza precedente. <br/>                |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**Segreto**</dt> </dl>                     | Posizione di bit: ---xxxxx<br/>                                                      |



 

</dd> <dt>

*lBytesToRead* \[ Pollici\]
</dt> <dd>

Numero di byte da leggere da Transparent EF.

Se il campo Le contiene solo zeri, a seconda di b3b2b1 di P2 e entro il limite di 256 per la lunghezza breve o 65536 per la lunghezza estesa, il comando deve leggere completamente il singolo record richiesto o la sequenza richiesta di record.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

In input, puntatore a un [**oggetto interfaccia ISCardCmd**](iscardcmd.md) o **NULL.**

In caso di restituzione, viene riempito con il comando APDU costruito da questa operazione. Se *ppCmd è* stato impostato su **NULL,** un [*smart card*](../secgloss/s-gly.md) [**isCardCmd**](iscardcmd.md) viene creato internamente e restituito tramite il *puntatore ppCmd.*

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

Il comando incapsulato può essere eseguito solo se lo stato di sicurezza del [*smart card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare letto.

Se è attualmente selezionato un altro file elementare al momento dell'emissione di questo comando, è possibile elaborarlo senza identificare il file attualmente selezionato.

Quando il comando contiene un identificatore elementare breve valido, imposta il file come file elementare corrente.

I file elementari senza una struttura di record non possono essere letti. Il comando incapsulato viene interrotto se applicato a un file elementare senza una struttura di record.

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

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

[**AppendRecord**](iscardiso7816-appendrecord.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> <dt>

[**WriteRecord**](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
