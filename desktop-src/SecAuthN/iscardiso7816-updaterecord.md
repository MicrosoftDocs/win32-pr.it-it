---
description: Il metodo UpdateRecord costruisce un comando APDU (Application Protocol Data Unit) che aggiorna un record specifico con i bit specificati nel comando APDU.
ms.assetid: 66039afd-5d73-41b3-b87b-b5d598c6f3db
title: 'Metodo ISCardISO7816:: UpdateRecord (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bf810594e623d58944f58d3b7671664b3be175f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231716"
---
# <a name="iscardiso7816updaterecord-method"></a>Metodo ISCardISO7816:: UpdateRecord

\[Il metodo **UpdateRecord** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **UpdateRecord** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che aggiorna un record specifico con i bit specificati nel comando APDU.

> [!Note]  
> Quando si usa l'indirizzamento dei record corrente, il comando imposta il puntatore del record sul record aggiornato correttamente.

 

## <a name="syntax"></a>Sintassi


```C++
HRESULT UpdateRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byRecordId* \[ in\]
</dt> <dd>

Valore P1:

P1 = 00 indica il record corrente

P1! = "00" è il numero del record specificato

</dd> <dt>

*byRefCtrl* \[ in\]
</dt> <dd>

Codifica del controllo di riferimento P2:



| Valore                                                                                                                                                                                                | Significato                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**EF corrente**</dt> </dl>                     | Posizione bit: 00000---<br/> Attualmente selezionato EF.<br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**ID EF breve**</dt> </dl>                 | Posizione bit: xxxxx---<br/> Identificatore EF breve.<br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <dt>**Primo record**</dt> </dl>             | Posizione bit:-----000<br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <dt>**Ultimo record**</dt> </dl>                 | Posizione bit:-----001<br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <dt>**Record successivo**</dt> </dl>                 | Posizione bit:-----010<br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <dt>**Record precedente**</dt> </dl> | Posizione bit:-----011<br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <dt>**Record \# in P1**</dt> </dl>    | Posizione bit:-----100<br/>                                   |



 

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Puntatore al record da aggiornare.

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

Il comando incapsulato può essere eseguito solo se lo stato di sicurezza della [*Smart Card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare elaborato.

Quando il comando contiene un identificatore elementare breve valido, imposta il file come file elementare corrente. Se al momento dell'invio di questo comando è attualmente selezionato un altro file elementare, questo comando può essere elaborato senza l'identificazione del file attualmente selezionato.

Se il comando costruito si applica a un file elementare fisso o con struttura ciclica, verrà interrotto se la lunghezza del record è diversa dalla lunghezza del record esistente.

Se il comando si applica a un file elementare strutturato con variabile lineare, può essere eseguito quando la lunghezza del record è diversa dalla lunghezza del record esistente.

L'opzione "Previous" del comando (P2 = xxxxx011), applicata a un file ciclico, ha lo stesso comportamento di un comando costruito da [**AppendRecord**](iscardiso7816-appendrecord.md).

Non è possibile leggere i file elementari senza una struttura di record. Il comando costruito viene interrotto se applicato a un file elementare senza struttura di record.

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

[**ReadRecord**](iscardiso7816-readrecord.md)
</dt> <dt>

[**WriteRecord**](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
