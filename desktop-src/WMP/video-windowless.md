---
title: VIDEO. senza finestra
description: L'attributo senza finestra specifica o recupera un valore che indica se il controllo video sarà finestra o senza finestra; ovvero se l'intero rettangolo del controllo sarà sempre visibile o possa essere ritagliato.
ms.assetid: d59e6baf-374b-48f6-b99f-35a83af7feb6
keywords:
- VIDEO. finestre senza finestra Media Player
topic_type:
- apiref
api_name:
- VIDEO.windowless
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a17d905d2ba8c11254476337d656890469b2b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328289"
---
# <a name="videowindowless"></a>VIDEO. senza finestra

L'attributo senza **finestra** specifica o recupera un valore che indica se il controllo video sarà finestra o senza finestra; ovvero se l'intero rettangolo del controllo sarà sempre visibile o possa essere ritagliato. Può essere impostato solo in fase di progettazione.

``` syntax
        elementID.windowless
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** specificato in fase di progettazione e di sola lettura in seguito.



| Valore | Descrizione                              |
|-------|------------------------------------------|
| true  | Il controllo video sarà privo di finestra.        |
| false | Valore predefinito. Il controllo video sarà a finestre. |



 

## <a name="remarks"></a>Commenti

Se si desidera una finestra video non rettangolare o si desidera coprire qualsiasi parte della finestra video con un'immagine, questo attributo deve essere impostato su true. In questo modo si sacrificano alcune prestazioni per eseguire il troncamento necessario.

La riproduzione video è ottimizzata per la riproduzione non ritagliata. In questo caso, l'attributo senza **finestra** è impostato su false e l'intero rettangolo video viene sempre visualizzato. Qualsiasi immagine che copre la finestra video viene ignorata e la finestra del video ha l'ordine z di livello più alto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIDEO**](video-element.md)
</dt> </dl>

 

 





