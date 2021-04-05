---
title: Ridistribuzione del software
description: Ridistribuzione del software
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- Windows Media Format SDK, ridistribuzione software
- ASF (Advanced Systems Format), ridistribuzione del software
- ASF (formato avanzato dei sistemi), ridistribuzione del software
- Windows Media Format SDK, ridistribuzione
- ASF (Advanced Systems Format), ridistribuzione
- ASF (formato avanzato dei sistemi), ridistribuzione
- ridistribuzione del software, informazioni
- ridistribuzione, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d51f332f5b0e038293a1dbe1dbf59015931d67e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709475"
---
# <a name="software-redistribution"></a>Ridistribuzione del software

L'inclusione di software in formato Windows Media in un'installazione di applicazione è nota come ridistribuzione. Windows Media Format SDK include un pacchetto di installazione che può essere incluso nella configurazione dell'applicazione. Il pacchetto di installazione è un file eseguibile denominato wmfdist95.exe. Quando si installa Windows Media Format SDK, il pacchetto di installazione viene copiato nella \\ cartella Redist della directory di installazione (c: \\ WMSDK \\ wmfsdk per impostazione predefinita).

Nelle sezioni seguenti vengono fornite le procedure e altre informazioni per la configurazione della ridistribuzione software.



| Sezione                                                                            | Descrizione                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Per creare una configurazione di ridistribuzione](to-create-a-redistribution-setup.md)           | Viene descritta la procedura per la creazione di una configurazione dell'applicazione.                                                                                                                       |
| [Rilevamento dello stato di installazione](detecting-setup-status.md)                               | Fornisce il codice di esempio che controlla lo stato di installazione del registro di sistema per determinare se è necessario installare il pacchetto di ridistribuzione.                                    |
| [Codice di esempio per l'installazione della ridistribuzione](example-code-for-redistribution-setup.md) | Fornisce il codice di esempio che può essere utilizzato nella routine di installazione per eseguire i pacchetti di ridistribuzione in modalità non interattiva e notificare la routine di installazione quando il computer deve essere riavviato. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Considerazioni sui progetti**](project-considerations.md)
</dt> </dl>

 

 




