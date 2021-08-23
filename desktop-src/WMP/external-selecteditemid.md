---
title: External.selectedItemID
description: Nota Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. | External.selectedItemID
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- External.selectedItemID Windows Media Player
topic_type:
- apiref
api_name:
- External.selectedItemID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea4b93656adc3fab25ab96e41fe417bde158035c5c11a0af9be84c5d555b153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648431"
---
# <a name="externalselecteditemid"></a>External.selectedItemID

> [!Note]  
> In questo argomento vengono descritte le funzionalità progettate per l'utilizzo da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato.

 

La **proprietà selectedItemID** recupera l'identificatore dell'elemento multimediale attualmente selezionato in Windows Media Player.

## <a name="syntax"></a>Sintassi

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di sola **lettura.**

## <a name="remarks"></a>Commenti

Questa proprietà viene usata in combinazione con [la proprietà External.selectedItemType.](external-selecteditemtype.md) Ad esempio, se **selectedItemType** è uguale a CPTrackID, **selectedItemID** è l'ID della traccia selezionata. Per altre informazioni su come Windows Media Player caratterizza le visualizzazioni del contenuto dello store online, vedere [Posizione e elemento selezionato.](location-and-selected-item.md)

Alcune visualizzazioni Windows Media Player hanno un particolare elemento multimediale selezionato. Si supponga, ad esempio, che la visualizzazione corrente rappresenti un album. Un album è un contenitore di tracce, quindi **selectedItemType** è uguale a CPTrackID e **selectedItemID** è l'ID della traccia selezionata. Le altre visualizzazioni non dispongono di un elemento multimediale selezionato. Ad esempio, se l'utente fa clic sul nodo radice del negozio online nel controllo di visualizzazione albero, Windows Media Player visualizza una pagina di individuazione fornita dallo store online. Il lettore non visualizza alcun contenitore di elementi multimediali nell'interfaccia utente del lettore. In tal caso, **selectedItemType** è uguale a UnknownLocation e **selectedItemID** è uguale alla stringa vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.selectedItemType**](external-selecteditemtype.md)
</dt> <dt>

[**Posizione ed elemento selezionato**](location-and-selected-item.md)
</dt> </dl>

 

 





