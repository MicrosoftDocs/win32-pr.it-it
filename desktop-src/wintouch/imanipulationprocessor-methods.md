---
title: Metodi (IInertiaProcessor)
description: Questa sezione contiene i metodi per l'interfaccia IInertiaProcessor.
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Windows Touch, interfaccia IInertiaProcessor
- Windows Touch, metodi di interfaccia
- inerzia, interfaccia IInertiaProcessor
- Interfaccia IInertiaProcessor, metodi
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662bb9aaa51400c4fd302f56bfec7c845ce57645
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300900"
---
# <a name="methods-iinertiaprocessor"></a>Metodi (IInertiaProcessor)

Questa sezione contiene i metodi per l'interfaccia [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .



| Metodo                                                 | Descrizione                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Reset**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | Inizializza il processore con il timestamp iniziale e riavvia l'inerzia.                                                                                                                                                    |
| [**Processo**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | Esegue calcoli per il ciclo corrente e può generare l'evento **Delta** o **Completed** a seconda che l'estrapolazione sia stata completata o meno. Se l'estrapolazione è stata completata al momento precedente, il metodo non è op. |
| [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | Esegue calcoli per il segno di selezione specificato e può generare l'evento **Delta** o **Completed** a seconda che l'estrapolazione sia stata completata o meno.                                                                        |
| [**Operazione completata**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | Termina la manipolazione corrente e arresta l'inerzia del processore di inerzia.                                                                                                                                              |
| [**CompleteTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | Termina la manipolazione corrente in corrispondenza del segno di selezione specificato, interrompe l'inerzia del processore di inerzia e genera l'evento ManipulationCompleted.                                                                                   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




