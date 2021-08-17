---
title: Nuove funzionalità di TSF
description: Con il rilascio di Microsoft WindowsXP Service Pack1, Framework servizi di testo (TSF) include diverse nuove funzionalità.
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- Framework servizi di testo (TSF), nuove funzionalità
- TSF (Framework servizi di testo),nuove funzionalità
- servizi di testo, nuove funzionalità
- Applicazioni abilitate per TSF, nuove funzionalità
- Framework servizi di testo (TSF), supporto avanzato
- TSF (Framework servizi di testo), supporto avanzato
- servizi di testo, supporto avanzato
- Applicazioni abilitate per TSF, supporto avanzato
- Framework servizi di testo (TSF), Rich Edit
- TSF (Framework servizi di testo), Rich Edit
- servizi di testo, Rich Edit
- Applicazioni abilitate per TSF, Rich Edit
- Rich Edit
- Framework servizi di testo (TSF), sicurezza
- TSF (Framework servizi di testo),security
- servizi di testo, sicurezza
- applicazioni abilitate per TSF, sicurezza
- sicurezza per TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73494d4538b25dfa0b004c8691391fb1c572c7ce6d82247cacae4fb9e0a838
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952023"
---
# <a name="new-features-in-tsf"></a>Nuove funzionalità di TSF

Con il rilascio di Microsoft WindowsXP Service Pack1, Framework servizi di testo (TSF) include diverse nuove funzionalità.

## <a name="extended-support-of-advanced-text-services"></a>Supporto esteso dei servizi di testo avanzati

È stato aggiunto il supporto a TSF e Windows per fornire un'interfaccia utente coerente per tutte le applicazioni sul desktop. Questo nuovo supporto consente ad applicazioni o controlli legacy che non sono a conoscenza di TSF di sfruttare gratuitamente alcuni servizi di testo avanzati. Ad esempio, la dettatura vocale e la grafia possono ora essere usate per immettere testo in un documento in qualsiasi applicazione.

Questa nuova funzionalità è disponibile solo per WindowsXP Service Pack1 o versione successiva. È disattivato per impostazione predefinita. Per abilitarlo, fare clic sulla  casella di controllo nella nuova scheda Avanzate nella parte Servizi di testo e lingue di **input** del pannello di controllo Opzioni **internazionali** e della lingua.

![supporto dell'applicazione inconsapevole nel pannello di controllo tsf](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a>Supporto di Rich Edit

[Microsoft® Rich Edit](../controls/rich-edit-controls.md) La versione 4.1, usata dalle applicazioni per visualizzare e modificare testo con formattazione speciale di caratteri e paragrafi, ora espone la funzionalità TSF. Per impostazione predefinita, questo supporto è disattivato. Per abilitare TSF in Rich Edit, un'applicazione host invia un messaggio di finestra speciale al controllo Rich Edit.

## <a name="security-improvements"></a>Miglioramenti alla sicurezza

La sicurezza e l'affidabilità di TSF sono state notevolmente migliorate, per ridurre la probabilità che un programma ostile possa accedere allo stack, all'heap o ad altre posizioni di memoria sicura. È stata migliorata anche la sicurezza delle applicazioni di esempio sdk (Software Development Kit) e dei servizi di testo.

 

 