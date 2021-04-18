---
description: Autenticazione con smart card
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: Autenticazione con smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241d323f4c5e982fee96f44002da316d5d645d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316230"
---
# <a name="smart-card-authentication"></a>Autenticazione con smart card

Le parti di base del [*sottosistema Smart Card*](../secgloss/s-gly.md) sono basate sugli standard PC/SC (vedere le specifiche in [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ). Queste parti di base includono:

-   [*Gestore di risorse*](../secgloss/r-gly.md) che usa un'API Windows.
-   [*Interfaccia utente*](../secgloss/u-gly.md) (UI) che funziona con gestione risorse.
-   Diversi [*provider di servizi*](../secgloss/s-gly.md) di base che forniscono accesso a servizi specifici. Diversamente dall'API Windows di Resource Manager, i provider di servizi usano un modello di interfaccia COM per fornire servizi [*Smart Card*](../secgloss/s-gly.md) .

Nella figura seguente sono illustrate le relazioni di queste parti nell'architettura complessiva delle smart card.

![architettura Smart Card](images/smartovr2a.png)

Per informazioni sul funzionamento del [*sottosistema Smart Card*](../secgloss/s-gly.md) con altri servizi disponibili in Microsoft Internet Security Framework, vedere [relazioni con altri servizi](relation-to-other-services.md).

Per informazioni sull'autenticazione con smart card, vedere gli argomenti seguenti.



| Argomenti                                                                      | Contenuto                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Concetti relativi alle smart card](smart-card-concepts.md)<br/>                   | Concetti di base e Descrizione dell'interazione tra utenti e smart card.<br/>                                                                                                                                                        |
| [Gestione risorse smart card](smart-card-resource-manager.md)<br/>   | Informazioni sull'API di Resource Manager, che consente di gestire l'accesso ai [*lettori*](../secgloss/r-gly.md) e alle [*Smart Card*](../secgloss/s-gly.md).<br/> |
| [Interfaccia utente della smart card](smart-card-user-interface.md)<br/>       | Informazioni sulla finestra di [*dialogo comune della smart card*](../secgloss/s-gly.md).<br/>                                                                                   |
| [Provider di servizi Smart Card](smart-card-service-providers.md)<br/> | Informazioni su interfacce, comandi e wrapper che forniscono funzionalità per smart card.<br/>                                                                                                                                              |



 

Inoltre, è possibile trovare gli attuali sviluppi delle smart card Microsoft all'indirizzo [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) .

 

 
