---
description: Usato dal client di completamento automatico per notificare all'applicazione il testo che un utente ha inchiostrato nel pannello di input.
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: 'Metodo ITipAutocompleteProvider:: UpdatePendingText (TipAutoComplete. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITipAutocompleteProvider.UpdatePendingText
api_type:
- COM
api_location:
- tiptsf.dll
ms.openlocfilehash: 5c66e625639aa7088b1b3934a2f984d0f4097536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058332"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a>Metodo ITipAutocompleteProvider:: UpdatePendingText

Usato dal client di completamento automatico per notificare all'applicazione il testo che un utente ha inchiostrato nel pannello di input.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrPendingText* \[ in\]
</dt> <dd>

Testo di origine da usare per generare l'elenco di completamento automatico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Esito positivo.<br/>                       |
| <dl> <dt>**E \_ non riescono**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo testo non conterrà il testo già inserito nel campo con lo stato attivo. Il provider di completamento automatico è responsabile di prendere in considerazione il testo del campo corrente e la selezione per generare l'elenco di completamento automatico. Quando *bstrPendingText* è **null**, l'elenco di completamento automatico viene generato con il testo corrente a sinistra della selezione nel campo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                                   |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                       |
| Intestazione<br/>                   | <dl> <dt>TipAutoComplete. h (richiede anche PenInputPanel \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITipAutocompleteProvider**](itipautocompleteprovider.md)
</dt> <dt>

[Riferimento al pannello input di testo](text-input-panel-reference.md)
</dt> </dl>

 

 




