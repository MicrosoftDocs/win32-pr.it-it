---
title: Nuove funzionalità in TSF
description: Con il rilascio di Microsoft WindowsXP Service Pack1, il Framework di servizi di testo (TSF) dispone di numerose nuove funzionalità.
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- Framework servizi di testo (TSF), nuove funzionalità
- TSF (Text Services Framework), nuove funzionalità
- Servizi di testo, nuove funzionalità
- Applicazioni abilitate per TSF, nuove funzionalità
- Framework servizi di testo (TSF), supporto avanzato
- TSF (Text Services Framework), supporto avanzato
- Servizi di testo, supporto avanzato
- Applicazioni abilitate per TSF, supporto avanzato
- Framework servizi di testo (TSF), Rich Edit
- TSF (Text Services Framework), Rich Edit
- Servizi di testo, Rich Edit
- Applicazioni abilitate per TSF, Rich Edit
- Modifica avanzata
- Framework servizi di testo (TSF), sicurezza
- TSF (Framework di servizi di testo), sicurezza
- Servizi di testo, sicurezza
- Applicazioni abilitate per TSF, sicurezza
- sicurezza per TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7a345087304be638be93fa352845cdd468bf15
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399117"
---
# <a name="new-features-in-tsf"></a>Nuove funzionalità in TSF

Con il rilascio di Microsoft WindowsXP Service Pack1, il Framework di servizi di testo (TSF) dispone di numerose nuove funzionalità.

## <a name="extended-support-of-advanced-text-services"></a>Supporto esteso dei servizi di testo avanzati

È stato aggiunto il supporto a TSF e Windows per fornire un'interfaccia utente coerente per tutte le applicazioni sul desktop. Questo nuovo supporto Abilita le applicazioni o i controlli legacy che non sono a conoscenza di TSF per sfruttare gratuitamente alcuni servizi di testo avanzati. Ad esempio, è ora possibile usare la dettatura vocale e la grafia per immettere il testo in un documento in qualsiasi applicazione.

Questa nuova funzionalità è disponibile solo per il servizio WindowsXP Pack1 o versione successiva. È disattivata per impostazione predefinita. Per abilitarla, fare clic sulla casella di controllo nella scheda nuovo **Avanzate** della parte **servizi di testo e lingue di input** del pannello di controllo **Opzioni internazionali e della lingua** .

![supporto delle applicazioni non compatibili nel pannello di controllo TSF](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a>Supporto Rich Edit

[Microsoft® Rich Edit](../controls/rich-edit-controls.md) La versione 4,1, usata dalle applicazioni per visualizzare e modificare il testo con una formattazione speciale per caratteri e paragrafi, ora espone la funzionalità TSF. Per impostazione predefinita, questo supporto è disattivato. Per abilitare TSF in Rich Edit, un'applicazione host invia un messaggio di finestra speciale al controllo Rich Edit.

## <a name="security-improvements"></a>Miglioramenti alla sicurezza

La sicurezza e l'affidabilità di TSF sono state notevolmente migliorate, per ridurre la probabilità che un programma ostile possa accedere allo stack, all'heap o ad altre posizioni di memoria sicure. È stata migliorata anche la sicurezza delle applicazioni di esempio Software Development Kit (SDK) e dei servizi di testo.

 

 