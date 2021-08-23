---
title: Metodo External.buy
description: Nota Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato. Il metodo buy avvia l'acquisto di un set di elementi multimediali.
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- Metodo buy Windows Media Player
- Metodo buy Windows Media Player , classe esterna
- Classe esterna Windows Media Player , metodo buy
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
ms.openlocfilehash: 16acc578d18c2a93118e1d7aa55b0fdcbe474a8698a0982ef8c2df7edb3802ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649521"
---
# <a name="externalbuy-method"></a>Metodo External.buy

> [!Note]  
> In questo argomento vengono descritte le funzionalità progettate per l'utilizzo da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato.

 

Il **metodo buy** avvia l'acquisto di un set di elementi multimediali.

## <a name="syntax"></a>Sintassi


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ViewType* \[ Pollici\]
</dt> <dd>

**Stringa** che specifica il tipo di elemento da acquistare. Il chiamante deve impostare questo parametro su una delle costanti di [posizione della libreria seguenti:](library-location-constants.md)

CPListID

CPTrackID

CPAlbumID

</dd> <dt>

*Id visualizzazione* \[ Pollici\]
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

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.download**](external-download.md)
</dt> <dt>

[**IWMPContentPartner::Buy**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[**Acquisto di contenuti multimediali**](purchasing-media-content.md)
</dt> </dl>

 

 





