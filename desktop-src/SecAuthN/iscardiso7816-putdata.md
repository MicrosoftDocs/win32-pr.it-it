---
description: Il metodo PutData costruisce un comando APDU (Application Protocol Data Unit) che archivia un singolo oggetto dati primitivo o il set di oggetti dati contenuti in un oggetto dati costruito, a seconda del file selezionato.
ms.assetid: 6bad45fb-b202-4eb0-b2f4-fe0a6af64330
title: Metodo ISCardISO7816::P utData (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.PutData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 66698db3c15223071167441fc37437bfa299baa100c58943a41cb4d774a8e17c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141114"
---
# <a name="iscardiso7816putdata-method"></a>Metodo ISCardISO7816::P utData

\[Il **metodo PutData** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo PutData** costruisce un comando APDU [*(Application Protocol Data Unit)*](../secgloss/a-gly.md) che archivia un singolo oggetto dati primitivo o il set di oggetti dati contenuti in un oggetto dati costruito, a seconda del file selezionato.

La modalità di archiviazione degli oggetti (scrittura una sola volta e/o aggiornamento e/o aggiunta) dipende dalla definizione o dalla natura degli oggetti dati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PutData(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byP1* \[ Pollici\]
</dt> <dd>

Codifica di P1-P2.



| Valore                                                                                  | Significato                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000 - 003F</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0040 - 00FF</dt> </dl> | BER-TLV tag (1 byte) in P2<br/>            |
| <dl> <dt>0100 - 01FF</dt> </dl> | Dati dell'applicazione (codifica proprietaria)<br/> |
| <dl> <dt>0200 - 02FF</dt> </dl> | SIMPLE-TLV tag in P2<br/>                  |
| <dl> <dt>0300 - 03FF</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | Tag BER-TLV (2 byte) in P1-P2<br/>        |



 

</dd> <dt>

*byP2* \[ Pollici\]
</dt> <dd>

Codifica di P1-P2.



| Valore                                                                                  | Significato                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000 - 003F</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0040 - 00FF</dt> </dl> | BER-TLV tag (1 byte) in P2<br/>            |
| <dl> <dt>0100 - 01FF</dt> </dl> | Dati dell'applicazione (codifica proprietaria)<br/> |
| <dl> <dt>0200 - 02FF</dt> </dl> | SIMPLE-TLV tag in P2<br/>                  |
| <dl> <dt>0300 - 03FF</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | Tag BER-TLV (2 byte) in P1-P2<br/>        |



 

</dd> <dt>

*pData* \[ Pollici\]
</dt> <dd>

Puntatore a un buffer di byte che contiene i parametri e i dati da scrivere.

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

Il comando può essere eseguito solo se lo stato di sicurezza soddisfa le condizioni di sicurezza definite dall'applicazione all'interno del [*contesto*](../secgloss/c-gly.md) per la funzione.

<dl> <dt>

<span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Archiviare i dati dell'applicazione
</dt> <dd>

Quando il valore di P1-P2 è compreso nell'intervallo da 0100 a 01FF, il valore di P1-P2 deve essere un identificatore riservato per i test interni delle schede e per i servizi proprietari significativi all'interno di un determinato contesto dell'applicazione.

</dd> <dt>

<span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Archiviare oggetti dati
</dt> <dd>

Quando il valore P1-P2 è compreso nell'intervallo da 0040 a 00FF, il valore di P2 deve essere un tag BER-TLV su un singolo byte. Il valore 00FF è riservato per indicare che il campo dati contiene oggetti dati BER-TLV.

Quando il valore di P1-P2 è compreso nell'intervallo da 0200 a 02FF, il valore di P2 deve essere un tag SIMPLE-TLV. Il valore 0200 è RFU. Il valore 02FF è riservato per indicare che il campo dati contiene oggetti dati SIMPLE-TLV.

Quando il valore di P1-P2 è compreso nell'intervallo da 4000 a FFFF, il valore di P1-P2 deve essere un tag BER-TLV su due byte. I valori da 4000 a FFFF sono RFU.

Quando viene fornito un oggetto dati primitivo, il campo dati del messaggio di comando conterrà il valore dell'oggetto dati primitivo corrispondente.

Quando viene fornito un oggetto dati costruito, il campo dati del messaggio di comando deve contenere il valore dell'oggetto dati costruito, ovvero gli oggetti dati, inclusi tag, lunghezza e valore.

</dd> </dl>

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

[**GetData**](iscardiso7816-getdata.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
