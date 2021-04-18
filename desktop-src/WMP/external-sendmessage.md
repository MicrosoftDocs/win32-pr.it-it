---
title: Metodo External. sendMessage
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo sendMessage Invia un messaggio al plug-in del negozio online.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- Metodo sendMessage Media Player Windows
- Metodo sendMessage Media Player Windows, classe esterna
- Classe esterna Media Player Windows, metodo sendMessage
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
ms.openlocfilehash: 4648f3cf433a2828d3c97604ebf9ee6e7223b7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328410"
---
# <a name="externalsendmessage-method"></a>Metodo External. sendMessage

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Il metodo **SendMessage** Invia un messaggio al plug-in del negozio online.

## <a name="syntax"></a>Sintassi


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Messaggio* \[ in\]
</dt> <dd>

**Stringa** che contiene il messaggio.

</dd> <dt>

*Param* \[ in\]
</dt> <dd>

**Stringa** contenente i parametri associati al messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il messaggio viene inviato in modo asincrono. Questo metodo viene restituito immediatamente anziché attendere l'elaborazione del messaggio. Al termine dell'elaborazione del messaggio, il plug-in chiama il metodo [IWMPContentPartnerCallback:: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) , che a sua volta chiama il gestore dell'evento [OnSendMessageComplete](external-onsendmessagecomplete-event.md) dello script.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. OnSendMessageComplete**](external-onsendmessagecomplete-event.md)
</dt> <dt>

[**IWMPContentPartner:: SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





