---
title: Visualizza. barra del titolo
description: L'attributo barra del titolo recupera un valore che indica se la barra del titolo della finestra è visualizzata.
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- VIEW. barra del titolo Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea225103913e3906cf6cd3b129943fbf9b9f165
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326710"
---
# <a name="viewtitlebar"></a>Visualizza. barra del titolo

L'attributo **barra** del titolo recupera un valore che indica se la barra del titolo della finestra è visualizzata.

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è un **valore booleano** di sola lettura.



| Valore | Descrizione                             |
|-------|-----------------------------------------|
| true  | Valore predefinito. Viene visualizzata la barra del titolo della finestra. |
| false | La barra del titolo della finestra non viene visualizzata.      |



 

## <a name="remarks"></a>Commenti

Se viene visualizzata la barra del titolo, verranno visualizzati i pulsanti casella di controllo, Riduci a icona e Chiudi. Il titolo della finestra sarà il titolo dell'elemento di **visualizzazione** .

Se la **barra** del titolo è impostata su true e l'utente tenta di modificare il valore di **video. zoom**, la modifica non verrà eseguita a meno che non venga eseguito il monitoraggio dello **Zoom** e si intraprenda un'azione appropriata per il ridimensionamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------|
| Versione<br/> | Windows Media Player versione 7,0 o successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> <dt>

[**Visualizza. titolo**](view-title.md)
</dt> <dt>

[**VIDEO. zoom**](video-zoom.md)
</dt> </dl>

 

 





