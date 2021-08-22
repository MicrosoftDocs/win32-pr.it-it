---
description: Autenticazione con smart card
ms.assetid: cb5c80ea-c15e-4f68-a94b-b458d69ff474
title: Autenticazione con smart card
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78bccfa9e762c137e332c26b5375584658c22718d336800b6dc73cf056ebde1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918008"
---
# <a name="smart-card-authentication"></a>Autenticazione con smart card

Le parti di base del [*sottosistema smart card*](../secgloss/s-gly.md) sono basate sugli standard PC/SC (vedere le specifiche in [https://www.pcscworkgroup.com/](https://www.pcscworkgroup.com/) ). Queste parti di base includono:

-   Gestione [*risorse che*](../secgloss/r-gly.md) usa un'API Windows locale.
-   Interfaccia [*utente (UI)*](../secgloss/u-gly.md) che funziona con gestione risorse.
-   Diversi provider [*di servizi di base*](../secgloss/s-gly.md) che forniscono l'accesso a servizi specifici. A differenza dell'API Windows resource manager, i provider di servizi usano un modello di interfaccia COM per [*fornire*](../secgloss/s-gly.md) smart card servizi.

La figura seguente illustra le relazioni di queste parti nell'architettura smart card generale.

![smart card architettura](images/smartovr2a.png)

Per informazioni sul funzionamento [*del sottosistema smart card*](../secgloss/s-gly.md) con altri servizi disponibili in Microsoft Internet Security Framework, vedere [Relazione ad altri servizi](relation-to-other-services.md).

Per informazioni sull'smart card autenticazione, vedere gli argomenti seguenti.



| Argomenti                                                                      | Contenuto                                                                                                                                                                                                                                           |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Concetti relativi alle smart card](smart-card-concepts.md)<br/>                   | Concetti di base e descrizione dell'interazione tra utenti e smart card.<br/>                                                                                                                                                        |
| [Smart Card Resource Manager](smart-card-resource-manager.md)<br/>   | Informazioni sull'API di Resource Manager, che gestisce l'accesso ai [*lettori*](../secgloss/r-gly.md) e [*alle smart card.*](../secgloss/s-gly.md)<br/> |
| [Smart Card Interfaccia utente](smart-card-user-interface.md)<br/>       | Informazioni sulla finestra [*smart card comune*](../secgloss/s-gly.md).<br/>                                                                                   |
| [Provider di servizi smart card](smart-card-service-providers.md)<br/> | Informazioni su interfacce, comandi e wrapper che forniscono smart card funzionalità.<br/>                                                                                                                                              |



 

Inoltre, gli attuali sviluppi smart card Microsoft sono disponibili all'indirizzo [https://www.microsoft.com/whdc/device/input/smartcard/default.mspx](https://www.microsoft.com/whdc/device/input/smartcard/default.mspx) .

 

 
