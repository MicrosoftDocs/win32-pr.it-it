---
title: Ridistribuzione del software
description: Ridistribuzione del software
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- Windows Media Format SDK, ridistribuzione del software
- Advanced Systems Format (ASF), ridistribuzione del software
- ASF (Advanced Systems Format), ridistribuzione del software
- Windows MEDIA Format SDK, ridistribuzione
- Advanced Systems Format (ASF), ridistribuzione
- ASF (Advanced Systems Format), ridistribuzione
- ridistribuzione del software, informazioni
- ridistribuzione, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b933df9319c342d8ed3502fc66757df2e6d8fd6e8d60309023ced6ffa042d5b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807891"
---
# <a name="software-redistribution"></a>Ridistribuzione del software

L'inclusione di Windows software Media Format in una configurazione dell'applicazione è nota come ridistribuzione. L Windows Media Format SDK include un pacchetto di installazione che può essere incluso nella configurazione dell'applicazione. Il pacchetto di installazione è un file eseguibile denominato wmfdist95.exe. Quando si installa Windows Media Format SDK, il pacchetto di installazione viene copiato nella cartella Redist della directory di installazione \\ (c: \\ wmsdk \\ wmfsdk per impostazione predefinita).

Le sezioni seguenti forniscono procedure e altre informazioni per la configurazione della ridistribuzione del software.



| Sezione                                                                            | Descrizione                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Per creare un'installazione di ridistribuzione](to-create-a-redistribution-setup.md)           | Viene descritta la procedura per la creazione di un'installazione dell'applicazione.                                                                                                                       |
| [Rilevamento dello stato dell'installazione](detecting-setup-status.md)                               | Fornisce codice di esempio che controlla lo stato di installazione del Registro di sistema per determinare se è necessario installare il pacchetto di ridistribuzione.                                    |
| [Codice di esempio per l'installazione della ridistribuzione](example-code-for-redistribution-setup.md) | Fornisce codice di esempio che può essere usato nella routine di installazione per eseguire i pacchetti di ridistribuzione in modalità non interattiva e inviare una notifica alla routine di installazione quando è necessario riavviare il computer. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Project Considerazioni**](project-considerations.md)
</dt> </dl>

 

 




