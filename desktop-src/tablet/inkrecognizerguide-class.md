---
description: Rappresenta l'area utilizzata dal riconoscitore in cui è possibile disegnare l'input penna. L'area è nota come guida al riconoscimento.
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: Classe InkRecognizerGuide (Msinkaut. h)
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
ms.openlocfilehash: 55729513f748afc87f184b73eaba976184307bc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234082"
---
# <a name="inkrecognizerguide-class"></a>Classe InkRecognizerGuide

Rappresenta l'area utilizzata dal riconoscitore in cui è possibile disegnare l'input penna. L'area è nota come guida al riconoscimento.

**InkRecognizerGuide** dispone di questi tipi di membri:

-   [Interfacce](#interfaces)
-   [Proprietà](#properties)

### <a name="interfaces"></a>Interfacce

La classe **InkRecognizerGuide** definisce queste interfacce.



| Interfaccia               | Descrizione                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| **IInkRecognizerGuide** | Questo oggetto implementa l'interfaccia com **IInkRecognizerGuide** .<br/> |



 

### <a name="properties"></a>Proprietà

La classe **InkRecognizerGuide** dispone di queste proprietà.



| Proprietà                                                       | Tipo di accesso           | Descrizione                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**Colonne**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | Lettura/Scrittura<br/> | Ottiene o imposta il numero di colonne nella casella della guida.<br/>                                                                |
| [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | Lettura/Scrittura<br/> | Ottiene o imposta la casella che viene fisicamente disegnata nella schermata del tablet e in cui avviene la scrittura.<br/>              |
| [**GuideData**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | Lettura/Scrittura<br/> | Ottiene o imposta i dati della Guida per gli sviluppatori C++.<br/>                                                                         |
| [**Midline**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | Lettura/Scrittura<br/> | Ottiene o imposta l'altezza del midline. L'altezza del midline è la distanza tra la linea di base e la linea media, della casella disegnata.<br/> |
| [**Righe**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | Lettura/Scrittura<br/> | Ottiene o imposta il numero di righe nella casella della guida.<br/>                                                                   |
| [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta l'area di scrittura invisibile della casella della Guida in cui può effettivamente essere eseguita la scrittura.<br/>                  |



 

## <a name="remarks"></a>Commenti

È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .

Per impostazione predefinita, non è disponibile alcuna guida per il riconoscimento. Una guida predefinita ha tutti i valori delle proprietà impostati su 0. Per impostare la guida, è necessario utilizzare le proprietà di questo oggetto.

Se l'applicazione ha disegnato linee guida sullo schermo in cui si prevede che l'utente scriva, l'applicazione deve impostare i valori delle proprietà della Guida di riconoscimento per informare il riconoscimento. Queste proprietà sono destinate solo all'uso del riconoscimento. L'impostazione non consente di creare gli indizi visivi sullo schermo. L'applicazione o il controllo disegna gli indizi visivi.

La guida per il riconoscimento può essere costituita da righe e colonne e fornisce al riconoscimento un contesto migliore in cui eseguire il riconoscimento. Le lettere quali "t" e "I" sono più facilmente riconosciute quando viene usata una guida per fornire contesto all'input penna. Ad esempio, è possibile creare linee orizzontali in una schermata, che mostrano dove deve essere eseguita la scrittura (questo tipo di guida è costituito solo da righe e senza colonne). Scrivendo sulle righe, invece di uno spazio arbitrario, l'accuratezza del riconoscimento migliora.

La guida specifica i limiti dell'input penna nelle coordinate dello spazio di input penna.

La proprietà [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) può definire una casella di dimensioni uguali o inferiori alla casella definita dalla proprietà [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) .

Nella figura seguente vengono illustrati gli elementi di una guida di riconoscimento con due righe e nessuna colonna.

![illustrazione che Mostra gli elementi della guida del riconoscitore](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

Oltre a disegnare linee sullo schermo che mostrano gli utenti in cui scrivere, è possibile disegnare le celle sullo schermo in cui vengono scritti i caratteri o le parole. Questo metodo è denominato input boxed ed è utile con alcune lingue asiatiche. Per determinare se il riconoscimento è in grado di eseguire l'input boxed, chiamare la proprietà [**capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) dell'oggetto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) .

Nella figura seguente viene illustrata una guida di riconoscimento con quattro colonne.

![illustrazione che mostra la guida al riconoscitore con quattro colonne](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                           |
| Intestazione<br/>                   | <dl> <dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[**Classe InkRecognizerContext**](inkrecognizercontext-class.md)
</dt> </dl>

 

