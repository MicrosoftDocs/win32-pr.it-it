---
description: Il \_ metodo Put codiciformato imposta l'elenco dei codici di formato del payload multimediale. La variante contiene un SAFEARRAY di BSTR. Ogni BSTR all'interno di tale matrice è una stringa di codice del formato.
ms.assetid: b76a7fee-0fae-41fb-a8cd-6803458d9182
title: 'ITMedia: metodo:p ut_FormatCodes (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9131f946635c2bb066e704f1d6245c1c30d1372
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323939"
---
# <a name="itmediaput_formatcodes-method"></a>ITMedia::p UT \_ codiciformato metodo

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Il metodo **put \_ codiciformato** imposta l'elenco dei codici di formato del payload multimediale. La variante contiene un elemento SAFEARRAY di **BSTR**. Ogni **BSTR** all'interno di tale matrice è una stringa di codice del formato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_FormatCodes(
  [in] VARIANT NewVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewVal* \[ in\]
</dt> <dd>

Elenco dei codici di formato del payload multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il parametro *NewVal* non è valido.<br/>                 |
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

[**ITMedia:: Get \_ codiciformato**](itmedia-get-formatcodes.md)
</dt> </dl>

 

 




