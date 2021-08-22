---
description: Il metodo AppendRecord costruisce un comando APDU (Application Protocol Data Unit) che aggiunge un record alla fine di un file elementare con struttura lineare (EF) o scrive il record numero 1 in un file elementare con struttura ciclica.
ms.assetid: 4dd88661-41c4-4238-88c9-279b39afb206
title: Metodo ISCardISO7816::AppendRecord (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.AppendRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: de2b6ac4bfded1612713272111f3ef21f21cf4b7b8ac9cedae769531fee26c05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118923062"
---
# <a name="iscardiso7816appendrecord-method"></a>Metodo ISCardISO7816::AppendRecord

\[Il **metodo AppendRecord** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il metodo **AppendRecord** costruisce un comando APDU [*(Application Protocol Data Unit)*](../secgloss/a-gly.md) che aggiunge un record alla fine di un file elementare con struttura lineare (EF) o scrive il record numero 1 in un file elementare con struttura ciclica.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AppendRecord(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byRefCtrl* \[ Pollici\]
</dt> <dd>

Identifica il file elementare da aggiungere.



| Valore                                                                                                                                                                                | Significato                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <dt>**EF corrente**</dt> </dl>     | Posizione bit: 00000000<br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <dt>**ID EF breve**</dt> </dl> | Posizione bit: xxxxx000<br/> |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <dt>**Riservato**</dt> </dl>             | Posizione di bit: xxxxxxxx<br/> |



 

</dd> <dt>

*pData* \[ Pollici\]
</dt> <dd>

Puntatore ai dati da aggiungere al file.



| Valore                                                                                                                                                | Significato                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="Tn"></span><span id="tn"></span><span id="TN"></span><dl> <dt>**Tn**</dt> </dl>     | 1 byte<br/>       |
| <span id="Ln_"></span><span id="ln_"></span><span id="LN_"></span><dl> <dt>**Ln**</dt> </dl> | 1 o 3 byte<br/> |
| <span id="data"></span><span id="DATA"></span><dl> <dt>**Dati**</dt> </dl>                    | Byte Ln<br/>     |



 

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Nell'input, un puntatore a un [**oggetto interfaccia ISCardCmd**](iscardcmd.md) o **NULL.**

Al ritorno, viene riempito con il comando APDU costruito da questa operazione. Se *ppCmd è* stato impostato su **NULL,** [**smart card'oggetto ISCardCmd**](iscardcmd.md) viene creato internamente e restituito usando il *puntatore ppCmd.* [](../secgloss/s-gly.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Il comando incapsulato può essere eseguito solo se lo stato di sicurezza del [*smart card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare letto.

Se al momento dell'esecuzione di questo comando viene selezionato un altro file elementare, è possibile che venga elaborato senza l'identificazione del file attualmente selezionato.

I file elementari senza una struttura di record non possono essere letti. Il comando incapsulato viene interrotto se applicato a un file elementare senza una struttura di record.

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816.**](iscardiso7816.md)

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore smart card se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadRecord**](iscardiso7816-readrecord.md)
</dt> <dt>

[**UpdateRecord**](iscardiso7816-updaterecord.md)
</dt> <dt>

[**WriteRecord**](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
