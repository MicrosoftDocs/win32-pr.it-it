---
description: Il metodo GetResponse costruisce un comando APDU (Application Protocol Data Unit) che trasmette i comandi APDU (o parte di un comando APDU) che altrimenti non potevano essere trasmessi dai protocolli disponibili.
ms.assetid: 1aa83d38-d46d-4d3b-8f57-0256e5875e35
title: Metodo ISCardISO7816::GetResponse (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetResponse
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 21646b7de844509b28bb0ea437fa76cd9fa835932333677f919872daecb3ce60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481149"
---
# <a name="iscardiso7816getresponse-method"></a>Metodo ISCardISO7816::GetResponse

\[Il **metodo GetResponse** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo GetResponse** costruisce un comando APDU [*(Application Protocol Data Unit)*](../secgloss/a-gly.md) che trasmette i comandi APDU (o parte di un comando APDU) che altrimenti non potevano essere trasmessi dai protocolli disponibili.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetResponse(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lDataLength,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byP1* \[ Pollici\]
</dt> <dd>

Per iso 7816-4, P1 deve essere zero (RFU).

</dd> <dt>

*byP2* \[ Pollici\]
</dt> <dd>

Per iso 7816-4, P2 deve essere zero (RFU).

</dd> <dt>

*lDataLength* \[ Pollici\]
</dt> <dd>

Lunghezza dei dati trasmessi.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

In input, puntatore a un [**oggetto interfaccia ISCardCmd**](iscardcmd.md) o **NULL.**

In caso di restituzione, viene riempito con il comando APDU costruito da questa operazione. Se *ppCmd è* stato impostato su **NULL,** un [*smart card*](../secgloss/s-gly.md) [**oggetto ISCardCmd**](iscardcmd.md) viene creato internamente e restituito tramite il *puntatore ppCmd.*

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

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
