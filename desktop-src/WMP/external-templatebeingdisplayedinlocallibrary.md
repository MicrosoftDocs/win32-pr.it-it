---
title: External. templateBeingDisplayedInLocalLibrary
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. templateBeingDisplayedInLocalLibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- Media Player di Windows External. templateBeingDisplayedInLocalLibrary
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
ms.openlocfilehash: 9f1d9a93d870882a34014ea2d0d35f29b91f54d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328407"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a>External. templateBeingDisplayedInLocalLibrary

> [!Note]  
> Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.

 

La proprietà **templateBeingDisplayedInLocalLibrary** indica se il feed rappresentato dalla pagina di individuazione corrente viene visualizzato nel controllo di visualizzazione ad albero della libreria locale.

## <a name="syntax"></a>Sintassi

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a>Valori possibili

Questa proprietà è un **valore booleano** di sola lettura. **True** indica che il feed viene visualizzato nel controllo di visualizzazione ad albero della libreria locale.

## <a name="remarks"></a>Commenti

Una pagina di individuazione che rappresenta un feed per una playlist dinamica può visualizzare un pulsante che consente all'utente di salvare il feed nella propria libreria locale. Il salvataggio del feed, in questo contesto, significa che alcuni metadati vengono salvati nel computer dell'utente e il feed viene elencato sotto il nodo **playlist** nel controllo di visualizzazione albero libreria locale. Lo script nella pagina di individuazione può controllare la proprietà **templateBeingDisplayedInLocalLibrary** per determinare se l'utente ha già salvato il feed nella libreria locale. Se l'utente ha già salvato il feed, nella pagina di individuazione non verrà visualizzato il pulsante Salva.

Una pagina di individuazione che rappresenta un feed di radio deve controllare la proprietà **templateBeingDisplayedInLocalLibrary** per lo stesso motivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Media Player 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Oggetto esterno per i negozi di tipo 1 online**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





