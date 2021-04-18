---
title: Metodo External. Buy
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. Il metodo Buy avvia l'acquisto di un set di elementi multimediali.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- acquistare il metodo Windows Media Player
- Metodo di acquisto Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo Buy
topic_type:
- apiref
api_name:
- External.buy
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5ffee188372e33ed4ceadf1bb1ee2ea0f986207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328888"
---
# <a name="externalbuy-method"></a>Metodo External. Buy

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Il metodo **buy** avvia l'acquisto di un set di elementi multimediali.

## <a name="syntax"></a>Sintassi


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ViewType* \[ in\]
</dt> <dd>

**Stringa** che specifica il tipo di elemento da acquistare. Il chiamante deve impostare questo parametro su una delle seguenti [costanti del percorso della libreria](library-location-constants.md):

CPListID

CPTrackID

CPAlbumID

</dd> <dt>

*ID* \[ in\]
</dt> <dd>

**Stringa** contenente gli ID, delimitati da punti e virgola, degli elementi da acquistare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. download**](external-download.md)
</dt> <dt>

[**IWMPContentPartner:: Buy**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[**Acquisto di contenuti multimediali**](purchasing-media-content.md)
</dt> </dl>

 

 





