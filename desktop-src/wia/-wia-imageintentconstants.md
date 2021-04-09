---
description: Le costanti per finalità di immagine specificano il tipo di dati che l'immagine deve rappresentare.
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: Costanti per finalità di immagine (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_INTENT_IMAGE_TYPE_COLOR
- WIA_INTENT_IMAGE_TYPE_GRAYSCALE
- WIA_INTENT_IMAGE_TYPE_TEXT
- WIA_INTENT_MINIMIZE_SIZE
- WIA_INTENT_MAXIMIZE_QUALITY
- WIA_INTENT_BEST_PREVIEW
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f35c1f7436c8cc5110215a6ccf0383960ec3fb87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966843"
---
# <a name="image-intent-constants"></a>Costanti per finalità di immagine

Le costanti per finalità di immagine specificano il tipo di dati che l'immagine deve rappresentare. La proprietà [**WIA \_ IPS \_ cur \_ Intent**](-wia-wiaitempropscanneritem.md) scanner utilizza questi flag. Per fornire uno scopo, combinare un flag di tipo di immagine previsto con un flag di dimensioni/qualità previsto usando l'operatore OR. \_La finalità WIA \_ None non deve essere combinata con altri flag. Si noti che un'immagine non può essere sia di scala di grigi che di colore.

Di seguito sono riportate costanti per finalità di immagine valide:



| Flag del tipo di immagine previsto           | Descrizione                                  |
|-------------------------------------|----------------------------------------------|
| \_nessuna finalità \_ WIA                   | Valore predefinito. Non impostare alcuna proprietà. |
| \_colore del \_ tipo di immagine preventivo \_ per WIA \_     | Proprietà predefinite per il contenuto del colore.         |
| \_tipo di \_ immagine per finalità \_ WIA \_ | Proprietà predefinite per il contenuto in scala di grigi.     |
| \_ \_ testo tipo di immagine finalità \_ WIA \_      | Proprietà predefinite per il contenuto di testo.          |
| \_maschera del \_ tipo di immagine preventivo \_ WIA \_      | Maschera per tutti i flag del tipo di immagine.        |



 



| Flag di qualità/dimensioni immagine previsti | Descrizione                                  |
|-----------------------------------|----------------------------------------------|
| \_ \_ dimensioni minime della finalità WIA \_       | Proprietà predefinite per ridurre al minimo le dimensioni dell'immagine.    |
| \_finalità WIA \_ massimizza la \_ qualità    | Proprietà predefinite per ottimizzare la qualità dell'immagine. |
| \_ \_ maschera dimensioni finalità \_ WIA           | Maschera per tutti i flag di dimensione/qualità.      |
| \_Anteprima finalità \_ WIA \_        | Specifica l'anteprima della qualità migliore.          |



 

Nell'elenco seguente viene illustrato il nome della costante C/C++ seguito dal nome corrispondente tra parentesi utilizzate nello scripting. I nomi di script sono dal tipo enumerato WiaIntent. Si noti che non tutte le costanti sono disponibili tramite script.



| Costante/valore                                                                                                                                                                                                                                                                         | Descrizione                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <dt>**WIA \_ Tipo di immagine Intent \_ \_ \_ color**</dt> <dt>0x00000001</dt> </dl>             | Proprietà predefinite per il contenuto del colore.<br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <dt>**WIA \_ Tipo di immagine Intent in \_ \_ scala di \_ grigi**</dt> <dt>0x00000002</dt> </dl> | Proprietà predefinite per il contenuto in scala di grigi.<br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <dt>**WIA \_ Tipo di immagine preventivo 0x00000004 \_ \_ \_ testo**</dt> <dt></dt> </dl>                | Proprietà predefinite per il contenuto di testo.<br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <dt>**WIA \_ \_ \_ Dimensioni minime Intent**</dt> <dt>0x00010000</dt> </dl>                       | Proprietà predefinite per ridurre al minimo le dimensioni dell'immagine.<br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <dt>**WIA \_ Intent \_ massimizza la \_ qualità**</dt> <dt>0x00020000</dt> </dl>              | Proprietà predefinite per ottimizzare la qualità dell'immagine.<br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <dt>**WIA \_ Intent \_ Best \_ Preview**</dt> <dt>0x00040000</dt> </dl>                          | Specifica l'anteprima della qualità migliore.<br/>          |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




