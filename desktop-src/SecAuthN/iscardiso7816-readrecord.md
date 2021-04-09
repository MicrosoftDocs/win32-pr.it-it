---
description: Il metodo ReadRecord costruisce un comando APDU (Application Protocol Data Unit) che legge il contenuto dei record specificati o la parte iniziale di un record di un file elementare.
ms.assetid: b00a3242-93bc-4779-8c62-89157fbcb5d1
title: 'Metodo ISCardISO7816:: ReadRecord (scardssp. h)'
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
ms.openlocfilehash: 0cb9697315a6f9dd2436cd7a64d54fa6b44e00f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049980"
---
# <a name="iscardiso7816readrecord-method"></a>Metodo ISCardISO7816:: ReadRecord

\[Il metodo **ReadRecord** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **ReadRecord** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che legge il contenuto dei record specificati o la parte iniziale di un record di un file elementare.

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

*byRecordId* \[ in\]
</dt> <dd>

Numero di record o ID del primo record da leggere (00 indica il record corrente).

</dd> <dt>

*byRefCtrl* \[ in\]
</dt> <dd>

Codifica del controllo di riferimento.



| Valore                                                                                                                                                                                | Significato                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**EF corrente**</dt> </dl>     | Posizione bit: 00000---<br/> Attualmente selezionato EF.<br/>                    |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**ID EF breve**</dt> </dl> | Posizione bit: xxxxx---<br/> Identificatore EF breve.<br/>                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                       | Posizione bit: 11111---<br/>                                                      |
| <span id="Record__"></span><span id="record__"></span><span id="RECORD__"></span><dl> <dt>**Record \#**</dt> </dl>            | Posizione bit:-----1xx<br/> Utilizzo del numero di record in P1.<br/>             |
| <span id="Read_Record"></span><span id="read_record"></span><span id="READ_RECORD"></span><dl> <dt>**Leggi record**</dt> </dl> | Posizione bit:-----100<br/> Leggere il record P1.<br/>                           |
| <span id="Up_to_Last"></span><span id="up_to_last"></span><span id="UP_TO_LAST"></span><dl> <dt>**Fino alla fine**</dt> </dl>     | Posizione bit:-----101<br/> Leggere tutti i record da P1 fino alla fine. <br/> |
| <span id="Up_to_P1"></span><span id="up_to_p1"></span><span id="UP_TO_P1"></span><dl> <dt>**Fino a P1**</dt> </dl>             | Posizione bit:-----110<br/> Leggere tutti i record dall'ultimo fino a P1. <br/> |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                       | Posizione bit:-----111<br/>                                                      |
| <span id="Record_ID"></span><span id="record_id"></span><span id="RECORD_ID"></span><dl> <dt>**ID record**</dt> </dl>         | Posizione bit:-----0xx<br/> Utilizzo del numero di record in P1.<br/>             |
| <span id="First_Occur"></span><span id="first_occur"></span><span id="FIRST_OCCUR"></span><dl> <dt>**Prima occorrenza**</dt> </dl> | Posizione bit:-----000<br/> Lettura prima occorrenza. <br/>                   |
| <span id="Last_Occur"></span><span id="last_occur"></span><span id="LAST_OCCUR"></span><dl> <dt>**Ultima occorrenza**</dt> </dl>     | Posizione bit:-----001<br/> Leggere l'ultima occorrenza. <br/>                    |
| <span id="Next_Occur"></span><span id="next_occur"></span><span id="NEXT_OCCUR"></span><dl> <dt>**Prossima esecuzione**</dt> </dl>     | Posizione bit:-----010<br/> Leggere l'occorrenza successiva. <br/>                    |
| <span id="Previous"></span><span id="previous"></span><span id="PREVIOUS"></span><dl> <dt>**Indietro**</dt> </dl>             | Posizione bit:-----011<br/> Leggere l'occorrenza precedente. <br/>                |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <dt>**Segreto**</dt> </dl>                     | Posizione bit:---xxxxx<br/>                                                      |



 

</dd> <dt>

*lBytesToRead* \[ in\]
</dt> <dd>

Numero di byte da leggere dall'EF trasparente.

Se il campo le contiene solo zeri, a seconda del valore di b3b2b1 P2 e del limite di 256 per la lunghezza breve o 65536 per la lunghezza prolungata, il comando deve leggere completamente il singolo record richiesto o la sequenza di record richiesta.

</dd> <dt>

*ppCmd* \[ in uscita\]
</dt> <dd>

In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.

Al ritorno, viene compilato con il comando APDU creato da questa operazione. Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente tramite il puntatore *ppCmd* .

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

Il comando incapsulato può essere eseguito solo se lo stato di sicurezza della [*Smart Card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare letto.

Se al momento dell'invio di questo comando è attualmente selezionato un altro file elementare, è possibile che venga elaborato senza l'identificazione del file attualmente selezionato.

Quando il comando contiene un identificatore elementare breve valido, imposta il file come file elementare corrente.

Non è possibile leggere i file elementari senza una struttura di record. Il comando incapsulato viene interrotto se applicato a un file elementare senza una struttura di record.

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

[**AppendRecord**](iscardiso7816-appendrecord.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> <dt>

[**WriteRecord**](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
