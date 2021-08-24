---
description: Il metodo GetData costruisce un comando APDU (Application Protocol Data Unit) che recupera un singolo oggetto dati primitivo o un set di oggetti dati (contenuti in un oggetto dati costruito), a seconda del tipo di file selezionato.
ms.assetid: d764a765-f451-4bf7-9d06-f5901062dcac
title: Metodo ISCardISO7816::GetData (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1ef783092edb87a29203c83afcf67fb594eb84dcc296621379c9f39a9ccbcc79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672381"
---
# <a name="iscardiso7816getdata-method"></a>Metodo ISCardISO7816::GetData

\[Il **metodo GetData** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo GetData** costruisce un comando APDU [*(Application Protocol Data Unit)*](../secgloss/a-gly.md) che recupera un singolo oggetto dati primitivo o un set di oggetti dati (contenuti in un oggetto dati costruito), a seconda del tipo di file selezionato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetData(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToGet,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byP1* \[ Pollici\]
</dt> <dd>

Parametri.



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

Parametri.



| Valore                                                                                  | Significato                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0000 - 003F</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0040 - 00FF</dt> </dl> | BER-TLV tag (1 byte) in P2<br/>            |
| <dl> <dt>0100 - 01FF</dt> </dl> | Dati dell'applicazione (codifica proprietaria)<br/> |
| <dl> <dt>0200 - 02FF</dt> </dl> | SIMPLE-TLV tag in P2<br/>                  |
| <dl> <dt>0300 - 03FF</dt> </dl> | Rfu<br/>                                   |
| <dl> <dt>0400 - 04FF</dt> </dl> | Tag BER-TLV (2 byte) in P1-P2<br/>        |



 

</dd> <dt>

*lBytesToGet* \[ Pollici\]
</dt> <dd>

Numero di byte previsti nella risposta.

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

Il comando incapsulato può essere eseguito solo se lo stato di sicurezza del [*smart card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare letto. Le condizioni di sicurezza dipendono dai criteri della scheda e possono essere manipolate tramite [**ExternalAuthenticate,**](iscardiso7816-externalauthenticate.md) [**InternalAuthenticate,**](iscardiso7816-internalauthenticate.md) [**ISCardAuth**](iscardauth.md)e così via.

Per selezionare un file, chiamare [**SelectFile**](iscardiso7816-selectfile.md).

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

[**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[**InternalAuthenticate**](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[**ISCardAuth**](iscardauth.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**PutData**](iscardiso7816-putdata.md)
</dt> <dt>

[**SelectFile**](iscardiso7816-selectfile.md)
</dt> </dl>

 

 
