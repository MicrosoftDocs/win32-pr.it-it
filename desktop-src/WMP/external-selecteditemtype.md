---
title: External. selectedItemType
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. selectedItemType
ms.assetid: f566e41e-127b-4596-99e6-bb07fc97249e
keywords:
- Media Player di Windows External. selectedItemType
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
ms.openlocfilehash: 9755f66dd00947f295bdd40ea6ab79e69d655d49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324544"
---
# <a name="externalselecteditemtype"></a>External. selectedItemType

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

La proprietà **selectedItemType** Recupera il tipo dell'elemento multimediale attualmente selezionato in Windows Media Player.

## <a name="syntax"></a>Sintassi

finestra. External. selectedItemType ()

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di sola lettura che contiene una delle [costanti del percorso della libreria](library-location-constants.md).

## <a name="remarks"></a>Commenti

Questa proprietà viene utilizzata in combinazione con la proprietà **External. selectedItemID** . Ad esempio, se **selectedItemType** è uguale a CPTrackID, **SELECTEDITEMID** è l'ID della traccia selezionata. Per ulteriori informazioni sul modo in cui Windows Media Player caratterizza le visualizzazioni del contenuto di un negozio online, vedere [posizione e elemento selezionato](location-and-selected-item.md).

Per alcune visualizzazioni di Windows Media Player è selezionato un particolare elemento multimediale. Si supponga, ad esempio, che la visualizzazione corrente rappresenti un album. Un album è un contenitore di tracce, quindi **selectedItemType** è uguale a CPTrackID e **SELECTEDITEMID** è l'ID della traccia selezionata. Altre visualizzazioni non dispongono di un elemento multimediale selezionato. Ad esempio, se l'utente fa clic sul nodo radice dell'archivio online nel controllo di visualizzazione albero, Windows Media Player visualizza una pagina di individuazione fornita dal negozio online. Il lettore non visualizza alcun contenitore di elementi multimediali nell'interfaccia utente del lettore. In tal caso, **selectedItemType** è uguale a UnknownLocation e **selectedItemID** è uguale alla stringa vuota.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. selectedItemID**](external-selecteditemid.md)
</dt> <dt>

[**Posizione e elemento selezionato**](location-and-selected-item.md)
</dt> </dl>

 

 





