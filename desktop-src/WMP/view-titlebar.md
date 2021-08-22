---
title: VIEW.titleBar
description: L'attributo titleBar recupera un valore che indica se viene visualizzata la barra del titolo della finestra.
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- View.titleBar Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb05550c22c342d14690f24f42c62a3af328eae65201b8138e82a7a33bf99fb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054069"
---
# <a name="viewtitlebar"></a>VIEW.titleBar

**L'attributo titleBar** recupera un valore che indica se viene visualizzata la barra del titolo della finestra.

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un valore booleano di **sola lettura.**



| Valore | Descrizione                             |
|-------|-----------------------------------------|
| true  | Valore predefinito. Viene visualizzata la barra del titolo della finestra. |
| false | La barra del titolo della finestra non viene visualizzata.      |



 

## <a name="remarks"></a>Commenti

Se viene visualizzata la barra del titolo, verranno visualizzati i pulsanti Casella di controllo, Riduci a icona e Chiudi. Il titolo della finestra sarà il titolo **dell'elemento VIEW.**

Se **titleBar** è impostato su true e l'utente tenta di modificare il valore di **Video.zoom,** la modifica non verrà eseguita a meno che l'interfaccia non monitori **lo zoom** e non esempi l'azione appropriata per ridimensionarsi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7.0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> <dt>

[**VIEW.title**](view-title.md)
</dt> <dt>

[**VIDEO.zoom**](video-zoom.md)
</dt> </dl>

 

 





