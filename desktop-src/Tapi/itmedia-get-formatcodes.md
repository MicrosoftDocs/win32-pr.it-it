---
description: Il \_ metodo Get codiciformato Ottiene l'elenco dei codici di formato del payload multimediale. Il VARIANT restituisce un SAFEARRAY di BSTR. Ogni BSTR all'interno di tale matrice è una stringa di codice del formato.
ms.assetid: 8663d7e8-d46f-44d1-93db-9b5142bb28dd
title: 'Metodo ITMedia:: get_FormatCodes (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9e28a0323ac001c948a3b19b8dae2cfe9daf5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330367"
---
# <a name="itmediaget_formatcodes-method"></a>Metodo ITMedia:: Get \_ codiciformato

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **get \_ codiciformato** Ottiene l'elenco dei codici di formato del payload multimediale. Il VARIANT restituisce un SAFEARRAY di **BSTR** s. Ogni **BSTR** all'interno di tale matrice è una stringa di codice del formato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_FormatCodes(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pval* \[ out\]
</dt> <dd>

Matrice di codici di formato del payload multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Il parametro *pval* non è un puntatore valido.<br/>         |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | La memoria disponibile non è sufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ non riescono**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

Quando viene fornito un elenco di formati di payload, questo implica che tutti questi formati possono essere utilizzati nella sessione, ma il primo di questi formati è il formato predefinito per la sessione. Quando il protocollo di trasporto è RTP, i codici di formato sono tipi di payload RTP.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::p UT \_ codiciformato**](itmedia-put-formatcodes.md)
</dt> </dl>

 

 




