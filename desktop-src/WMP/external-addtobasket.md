---
title: External. addToBasket, metodo
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. addToBasket, metodo
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- Metodo addToBasket Windows Media Player
- Metodo addToBasket Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo addToBasket
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
ms.openlocfilehash: d2e2fab549dec9e24b0c5bbe61f5511e375c4c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329932"
---
# <a name="externaladdtobasket-method"></a>External. addToBasket, metodo

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

Il metodo **addToBasket** aggiunge elementi multimediali al riquadro elenco (detto anche basket) in Windows Media Player.

## <a name="syntax"></a>Sintassi


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ViewType* \[ in\]
</dt> <dd>

**Stringa** che specifica il tipo di elemento da aggiungere al riquadro elenco. Il chiamante deve impostare questo parametro su una delle seguenti [costanti del percorso della libreria](library-location-constants.md):

CPListID

CPTrackID

CPAlbumID

CPArtist

CPGenreID

CPAlbumSubGenreID

CPRadioID

</dd> <dt>

*ID* \[ in\]
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

[**ExternalObject per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. basketTitle**](external-baskettitle.md)
</dt> </dl>

 

 





