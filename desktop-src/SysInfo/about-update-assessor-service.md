---
description: Nell'argomento seguente viene descritto il funzionamento dell'API della piattaforma di valutazione di Windows As a Service (WaaS).
ms.assetid: B107AAF3-4248-40EF-ABD2-C5B31602AEF7
title: Informazioni sulla piattaforma di valutazione WaaS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb96dd27fdc5b8838f2e2a26e74f0046eda8f20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313270"
---
# <a name="about-the-waas-assessment-platform"></a>Informazioni sulla piattaforma di valutazione WaaS

Nell'argomento seguente viene descritto il funzionamento dell'API della piattaforma di valutazione di Windows As a Service (WaaS).

L'API WaaS Assessment offre al chiamante le informazioni seguenti:

-   Se un dispositivo si trova negli aggiornamenti Microsoft più recenti.
-   Indica se il dispositivo ha raggiunto la fine del supporto.
-   Ora di rilascio per gli aggiornamenti applicabili più recenti per il dispositivo.
-   Una valutazione del motivo per cui un dispositivo non è aggiornato e il potenziale impatto sul dispositivo.

La piattaforma di valutazione WaaS usa il modello API COM e viene eseguita automaticamente almeno una volta al giorno. Questo ciclo rileva le informazioni sulla versione applicabili. Durante il periodo di memorizzazione nella cache, le valutazioni vengono effettuate rispetto alle informazioni sulla versione memorizzata nella cache. Se viene eseguita una chiamata al di fuori della finestra di scadenza della cache, viene effettuata una chiamata e una valutazione aggiornate, memorizzate nella cache e restituite. Quando viene effettuata una chiamata, il client di valutazione WaaS Contatta il servizio di valutazione WaaS con gli attributi del dispositivo e riceve un dossier di informazioni applicabili al dispositivo. Il client usa quindi queste informazioni a fronte delle informazioni raccolte sul dispositivo per eseguire la valutazione.

> [!NOTE]
> Il codice deve disporre dei privilegi di amministratore per chiamare l'API WAAS assessment. Per ulteriori informazioni sullo sviluppo di applicazioni che richiedono privilegi di amministratore, vedere [questo articolo](../secauthz/developing-applications-that-require-administrator-privilege.md).

 
