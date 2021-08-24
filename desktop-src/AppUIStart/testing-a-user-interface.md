---
title: Test di un Interfaccia utente
description: Questa sezione descrive in dettaglio alcune delle attività associate al test di un'interfaccia utente per un Windows applizione.
ms.assetid: d628e530-7a0b-4a8d-9a9f-253aec275fa9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17f3d6686cdcd892aa5608944cf8c1a20df0d44106a0fdac01b2bbbd855fe523
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507436"
---
# <a name="testing-a-user-interface"></a>Test di un Interfaccia utente

Questa sezione descrive in dettaglio alcune delle attività associate al test di un'interfaccia utente per un Windows applizione.

-   [Introduzione](#introduction)
-   [Test di usabilità](#usability-testing)
-   [Test di accessibilità](#accessibility-testing)

## <a name="introduction"></a>Introduzione

Per determinare completamente l'efficacia e l'usabilità complessiva di un'interfaccia utente dell'applicazione, è necessario testarla. Il test espone quanto sia facile o difficile l'uso dell'interfaccia utente per il pubblico più ampio possibile. Il tempo necessario per testare un'applicazione è molto importante.

Questo argomento è incentrato su tre scenari di test principali: usabilità generale, accessibilità e automazione.

## <a name="usability-testing"></a>Test di usabilità

I test di usabilità consentono di valutare un prodotto valutando il modo in cui gli utenti reali usano effettivamente il prodotto. Questa analisi garantisce che i presupposti chiave relativi agli utenti designati e alle progettazioni di interfacce siano supportati (o contestati) con dati reali. Solo raccogliendo questi dati empirici è possibile scoprire quanto sia adatta l'interfaccia utente per un prodotto alle esigenze e alle aspettative degli utenti.

Osservando l'interazione dell'utente con il prodotto e l'ascolto dei commenti e suggerimenti degli utenti, vengono identificate funzionalità importanti che potrebbero essere difficili da trovare e usare. In base a questi risultati, è possibile apportare modifiche all'interfaccia utente in base alle esigenze. È quasi impossibile creare un prodotto utile senza un certo livello di test di usabilità, perché i risultati forniscono la base per prendere decisioni migliori sul prodotto e migliorare l'esperienza utente complessiva.

I test di usabilità forniscono un notevole miglioramento solo quando è ben integrato nell'intero ciclo di vita del progetto. Un singolo studio sull'usabilità può identificare i problemi, ma senza test di follow-up è difficile determinare se le soluzioni hanno risolto tali problemi o ne sono state introdotte di nuove.

Gli scenari principali per i test di usabilità sono:

-   Se si è un fornitore di prodotti software, testare gli utenti reali del prodotto significa valutare la progettazione. In base a come è stata progettata l'applicazione, gli utenti possono completare le attività necessarie? Il test di utenti reali che eserviranno attività reali può anche far capire se le linee guida dell'interfaccia utente che si stanno seguendo funzionano nel contesto del prodotto e quando la coerenza consente o impedisce a un utente di eseguire il proprio lavoro.
-   Gli acquirenti di prodotti software possono eseguire test di usabilità per valutare un prodotto per l'acquisto. Ad esempio, l'azienda potrebbe prendere in considerazione l'acquisto di un prodotto per i suoi ventimila dipendenti. Prima che l'azienda spenda i propri denaro, vuole assicurarsi che il prodotto in questione sia effettivamente utile ai dipendenti per migliorare il proprio lavoro. I test di usabilità possono essere utili anche per verificare se l'applicazione proposta segue le linee guida di stile dell'interfaccia utente pubblicate (interne o esterne). È meglio usare le linee guida dell'interfaccia utente come fonte ausiliaria, anziché primaria, di informazioni per prendere decisioni di acquisto.

Per altre informazioni, vedere [Usabilità nella pratica: test di usabilità.](/archive/msdn-magazine/2009/brownfield/usability-in-practice-usability-testing)

## <a name="accessibility-testing"></a>Test di accessibilità

I test di accessibilità comprendono due aree di progettazione dell'interfaccia utente: il supporto per gli utenti con disabilità e l'accesso a livello di codice da parte di framework di test automatizzati.

Assicurarsi che un'applicazione sia accessibile agli utenti con disabilità comporta il test per:

-   Conformità: l'applicazione è conforme a vari requisiti legali relativi all'accessibilità?
-   Efficacia: gli utenti con disabilità possono usare l'applicazione?
-   Utilità: l'applicazione espone funzionalità adeguate per gli utenti con disabilità?
-   Soddisfazione: come viene percepita l'applicazione dagli utenti con disabilità?

Il test di questi aspetti di un'applicazione può essere realizzato tramite un controllo di accessibilità, che prevede una revisione manuale dell'applicazione da parte di un esperto di accessibilità e uno studio mirato sull'usabilità di utenti disabilitati e dispositivi assistive technology.

Anche se apparentemente non correlato, esiste una stretta correlazione tra i requisiti di accesso a livello di codice dei framework di test automatizzati e quelli dei assistive technology dispositivi. Il supporto di uno ha il vantaggio di abilitare l'altro. Per altre informazioni sull'accessibilità e sull'automazione dei [](/windows/desktop/WinAuto/testing-tools)test nelle applicazioni Windows, vedere Accessibilità [,](/windows/desktop/accessibility)Strumenti di test e l'API [Windows Automation](/windows/desktop/WinAuto/windows-automation-api-portal).

 

 