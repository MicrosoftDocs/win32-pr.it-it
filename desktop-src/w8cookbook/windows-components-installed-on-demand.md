---
title: Windows componenti installati su richiesta
description: Windows componenti installati su richiesta
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 765768d2e16005ca0a465b53f076c64c6a30f31b8739113954ccc11959c8e0c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028799"
---
# <a name="windows-components-installed-on-demand"></a>Windows componenti installati su richiesta

## <a name="platform"></a>Piattaforma

**Client -** Windows 8.1  







## <a name="description"></a>Descrizione

Due Windows componenti verranno installati su richiesta in Windows 8.1: DirectPlay e NTVDM. Questi componenti sono elencati in Componenti facoltativi nel nodo "Componenti legacy". Questi componenti vengono installati in locale come parte del sistema operativo e compressi come componenti facoltativi. Quando un'app fa riferimento o chiama uno di questi componenti (in genere al primo avvio dell'app), l'installazione viene attivata automaticamente. Gli utenti riceveranno una notifica che il componente verrà installato e devono confermare l'azione per continuare. L'elevazione dei privilegi è necessaria se l'utente non è un amministratore. Dopo l'installazione iniziale, l'utente non deve eseguire altre azioni per usare nuovamente il componente.

## <a name="manifestation"></a>Manifestazione

Quando un'app fa riferimento o chiama un componente legacy nei componenti facoltativi (al primo avvio), l'app verrà sospesa e verrà aperta la finestra di dialogo Funzionalità su richiesta, che richiede l'autorizzazione dell'utente per installare il componente. Se gli utenti fanno clic su OK, è anche possibile che venga visualizzata una richiesta di elevazione dei privilegi in cui devono immettere le credenziali. Il componente verrà quindi installato e l'app verrà ripresa.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Per evitare l'apertura dell'interfaccia utente di Funzionalità su richiesta, è possibile preinstallare DirectPlay e NTVDM usando Gestione e manutenzione immagini distribuzione o l'interfaccia utente dei componenti facoltativi.

## <a name="solution"></a>Soluzione

È consigliabile evitare di fare riferimento o chiamare componenti elencati come componenti facoltativi legacy in Windows nelle versioni future dell'app. I componenti facoltativi legacy includeranno solo componenti meno recenti e meno usati che potrebbero causare problemi di prestazioni e sicurezza per gli utenti.

## <a name="tests"></a>Test

Non sono necessarie altre sistemazioni di test per la compatibilità. È importante tenere presente che questa finestra di dialogo verrà visualizzata quando viene chiamato o fatto riferimento al componente facoltativo e questa installazione richiede l'elevazione dei privilegi.

 

 




