---
title: AmbientAttributes. accKeyboardShortcut
description: L'attributo accKeyboardShortcut specifica o Recupera una descrizione del tasto di scelta rapida per qualsiasi elemento.
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- Media Player Windows AmbientAttributes. accKeyboardShortcut
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d7259f0b32e3575d902a83b6508383361028d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326742"
---
# <a name="ambientattributesacckeyboardshortcut"></a>AmbientAttributes. accKeyboardShortcut

L'attributo **accKeyboardShortcut** specifica o Recupera una descrizione del tasto di scelta rapida per qualsiasi elemento.

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a>Valori possibili

Questo attributo è una **stringa** di lettura/scrittura con un valore predefinito di "" (stringa vuota). Per l'elemento **Button** , il valore predefinito di questo attributo è "barra spaziatrice o invio". Per l'elemento **Slider** , il valore predefinito è "freccia destra/freccia su per aumentare, freccia sinistra/giù per diminuire".

## <a name="remarks"></a>Commenti

Questo attributo viene utilizzato per scopi di accessibilità. Consente una descrizione del tasto di scelta rapida per qualsiasi elemento da leggere ad alta voce da un programma Reader. Questo attributo non imposta il collegamento. Lo Scripter deve eseguire tale operazione.

Questo attributo si applica anche agli elementi Button all'interno del controllo gruppo di pulsanti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------|
| Versione<br/> | Windows Media Player 9 serie o versione successiva<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributi di ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





