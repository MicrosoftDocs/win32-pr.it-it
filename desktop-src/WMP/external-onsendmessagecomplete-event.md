---
title: External.OnSendMessageComplete Event
description: Nota Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. | External.OnSendMessageComplete Event
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- Evento External.OnSendMessageComplete Windows Media Player
topic_type:
- apiref
api_name:
- External.OnSendMessageComplete Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1dede59d2c52f20050a490e6ded1389e63884e598868e9736195280e3269a72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648731"
---
# <a name="externalonsendmessagecomplete-event"></a>External.OnSendMessageComplete Event

> [!Note]  
> In questo argomento vengono descritte le funzionalità progettate per l'utilizzo da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di un negozio online non è supportato.

 

**L'evento OnSendMessageComplete si** verifica quando lo store online ha terminato l'elaborazione di un messaggio. Lo script nella pagina di individuazione ha inviato in precedenza il messaggio [chiamando External.sendMessage](external-sendmessage.md).

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a>Valori possibili

Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player quando si verifica l'evento.

## <a name="parameters"></a>Parametri

La funzione che gestisce questo evento ha i parametri seguenti.

<dl> <dt>

<span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Msg*
</dt> <dd>

Stessa stringa passata nel parametro **Msg** di **sendMessage**.

</dd> <dt>

<span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*
</dt> <dd>

Stessa stringa passata nel parametro **Param** di **sendMessage**.

</dd> <dt>

<span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Risultato*
</dt> <dd>

**Stringa** contenente il risultato della gestione dei messaggi. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il **metodo sendMessage** chiama [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), che restituisce in modo asincrono. Ciò significa che viene restituito prima che lo store online finisca di elaborare il messaggio. Quando lo store online termina l'elaborazione del messaggio, chiama [IWMPContentPartnerCallback::SendMessageComplete,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)che a sua volta chiama il gestore eventi **OnSendMessageComplete dello** script.

Quando lo store online chiama **IWMPContentPartnerCallback::SendMessageComplete,** fornisce un codice risultato nel *parametro bstrResult.* Windows Media Player non interpreta il codice del risultato. Al contrario, Windows Media Player passa il codice del risultato al gestore dell'evento **OnSendMessageComplete** nel *parametro Result.*

Nessuno dei parametri (*Msg*, *Param*, *Result*) del gestore dell'evento **OnSendMessageComplete** viene interpretato Windows Media Player. I parametri hanno un significato solo per lo store online.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.sendMessage**](external-sendmessage.md)
</dt> <dt>

[**IWMPContentPartner::SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





