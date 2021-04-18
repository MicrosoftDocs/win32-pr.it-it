---
title: Evento External. OnSendMessageComplete
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | Evento External. OnSendMessageComplete
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- Media Player di Windows dell'evento External. OnSendMessageComplete
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
ms.openlocfilehash: 05d4de69a753811537f60ae8a3244cfaf012f60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324558"
---
# <a name="externalonsendmessagecomplete-event"></a>Evento External. OnSendMessageComplete

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

L'evento **OnSendMessageComplete** si verifica al termine dell'elaborazione di un messaggio da parte del negozio online. Script nella pagina di individuazione ha inviato in precedenza il messaggio chiamando [External. SendMessage](external-sendmessage.md).

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a>Valori possibili

Si tratta di una proprietà di sola scrittura che specifica il nome della funzione nello script che Windows Media Player chiama quando si verifica l'evento.

## <a name="parameters"></a>Parametri

La funzione che gestisce questo evento presenta i parametri seguenti.

<dl> <dt>

<span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Messaggio*
</dt> <dd>

La stessa stringa passata nel parametro **msg** di **SendMessage**.

</dd> <dt>

<span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*
</dt> <dd>

La stessa stringa passata nel parametro **param** di **SendMessage**.

</dd> <dt>

<span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Risultato*
</dt> <dd>

**Stringa** che contiene il risultato della gestione dei messaggi. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il metodo **SendMessage** chiama [IWMPContentPartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), che restituisce in modo asincrono. Ovvero, viene restituito prima del completamento dell'elaborazione del messaggio da parte del negozio online. Al termine dell'elaborazione del messaggio da parte del negozio online, viene chiamato [IWMPContentPartnerCallback:: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), che a sua volta chiama il gestore dell'evento **OnSendMessageComplete** dello script.

Quando l'archivio online chiama **IWMPContentPartnerCallback:: SendMessageComplete**, fornisce un codice risultato nel parametro *bstrResult* . Windows Media Player non interpreta il codice risultante. Al contrario, Windows Media Player passa il codice risultato insieme al gestore eventi **OnSendMessageComplete** nel parametro *result* .

Nessuno dei parametri (*msg*, *param*, *result*) del gestore dell'evento **OnSendMessageComplete** viene interpretato da Windows Media Player. I parametri hanno un significato solo per il negozio online.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**SendMessage esterno**](external-sendmessage.md)
</dt> <dt>

[**IWMPContentPartner:: SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





