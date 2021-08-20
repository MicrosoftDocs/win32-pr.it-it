---
title: External.templateBeingDisplayedInLocalLibrary
description: Nota Questo argomento descrive le funzionalità progettate per l'uso da parte dei negozi online. | External.templateBeingDisplayedInLocalLibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- External.templateBeingDisplayedInLocalLibrary Windows Media Player
topic_type:
- apiref
api_name:
- External.templateBeingDisplayedInLocalLibrary
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8292e2527fe14ec00a2bf7169b4e2ea2ca4c8229672625712ed3ad3a10e421e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648271"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a>External.templateBeingDisplayedInLocalLibrary

> [!Note]  
> In questo argomento vengono descritte le funzionalità progettate per l'utilizzo da parte dei negozi online. L'uso di questa funzionalità al di fuori del contesto di uno store online non è supportato.

 

La **proprietà templateBeingDisplayedInLocalLibrary** indica se il feed rappresentato dalla pagina di individuazione corrente viene visualizzato nel controllo di visualizzazione albero della libreria locale.

## <a name="syntax"></a>Sintassi

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un valore booleano **di sola lettura.** **TRUE** indica che il feed viene visualizzato nel controllo di visualizzazione albero della libreria locale.

## <a name="remarks"></a>Commenti

Una pagina di individuazione che rappresenta un feed per una playlist dinamica può visualizzare un pulsante che consente all'utente di "salvare" il feed nella libreria locale. Il salvataggio del feed, in questo contesto, significa che alcuni metadati vengono salvati nel computer dell'utente e il feed è elencato sotto il nodo **Playlist** nel controllo di visualizzazione albero della libreria locale. Lo script nella pagina di individuazione può esaminare la proprietà **templateBeingDisplayedInLocalLibrary** per determinare se l'utente ha già salvato il feed nella libreria locale. Se l'utente ha già salvato il feed, la pagina di individuazione non dovrebbe visualizzare il pulsante Salva.

Una pagina di individuazione che rappresenta un feed radio deve esaminare la proprietà **templateBeingDisplayedInLocalLibrary** per lo stesso motivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi online di tipo 1**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





