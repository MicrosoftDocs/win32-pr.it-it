---
title: Strumenti di accessibilità - AccChecker (Controllo accessibilità interfaccia utente)
description: Descrive AccChecker (Ui Accessibility Checker), uno strumento per testare l'implementazione Automazione interfaccia utente o Microsoft Active Accessibility (MSAA) di un'applicazione.
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- Strumento di verifica dell'accessibilità dell'interfaccia utente
- AccChecker
- Automazione interfaccia utente, test
- implementazione dell'interfaccia utente, test
- Microsoft Active Accessibility, test
- implementazione MSAA, test
- test Automazione interfaccia utente
- test dell'interfaccia utente
- test Microsoft Active Accessibility
- test di MSAA
- Strumenti di test dell'interfaccia utente
- Automazione interfaccia utente strumenti di test
- Strumenti di test MSAA
- Microsoft Active Accessibility strumenti di test
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 452ff74140b50f1f6ea6d5357187e42ecff2d83cc85076d11ff22e191da7f3ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052409"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a>Strumenti di accessibilità - AccChecker (Controllo accessibilità interfaccia utente)

**AccChecker** (Ui Accessibility Checker) verifica che i requisiti chiave di accessibilità dell'interfaccia utente siano soddisfatti nella progettazione e nell'implementazione di Automazione interfaccia utente (UIA) o Microsoft Active Accessibility (MSAA) indipendentemente dal framework dell'interfaccia utente sottostante. **AccChecker include** anche un set di verifiche dell'accessibilità Web.

**AccChecker** offre i livelli di funzionalità seguenti:

- Un Windows gui che supporta il test manuale, la registrazione dei messaggi e la generazione di eliminazione.
- API da usare nei framework di test automatizzati.
- Applicazione console che supporta automazioni di test non gestite per scenari in cui l'API gestita **AccChecker** non può essere usata.

Tutti i livelli di **funzionalità AccChecker** forniscono routine per verificare l'accesso Microsoft Active Accessibility a livello di codice, la generazione di eventi a livello di codice, il layout di controllo e la navigazione da tastiera. **AccChecker fornisce** anche un servizio di trascrizione dell'utilità per la lettura dello schermo di base.

**AccChecker** viene installato con Windows Software Development Kit (SDK). Si trova nella cartella \\ bin \\ < *version* > \\ < *platform* > \\ AccChecker del percorso di installazione dell'SDK.

> [!NOTE]
> **AccChecker** è uno strumento legacy. In alternativa, è [consigliabile usare Insights](https://accessibilityinsights.io/) accessibilità.

## <a name="requirements"></a>Requisiti

Richiede .NET Framework 2.0 o versione successiva.

**AccChecker può** essere usato per esaminare i dati di accessibilità nei sistemi che non dispongono di Microsoft Automazione interfaccia utente, ma possono solo esaminare le Microsoft Active Accessibility proprietà. Per esaminare Automazione interfaccia utente, Automazione interfaccia utente deve essere presente nel sistema. Per altre informazioni, vedere la sezione "Requisiti" di [Automazione interfaccia utente](entry-uiauto-win32.md).

**AccChecker** viene installato come parte del set complessivo di strumenti in Windows SDK, non viene distribuito come download exe separato. L Windows SDK include tutti gli strumenti correlati all'accessibilità documentati in questa sezione. [Ottenere l Windows SDK.](https://developer.microsoft.com/) È anche disponibile un archivio di download dell'SDK collegato da tale pagina, se è necessaria una versione precedente.

## <a name="related-topics"></a>Argomenti correlati

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Controllare](inspect-objects.md)
- [Strumenti di test](testing-tools.md)
- [Verifica dell'automazione dell'interfaccia utente](ui-automation-verify.md)
