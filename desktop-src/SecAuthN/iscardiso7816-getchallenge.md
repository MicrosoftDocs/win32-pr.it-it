---
description: Il metodo GetChallenge costruisce un comando APDU (Application Protocol Data Unit) che emettere una richiesta di verifica (ad esempio, un numero casuale) da usare in una procedura correlata alla sicurezza.
ms.assetid: 61f6db1c-b83a-4c1f-8ace-0222a12560ff
title: Metodo ISCardISO7816::GetChallenge (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetChallenge
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: aa2c8b6ede97c9fede5984645fd298877da22153f9f0bf3aaf8789281b11889c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481118"
---
# <a name="iscardiso7816getchallenge-method"></a>Metodo ISCardISO7816::GetChallenge

\[Il **metodo GetChallenge** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo GetChallenge costruisce** un comando APDU [*(Application Protocol Data*](../secgloss/a-gly.md) Unit) che emettere una richiesta di verifica (ad esempio, un numero casuale) da usare in una procedura correlata alla sicurezza.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetChallenge(
  [in]      LONG       lBytesExpected,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lBytesExpected* \[ Pollici\]
</dt> <dd>

Lunghezza massima della risposta prevista.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Nell'input, un puntatore a un [**oggetto interfaccia ISCardCmd**](iscardcmd.md) o **NULL.**

Al ritorno, viene riempito con il comando APDU costruito da questa operazione. Se *ppCmd è* stato impostato su **NULL,** [**smart card'oggetto ISCardCmd**](iscardcmd.md) viene creato internamente e restituito tramite il *puntatore ppCmd.* [](../secgloss/s-gly.md)

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

La sfida è valida almeno per il comando successivo.

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

[**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[**InternalAuthenticate**](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
