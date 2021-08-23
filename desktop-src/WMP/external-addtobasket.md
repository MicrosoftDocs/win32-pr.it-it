---
title: Metodo External.addToBasket
description: Nota Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. | Metodo External.addToBasket
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- Metodo addToBasket Windows Media Player
- Metodo addToBasket Windows Media Player , classe external
- Classe esterna Windows Media Player, metodo addToBasket
topic_type:
- apiref
api_name:
- External.addToBasket
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f51cfc3df641b02a5aa3a0869e810f318357dd70ba67acb3ec2310f8a5a355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650011"
---
# <a name="externaladdtobasket-method"></a>Metodo External.addToBasket

> [!Note]  
> In questo argomento vengono descritte le funzionalità progettate per l'utilizzo da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato.

 

Il **metodo addToBasket** aggiunge elementi multimediali al riquadro elenco (detto anche carrello) in Windows Media Player.

## <a name="syntax"></a>Sintassi


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ViewType* \[ Pollici\]
</dt> <dd>

**Stringa** che specifica il tipo di elemento da aggiungere al riquadro elenco. Il chiamante deve impostare questo parametro su una delle costanti di [posizione della libreria seguenti:](library-location-constants.md)

CPListID

CPTrackID

CPAlbumID

CPArtist

CPGenreID

CPAlbumSubGenreID

CPRadioID

</dd> <dt>

*Id visualizzazione* \[ Pollici\]
</dt> <dd>

**Stringa** contenente gli ID, delimitati da punti e virgola, degli elementi da aggiungere al riquadro elenco.

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

[**ExternalObject per store online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.basketTitle**](external-baskettitle.md)
</dt> </dl>

 

 





