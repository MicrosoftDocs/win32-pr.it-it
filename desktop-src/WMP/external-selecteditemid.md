---
title: External. selectedItemID
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. selectedItemID
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- Media Player di Windows External. selectedItemID
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
ms.openlocfilehash: 768387c9e20082ef47cb0f502a2c4572bf462f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324545"
---
# <a name="externalselecteditemid"></a>External. selectedItemID

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

La proprietà **selectedItemID** recupera l'identificatore dell'elemento multimediale attualmente selezionato in Windows Media Player.

## <a name="syntax"></a>Sintassi

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è una **stringa** di sola lettura.

## <a name="remarks"></a>Commenti

Questa proprietà viene utilizzata in combinazione con la proprietà [External. selectedItemType](external-selecteditemtype.md) . Ad esempio, se **selectedItemType** è uguale a CPTrackID, **SELECTEDITEMID** è l'ID della traccia selezionata. Per ulteriori informazioni sul modo in cui Windows Media Player caratterizza le visualizzazioni del contenuto di un negozio online, vedere [posizione e elemento selezionato](location-and-selected-item.md).

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

[**External. selectedItemType**](external-selecteditemtype.md)
</dt> <dt>

[**Posizione e elemento selezionato**](location-and-selected-item.md)
</dt> </dl>

 

 





