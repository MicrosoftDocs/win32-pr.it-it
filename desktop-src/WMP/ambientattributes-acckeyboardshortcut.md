---
title: AmbientAttributes.accKeyboardShortcut
description: L'attributo accKeyboardShortcut specifica o recupera una descrizione dei tasti di scelta rapida per qualsiasi elemento.
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- AmbientAttributes.accKeyboardShortcut Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f467304bb9f38ab0683440d2a0ebc5fcc51adb92fbb1d50e8275eb36f256a159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055210"
---
# <a name="ambientattributesacckeyboardshortcut"></a>AmbientAttributes.accKeyboardShortcut

**L'attributo accKeyboardShortcut** specifica o recupera una descrizione dei tasti di scelta rapida per qualsiasi elemento.

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una  stringa di lettura/scrittura con valore predefinito "" (stringa vuota). Per **l'elemento BUTTON,** questo attributo ha il valore predefinito "BARRA SPAZIATRICE o INVIO". Per **l'elemento SLIDER,** il valore predefinito è "Freccia DESTRA/FRECCIA SU per aumentare, Freccia SINISTRA/GIÙ per diminuire".

## <a name="remarks"></a>Commenti

Questo attributo viene usato per scopi di accessibilità. Consente una descrizione del tasto di scelta rapida per qualsiasi elemento che può essere letto ad alta voce da un programma di lettura. Questo attributo non imposta il collegamento. Lo scripter deve eseguire questa operazione.

Questo attributo si applica anche agli elementi pulsante all'interno del controllo gruppo di pulsanti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player serie 9 o successive<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





