---
title: Proprietà (IInertiaProcessor)
description: Questa sezione contiene le proprietà per l'interfaccia IInertiaProcessor.
ms.assetid: 47fd1a49-8e14-4076-8ce6-f0c4917e8cf1
keywords:
- Windows Touch, interfaccia IInertiaProcessor
- Windows Touch, proprietà dell'interfaccia
- inerzia, interfaccia IInertiaProcessor
- Interfaccia IInertiaProcessor, proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab3e1754c7b723b4be446e82fd0ba39fc67af5d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400052"
---
# <a name="properties-iinertiaprocessor"></a>Proprietà (IInertiaProcessor)

Questa sezione contiene le proprietà per l'interfaccia [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) .



| Proprietà                                                                               | Descrizione                                                                                               |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**InitialOriginX**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginx)                             | Specifica la posizione orizzontale iniziale per una destinazione con Intertia.                                   |
| [**InitialOriginY**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialoriginy)                             | Specifica la posizione verticale iniziale per una destinazione con Intertia.                                     |
| [**InitialVelocityX**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityx)                         | Specifica lo spostamento iniziale dell'oggetto di destinazione sull'asse orizzontale.                              |
| [**InitialVelocityY**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialvelocityy)                         | Specifica lo spostamento iniziale dell'oggetto di destinazione sull'asse verticale.                                |
| [**InitialAngularVelocity**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialangularvelocity)             | Specifica la velocità rotazionale della destinazione quando inizia il movimento.                                    |
| [**InitialExpansionVelocity**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialexpansionvelocity)         | Specifica la frequenza di espansione RADIUS della destinazione quando inizia lo spostamento.                               |
| [**InitialRadius**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialradius)                               | Specifica la distanza tra il bordo della destinazione e il centro prima che l'oggetto sia stato modificato.          |
| [**BoundaryLeft**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryleft)                                 | Limita la distanza verso il lato sinistro dello schermo che l'oggetto di destinazione può spostare.                                 |
| [**BoundaryTop**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarytop)                                   | Limita la distanza verso la parte superiore dello schermo che l'oggetto di destinazione può spostare.                                  |
| [**BoundaryRight**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundaryright)                               | Limita la distanza verso il lato destro dello schermo che l'oggetto di destinazione può spostare.                           |
| [**BoundaryBottom**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_boundarybottom)                             | Limita la distanza verso la parte inferiore dello schermo che l'oggetto di destinazione può spostare.                               |
| [**ElasticMarginLeft**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginleft)                       | Specifica l'area a sinistra per il rimbalzo dell'oggetto di destinazione.                                            |
| [**ElasticMarginTop**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmargintop)                         | Specifica l'area superiore per il rimbalzo dell'oggetto di destinazione.                                             |
| [**ElasticMarginRight**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginright)                     | Specifica l'area più a destra per il rimbalzo dell'oggetto di destinazione.                                           |
| [**ElasticMarginBottom**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_elasticmarginbottom)                   | Specifica l'area inferiore per il rimbalzo dell'oggetto di destinazione.                                              |
| [**DesiredAngularDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration)     | Specifica la frequenza desiderata per cui l'oggetto di destinazione smetterà di girare in radianti per msec.                |
| [**DesiredRotation**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredrotation)                           | Specifica la distanza desiderata (in radianti) che un oggetto verrà modificato dal processore di inerzia. |
| [**DesiredExpansion**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansion)                         | Specifica la modifica desiderata nel raggio medio dell'oggetto.                                        |
| [**DesiredExpansionDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredexpansiondeceleration) | Specifica la frequenza con cui l'oggetto si arresterà in espansione.                                              |
| [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)                   | Specifica la frequenza desiderata per la decelerazione delle operazioni di conversione.                              |
| [**DesiredDisplacement**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddisplacement)                   | Specifica la distanza desiderata per il trasferimento dell'oggetto.                                              |
| [**InitialTimestamp**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_initialtimestamp)                         | Specifica il timestamp di inizio per un oggetto di destinazione con inerzia.                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




