---
title: Metodo External.sendMessage
description: Nota Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di un negozio online non è supportato. Il metodo sendMessage invia un messaggio al plug-in dello store online.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- Metodo sendMessage Windows Media Player
- Metodo sendMessage Windows Media Player , classe External
- Classe esterna Windows Media Player, metodo sendMessage
topic_type:
- apiref
api_name:
- External.sendMessage
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4985bae2f9170bdb0db1d6cdb995f2c14fe813bcb061485c179bc058539e84c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648361"
---
# <a name="externalsendmessage-method"></a>Metodo External.sendMessage

> [!Note]  
> In questo argomento vengono descritte le funzionalità progettate per l'utilizzo da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di un negozio online non è supportato.

 

Il **metodo sendMessage** invia un messaggio al plug-in dello store online.

## <a name="syntax"></a>Sintassi


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Msg* \[ Pollici\]
</dt> <dd>

**Stringa** contenente il messaggio.

</dd> <dt>

*Parametro* \[ Pollici\]
</dt> <dd>

**Stringa** contenente i parametri associati al messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il messaggio viene inviato in modo asincrono. Ciò significa che questo metodo restituisce immediatamente anziché attendere l'elaborazione del messaggio. Al termine dell'elaborazione del messaggio, il plug-in chiama il metodo [IWMPContentPartnerCallback::SendMessageComplete,](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) che a sua volta chiama il gestore eventi [OnSendMessageComplete](external-onsendmessagecomplete-event.md) dello script.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.OnSendMessageComplete**](external-onsendmessagecomplete-event.md)
</dt> <dt>

[**IWMPContentPartner::SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





