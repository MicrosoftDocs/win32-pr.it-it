---
title: Componenti di Windows installati su richiesta
description: Componenti di Windows installati su richiesta
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d2c3c3fee1cd12d7b12900e41dc006badcf53f
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104047492"
---
# <a name="windows-components-installed-on-demand"></a>Componenti di Windows installati su richiesta

## <a name="platform"></a>Piattaforma

**Client-** Windows 8.1  







## <a name="description"></a>Descrizione

Due componenti di Windows verranno installati su richiesta in Windows 8.1: DirectPlay e NTVDM. Questi componenti sono elencati all'interno dei componenti facoltativi nel nodo "componenti legacy". Questi componenti vengono installati localmente come parte del sistema operativo e compressi come componenti facoltativi. Quando un'app fa riferimento a o chiama uno di questi componenti (in genere al primo avvio dell'app), l'installazione viene attivata automaticamente. Gli utenti riceveranno una notifica che indica che il componente verrà installato e dovranno confermare l'azione per continuare. Per avere esito positivo, l'elevazione è necessaria se l'utente non è un amministratore. Dopo l'installazione iniziale, l'utente non deve eseguire altre azioni per riutilizzare il componente.

## <a name="manifestation"></a>Manifestazione

Quando un'app fa riferimento o chiama un componente legacy in componenti facoltativi (al primo avvio), l'app verrà sospesa e verrà visualizzata la finestra di dialogo funzionalità su richiesta, che richiede l'autorizzazione utente per installare il componente. Se gli utenti fanno clic su OK, è possibile che venga visualizzata una richiesta di elevazione dei privilegi in cui devono immettere le proprie credenziali. Il componente verrà quindi installato e l'app verrà ripresa.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Per impedire l'apertura dell'interfaccia utente su richiesta delle funzionalità, è possibile pre-installare DirectPlay e NTVDM utilizzando DISM o l'interfaccia utente dei componenti facoltativi.

## <a name="solution"></a>Soluzione

Si consiglia di evitare di fare riferimento o chiamare componenti che sono stati elencati come componenti facoltativi legacy in Windows nelle versioni future dell'app. I componenti facoltativi legacy includeranno solo componenti meno recenti e meno utilizzati che potrebbero causare problemi di prestazioni e sicurezza per gli utenti.

## <a name="tests"></a>Test

Non sono necessarie ulteriori soluzioni di test per la compatibilità. È importante tenere presente che questa finestra di dialogo verrà visualizzata quando il componente facoltativo viene chiamato o a cui viene fatto riferimento e questa installazione richiede l'elevazione dei privilegi.

 

 




