---
description: Le costanti di finalità dell'immagine specificano il tipo di dati che l'immagine deve rappresentare.
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: Costanti finalità immagine (Wiadef.h)
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
ms.openlocfilehash: 78130128a26057ed521512dd21acc5a1bd7e98c47ed689eaabc250a972c2a003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814121"
---
# <a name="image-intent-constants"></a>Costanti finalità immagine

Le costanti di finalità dell'immagine specificano il tipo di dati che l'immagine deve rappresentare. La proprietà dello scanner [**\_ della \_ finalità CUR \_ DI WIA IPS**](-wia-wiaitempropscanneritem.md) usa questi flag. Per fornire una finalità, combinare un flag del tipo di immagine desiderato con un flag di dimensioni/qualità previsto usando l'operatore OR. LA \_ FINALITÀ WIA \_ NONE non deve essere combinata con altri flag. Si noti che un'immagine non può essere sia in scala di grigi che a colori.

Di seguito sono riportate le costanti di finalità dell'immagine valide:



| Flag del tipo di immagine previsto           | Descrizione                                  |
|-------------------------------------|----------------------------------------------|
| FINALITÀ WIA \_ \_ NONE                   | Valore predefinito. Non impostare alcuna proprietà. |
| COLORE DEL TIPO \_ DI \_ IMMAGINE FINALITÀ \_ WIA \_     | Proprietà preimpostate per il contenuto a colori.         |
| TIPO DI IMMAGINE FINALITÀ WIA \_ \_ IN SCALA DI \_ \_ GRIGI | Proprietà predefinite per il contenuto in scala di grigi.     |
| TESTO DEL TIPO DI \_ \_ IMMAGINE FINALITÀ \_ WIA \_      | Proprietà predefinite per il contenuto di testo.          |
| MASCHERA DEL TIPO DI \_ \_ IMMAGINE FINALITÀ \_ WIA \_      | Maschera per tutti i flag del tipo di immagine.        |



 



| Flag di qualità/dimensioni dell'immagine prevista | Descrizione                                  |
|-----------------------------------|----------------------------------------------|
| DIMENSIONE MINIMA FINALITÀ WIA \_ \_ \_       | Proprietà preimpostate per ridurre al minimo le dimensioni dell'immagine.    |
| FINALITÀ WIA \_ \_ - OTTIMIZZARE LA \_ QUALITÀ    | Proprietà preimpostate per ottimizzare la qualità dell'immagine. |
| MASCHERA DIMENSIONI \_ \_ FINALITÀ WIA \_           | Maschera per tutti i flag di dimensione/qualità.      |
| ANTEPRIMA MIGLIORE \_ DELLA \_ FINALITÀ WIA \_        | Specifica la migliore qualità dell'anteprima.          |



 

L'elenco seguente mostra il nome della costante C/C++ seguito dal nome corrispondente tra parentesi usato nello scripting. I nomi degli script derivano dal tipo enumerato WiaIntent. Si noti che non tutte le costanti sono disponibili tramite script.



| Costante/valore                                                                                                                                                                                                                                                                         | Descrizione                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <dt>**WiA \_ COLORE \_ TIPO \_ IMMAGINE \_ FINALITÀ**</dt> <dt>0x00000001</dt> </dl>             | Proprietà preimpostate per il contenuto a colori.<br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <dt>**WiA \_ TIPO \_ DI IMMAGINE \_ \_ FINALITÀ GRAYSCALE**</dt> <dt>0x00000002</dt> </dl> | Proprietà predefinite per il contenuto in scala di grigi.<br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <dt>**WiA \_ TESTO \_ DEL TIPO DI IMMAGINE \_ \_ DELLA**</dt> <dt>FINALITÀ 0x00000004</dt> </dl>                | Proprietà predefinite per il contenuto di testo.<br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <dt>**WiA \_ DIMENSIONI \_ DELLA \_ FINALITÀ RIDOTTA A**</dt> <dt>0X00010000</dt> </dl>                       | Proprietà preimpostate per ridurre al minimo le dimensioni dell'immagine.<br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <dt>**WiA \_ INTENT \_ MAXIMIZE \_ QUALITY**</dt> <dt>0X00020000</dt> </dl>              | Proprietà preimpostate per ottimizzare la qualità dell'immagine.<br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <dt>**WiA \_ ANTEPRIMA \_ \_ DI INTENT BEST**</dt> <dt>0x00040000</dt> </dl>                          | Specifica la migliore qualità dell'anteprima.<br/>          |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




