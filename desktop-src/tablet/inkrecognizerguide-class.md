---
description: Rappresenta l'area utilizzata dal riconoscimento in cui è possibile disegnare l'input penna. L'area è nota come guida al riconoscimento.
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: Classe InkRecognizerGuide (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerGuide
- InkRecognizerGuide.IInkRecognizerGuide
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 758c2ac58803b0086a4a4083545a66d250799b414bd44e3814c90de37ca9d082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675668"
---
# <a name="inkrecognizerguide-class"></a>Classe InkRecognizerGuide

Rappresenta l'area utilizzata dal riconoscimento in cui è possibile disegnare l'input penna. L'area è nota come guida al riconoscimento.

**InkRecognizerGuide** ha questi tipi di membri:

-   [Interfacce](#interfaces)
-   [Proprietà](#properties)

### <a name="interfaces"></a>Interfacce

La **classe InkRecognizerGuide** definisce queste interfacce.



| Interfaccia               | Descrizione                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| **IInkRecognizerGuide** | Questo oggetto implementa **l'interfaccia COM IInkRecognizerGuide.**<br/> |



 

### <a name="properties"></a>Proprietà

La **classe InkRecognizerGuide** ha queste proprietà.



| Proprietà                                                       | Tipo di accesso           | Descrizione                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Colonne**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | Lettura/Scrittura<br/> | Ottiene o imposta il numero di colonne nella casella della guida.<br/>                                                                |
| [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta la casella disegnata fisicamente sullo schermo del tablet e in cui avviene la scrittura.<br/>              |
| [**GuideData**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | Lettura/Scrittura<br/> | Ottiene o imposta i dati della guida per gli sviluppatori C++.<br/>                                                                         |
| [**Midline**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | Lettura/Scrittura<br/> | Ottiene o imposta l'altezza della linea media. L'altezza della linea mediana è la distanza dalla linea di base alla linea mediana della casella disegnata.<br/> |
| [**Righe**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta il numero di righe nella casella della guida.<br/>                                                                   |
| [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta l'area di scrittura invisibile della casella della guida in cui è effettivamente possibile eseguire la scrittura.<br/>                  |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il [**metodo CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

Per impostazione predefinita, non è disponibile alcuna guida per il riconoscimento. Una guida predefinita ha tutti i valori delle proprietà impostati su 0. È necessario utilizzare le proprietà di questo oggetto per impostare la guida.

Se l'applicazione ha tracciato linee guida sullo schermo in cui si prevede che l'utente scrivo, l'applicazione deve impostare i valori delle proprietà della guida del riconoscitore per informare il riconoscitore. Queste proprietà sono solo per l'uso del sistema di riconoscimento. L'impostazione di questi elementi non di per sé non consente di tracciare indicazioni visive sullo schermo. L'applicazione o il controllo traccia gli indizi visivi.

La guida al riconoscimento può essere costituita da righe e colonne e offrono al sistema di riconoscimento un contesto migliore in cui eseguire il riconoscimento. Lettere come "t" e "I" sono più facilmente riconosciute quando si usa una guida per fornire contesto all'input penna. Ad esempio, è possibile disegnare linee orizzontali su uno schermo, che indicano dove deve verificarsi la scrittura (questo tipo di guida è costituito solo da righe e nessuna colonna). Scrivendo sulle righe, invece di uno spazio arbitrario, l'accuratezza del riconoscimento migliora.

La guida specifica i limiti dell'input penna nelle coordinate dello spazio input penna.

La [**proprietà DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) può definire una casella delle stesse dimensioni o più piccola della casella definita dalla [**proprietà WritingBox.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)

La figura seguente mostra gli elementi di una guida di riconoscimento con due righe e nessuna colonna.

![illustrazione che mostra gli elementi della guida al riconoscimento](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

Oltre a disegnare linee sullo schermo che mostrano agli utenti dove scrivere, è possibile disegnare celle sullo schermo in cui vengono scritti caratteri o parole. Questa operazione è detta input boxed ed è utile con alcune lingue dell'Asia. Per determinare se il sistema di riconoscimento è in grado di eseguire l'input boxed, chiamare la [**proprietà Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) [**dell'oggetto IInkRecognizer.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)

La figura seguente mostra una guida al riconoscimento con quattro colonne.

![illustrazione che mostra la guida al riconoscimento con quattro colonne](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> </dl>

 

