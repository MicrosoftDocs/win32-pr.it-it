---
title: Costanti (riferimenti Windows'animazione)
description: Documentazione di riferimento per costanti ed enumerazioni definite da Windows Animation Manager.
ms.assetid: c590cf68-28ce-4d7d-949d-2683ece3c12d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23964a2936b3879d551bcde9c2c25c2d63465e1cb4afb07cee25a3ce74a2a57f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419126"
---
# <a name="constants-windows-animation-reference"></a>Costanti (riferimenti Windows'animazione)

Documentazione di riferimento per costanti ed enumerazioni definite da Windows Animation Manager.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DIMENSIONE \_ \_ DELL'ANIMAZIONE DELL'INTERFACCIA \_ UTENTE SCONOSCIUTA**](ui-animation-dimension-unknown.md)<br/>                                            | Indica che non è possibile recuperare la dimensione richiesta.<br/>                                                                                                                                                                                                     |
| [**ITERAZIONE \_ DELL'ANIMAZIONE \_ \_ DELL'INTERFACCIA UTENTE NESSUNA**](-ui-animation-iteration-none.md)<br/>                                                 | Indica che si tratta della voce iniziale in un ciclo specificato.<br/>                                                                                                                                                                                                     |
| [**AVVIO DELLO \_ \_ STORYBOARD DEL FOTOGRAMMA CHIAVE DELL'ANIMAZIONE \_ \_ DELL'INTERFACCIA UTENTE**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85))<br/>                           | Rappresenta il fotogramma chiave implicito all'inizio di ogni storyboard.<br/>                                                                                                                                                                                              |
| [**\_RIPETIZIONE \_ \_ INDEFINITA DELL'ANIMAZIONE DELL'INTERFACCIA UTENTE**](ui-animation-repeat-indefinitely.md)<br/>                                        | Indica che l'intervallo tra due fotogrammi chiave in uno storyboard deve essere ripetuto a tempo indeterminato fino a quando non viene chiamato il metodo [**IUIAnimationStoryboard::Conclude.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude)<br/>                                                            |
| [**\_RIPETIZIONE \_ \_ INDEFINITA DELL'ANIMAZIONE DELL'INTERFACCIA \_ \_ UTENTE ALLA \_ FINE**](ui-animation-repeat-indefinitely-conclude-at-end.md)<br/>     | Indica che l'intervallo tra due fotogrammi chiave in uno storyboard deve ripetersi indefinitamente fino a quando il ciclo del fotogramma chiave termina sul fotogramma chiave finale quando viene chiamato il metodo [**IUIAnimationStoryboard::Conclude.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude)<br/>   |
| [**\_RIPETIZIONE \_ \_ INDEFINITA DELL'ANIMAZIONE DELL'INTERFACCIA UTENTE \_ \_ \_ ALL'AVVIO**](ui-animation-repeat-indefinitely-conclude-at-start.md)<br/> | Indica che l'intervallo tra due fotogrammi chiave in uno storyboard deve essere ripetuto a tempo indeterminato finché il ciclo del fotogramma chiave non termina sul fotogramma chiave iniziale quando viene chiamato il metodo [**IUIAnimationStoryboard::Conclude.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude)<br/> |
| [**SECONDI DI \_ ANIMAZIONE \_ DELL'INTERFACCIA \_ UTENTE ALLA FINE**](ui-animation-seconds-eventually.md)<br/>                                          | Indica che Windows'animazione può ritardare l'avvio pianificato di uno storyboard per il tempo necessario per evitare conflitti di pianificazione.<br/>                                                                                                                     |
| [**SECONDI DI \_ ANIMAZIONE \_ DELL'INTERFACCIA \_ UTENTE INFINITI**](ui-animation-seconds-infinite.md)<br/>                                              | Indica che non sono presenti eventi pianificati.<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Informazioni di riferimento sulle animazioni](windows-animation-reference.md)
</dt> </dl>

 

