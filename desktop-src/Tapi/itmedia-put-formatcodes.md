---
description: Il metodo put \_ FormatCodes imposta l'elenco di codici di formato del payload multimediale. La variante contiene un SAFEARRAY di BSTR. Ogni BSTR all'interno di tale matrice è una stringa di codice di formato.
ms.assetid: b76a7fee-0fae-41fb-a8cd-6803458d9182
title: Metodo ITMedia::p ut_FormatCodes (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dac8c2d9e102c6a923a535b8141c546885c583668e32fddb1fc607a8c1179a99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012961"
---
# <a name="itmediaput_formatcodes-method"></a>Metodo ITMedia::p ut \_ FormatCodes

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

Il **metodo put \_ FormatCodes** imposta l'elenco di codici di formato del payload multimediale. La variante contiene un SAFEARRAY di **BSTR.** Ogni **BSTR all'interno** di tale matrice è una stringa di codice di formato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_FormatCodes(
  [in] VARIANT NewVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NewVal* \[ Pollici\]
</dt> <dd>

Elenco di codici di formato di payload multimediale.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                                   | Descrizione                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Il *parametro NewVal* non è valido.<br/>                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente per eseguire l'operazione.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Errore non specificato.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Questo metodo non è ancora implementato.<br/>                  |



 

## <a name="remarks"></a>Commenti

Quando viene fornito un elenco di formati di payload, ciò implica che tutti questi formati possono essere usati nella sessione, ma il primo di questi formati è il formato predefinito per la sessione. Quando il protocollo di trasporto è RTP, i codici di formato sono tipi di payload RTP.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::get \_ FormatCodes**](itmedia-get-formatcodes.md)
</dt> </dl>

 

 




