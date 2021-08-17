---
description: Usato dal client di completamento automatico per notificare all'applicazione il testo che un utente ha inserito nel pannello di input penna.
ms.assetid: 68413836-321a-4e75-8538-c5a8fc577c0f
title: Metodo ITipAutocompleteProvider::UpdatePendingText (TipAutoComplete.h)
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
ms.openlocfilehash: 99fc67b5ba6495e2bdfb8a54de2412ca01cbdd37475d08d20d227b203f2da1bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716431"
---
# <a name="itipautocompleteproviderupdatependingtext-method"></a>Metodo ITipAutocompleteProvider::UpdatePendingText

Usato dal client di completamento automatico per notificare all'applicazione il testo che un utente ha inserito nel pannello di input penna.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UpdatePendingText(
  [in] BSTR bstrPendingText
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bstrPendingText* \[ Pollici\]
</dt> <dd>

Testo di origine da usare per generare l'elenco di completamento automatico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                            | Descrizione                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Operazione completata.<br/>                       |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Si è verificato un errore non specificato.<br/> |



 

## <a name="remarks"></a>Commenti

Questo testo non conterrà il testo già inserito nel campo con lo stato attivo. Il provider di completamento automatico è responsabile di prendere in considerazione il testo del campo corrente e la selezione per generare l'elenco di completamento automatico. Quando *bstrPendingText* è **NULL,** l'elenco di completamento automatico viene generato con il testo corrente a sinistra della selezione nel campo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                                   |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                                       |
| Intestazione<br/>                   | <dl> <dt>TipAutoComplete.h (richiede anche Peninputpanel \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Tiptsf.dll</dt> </dl>                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia ITipAutocompleteProvider**](itipautocompleteprovider.md)
</dt> <dt>

[Informazioni di riferimento sul pannello Input di testo](text-input-panel-reference.md)
</dt> </dl>

 

 




