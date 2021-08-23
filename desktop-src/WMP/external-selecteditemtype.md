---
title: External.selectedItemType
description: Nota Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. | External.selectedItemType
ms.assetid: f566e41e-127b-4596-99e6-bb07fc97249e
keywords:
- External.selectedItemType Windows Media Player
topic_type:
- apiref
api_name:
- External.selectedItemType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb58b13f1486bb30a79cd20e2f43f715df694f661c7b56e5eadd29f0c5c06c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648417"
---
# <a name="externalselecteditemtype"></a>External.selectedItemType

> [!Note]  
> In questo argomento vengono descritte le funzionalità progettate per l'utilizzo da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato.

 

La **proprietà selectedItemType** recupera il tipo dell'elemento multimediale attualmente selezionato in Windows Media Player.

## <a name="syntax"></a>Sintassi

window.external.selectedItemType()

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una stringa di sola **lettura** che contiene una delle costanti [di percorso della libreria](library-location-constants.md).

## <a name="remarks"></a>Commenti

Questa proprietà viene usata in combinazione con **la proprietà External.selectedItemID.** Ad esempio, se **selectedItemType** è uguale a CPTrackID, **selectedItemID** è l'ID della traccia selezionata. Per altre informazioni su come Windows Media Player le visualizzazioni del contenuto dello store online, vedere [Posizione e elemento selezionato.](location-and-selected-item.md)

Alcune visualizzazioni Windows Media Player hanno un particolare elemento multimediale selezionato. Si supponga, ad esempio, che la visualizzazione corrente rappresenti un album. Un album è un contenitore di tracce, quindi **selectedItemType** è uguale a CPTrackID e **selectedItemID** è l'ID della traccia selezionata. Le altre visualizzazioni non dispongono di un elemento multimediale selezionato. Ad esempio, se l'utente fa clic sul nodo radice del negozio online nel controllo visualizzazione albero, Windows Media Player visualizza una pagina di individuazione fornita dal negozio online. Il lettore non visualizza alcun contenitore di elementi multimediali nell'interfaccia utente del lettore. In tal caso, **selectedItemType** è uguale a UnknownLocation e **selectedItemID** è uguale alla stringa vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.selectedItemID**](external-selecteditemid.md)
</dt> <dt>

[**Posizione ed elemento selezionato**](location-and-selected-item.md)
</dt> </dl>

 

 





