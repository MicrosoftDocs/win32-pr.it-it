---
title: Costanti (riferimenti per animazioni Windows)
description: Documentazione di riferimento per costanti ed enumerazioni definite da Gestione animazioni di Windows.
ms.assetid: c590cf68-28ce-4d7d-949d-2683ece3c12d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2cceae981ea7cc0e2b78d9dadbea88075eb3ad
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300759"
---
# <a name="constants-windows-animation-reference"></a>Costanti (riferimenti per animazioni Windows)

Documentazione di riferimento per costanti ed enumerazioni definite da Gestione animazioni di Windows.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                                             | Descrizione                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_dimensione animazione interfaccia utente \_ \_ sconosciuta**](ui-animation-dimension-unknown.md)<br/>                                            | Indica che non è possibile recuperare la dimensione richiesta.<br/>                                                                                                                                                                                                     |
| [**\_iterazione animazione interfaccia utente \_ \_ nessuno**](-ui-animation-iteration-none.md)<br/>                                                 | Indica che si tratta della voce iniziale in un ciclo specificato.<br/>                                                                                                                                                                                                     |
| [**\_avvio dello \_ storyboard del fotogramma chiave animazione interfaccia \_ utente \_**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85))<br/>                           | Rappresenta il fotogramma chiave implicito all'inizio di ogni Storyboard.<br/>                                                                                                                                                                                              |
| [**animazione dell'interfaccia utente ripetuta per un periodo \_ \_ \_ illimitato**](ui-animation-repeat-indefinitely.md)<br/>                                        | Indica che l'intervallo tra due fotogrammi chiave in uno storyboard deve essere ripetuto per un tempo illimitato fino a quando non viene chiamato il metodo [**IUIAnimationStoryboard:: terminate**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) .<br/>                                                            |
| [**la ripetizione dell'animazione dell'interfaccia utente si \_ \_ \_ \_ conclude \_ a \_ oltranza**](ui-animation-repeat-indefinitely-conclude-at-end.md)<br/>     | Indica che l'intervallo tra due fotogrammi chiave in uno storyboard deve essere ripetuto per un tempo illimitato fino a quando il ciclo del fotogramma chiave termina sul fotogramma chiave finale quando viene chiamato il metodo [**IUIAnimationStoryboard:: terminate**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) .<br/>   |
| [**\_ripetizione indefinita dell'animazione dell'interfaccia utente \_ \_ \_ \_ all' \_ inizio**](ui-animation-repeat-indefinitely-conclude-at-start.md)<br/> | Indica che l'intervallo tra due fotogrammi chiave in uno storyboard deve essere ripetuto per un tempo illimitato fino a quando il ciclo del fotogramma chiave termina sul fotogramma chiave iniziale quando viene chiamato il metodo [**IUIAnimationStoryboard:: terminate**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) .<br/> |
| [**\_secondi di animazione interfaccia utente \_ \_**](ui-animation-seconds-eventually.md)<br/>                                          | Indica che l'animazione Windows può ritardare l'avvio pianificato di uno storyboard per il tempo necessario per evitare conflitti di pianificazione.<br/>                                                                                                                     |
| [**\_secondi animazione interfaccia utente \_ \_ infinita**](ui-animation-seconds-infinite.md)<br/>                                              | Indica che non sono presenti eventi pianificati.<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sull'animazione Windows](windows-animation-reference.md)
</dt> </dl>

 

