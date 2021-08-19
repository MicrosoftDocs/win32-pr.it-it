---
title: Proprietà (IInertiaProcessor)
description: Questa sezione contiene le proprietà per l'interfaccia IInertiaProcessor.
ms.assetid: 47fd1a49-8e14-4076-8ce6-f0c4917e8cf1
keywords:
- Windows Interfaccia Touch,IInertiaProcessor
- Windows Touch, proprietà dell'interfaccia
- inerzia, interfaccia IInertiaProcessor
- Interfaccia IInertiaProcessor,proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7825a97545c897f402144ce5113b79650b9eba31e19da7ceef1459ae6cdc13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030125"
---
# <a name="properties-iinertiaprocessor"></a>Proprietà (IInertiaProcessor)

Questa sezione contiene le proprietà per [**l'interfaccia IInertiaProcessor.**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)



| Proprietà                                                                               | Descrizione                                                                                               |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**InitialOriginX**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginx)                             | Specifica la posizione orizzontale iniziale per una destinazione con intertia.                                   |
| [**InitialOriginY**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginy)                             | Specifica la posizione verticale iniziale per una destinazione con intertia.                                     |
| [**InitialVelocityX**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityx)                         | Specifica lo spostamento iniziale dell'oggetto di destinazione sull'asse orizzontale.                              |
| [**InitialVelocityY**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityy)                         | Specifica lo spostamento iniziale dell'oggetto di destinazione sull'asse verticale.                                |
| [**InitialAngularVelocity**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialangularvelocity)             | Specifica la velocità di rotazione della destinazione all'inizio dello spostamento.                                    |
| [**InitialExpansionVelocity**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialexpansionvelocity)         | Specifica la velocità di espansione del raggio della destinazione all'inizio dello spostamento.                               |
| [**InitialRadius**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialradius)                               | Specifica la distanza dal bordo della destinazione al centro prima della modifica dell'oggetto.          |
| [**BoundaryLeft**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryleft)                                 | Limita la distanza a sinistra dello schermo che l'oggetto di destinazione può spostare.                                 |
| [**BoundaryTop**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarytop)                                   | Limita la distanza verso la parte superiore dello schermo che l'oggetto di destinazione può spostare.                                  |
| [**BoundaryRight**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryright)                               | Limita la distanza verso il lato destro dello schermo che l'oggetto di destinazione può spostare.                           |
| [**BoundaryBottom**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarybottom)                             | Limita la distanza verso la parte inferiore dello schermo che l'oggetto di destinazione può spostare.                               |
| [**ElasticMarginLeft**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginleft)                       | Specifica l'area più a sinistra per il rimbalzo dell'oggetto di destinazione.                                            |
| [**ElasticMarginTop**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmargintop)                         | Specifica l'area superiore per il rimbalzo dell'oggetto di destinazione.                                             |
| [**ElasticMarginRight**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginright)                     | Specifica l'area più a destra per il rimbalzo dell'oggetto di destinazione.                                           |
| [**ElasticMarginBottom**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginbottom)                   | Specifica l'area inferiore per il rimbalzo dell'oggetto di destinazione.                                              |
| [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration)     | Specifica la frequenza desiderata in base alla quale l'oggetto di destinazione interromperà la rotazione in radianti per msec.                |
| [**DesiredRotation**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredrotation)                           | Specifica la distanza desiderata (in radianti) che un oggetto verrà modificato dal processore di inerzia. |
| [**DesiredExpansion**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansion)                         | Specifica la modifica desiderata nel raggio medio dell'oggetto .                                        |
| [**DesiredExpansionDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansiondeceleration) | Specifica la velocità di arresto dell'espansione dell'oggetto.                                              |
| [**Desireddeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)                   | Specifica la velocità desiderata con cui le operazioni di conversione deceleranno.                              |
| [**DesiredDisplacement**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddisplacement)                   | Specifica la distanza desiderata percorsa dall'oggetto.                                              |
| [**InitialTimestamp**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialtimestamp)                         | Specifica il timestamp iniziale per un oggetto di destinazione con inerzia.                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Iinertiaprocessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




