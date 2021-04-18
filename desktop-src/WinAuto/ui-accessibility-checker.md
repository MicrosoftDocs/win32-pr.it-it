---
title: Strumenti di accessibilità-AccChecker (controllo di accessibilità dell'interfaccia utente)
description: Descrive AccChecker (controllo dell'accessibilità dell'interfaccia utente), uno strumento per testare l'automazione interfaccia utente di un'applicazione o l'implementazione di Microsoft Active Accessibility (MSAA).
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- Strumento di verifica dell'accessibilità dell'interfaccia utente
- AccChecker
- Implementazione di automazione interfaccia utente, test
- Implementazione di UIA, test
- Implementazione di Microsoft Active Accessibility, test
- Implementazione di MSAA, test
- test di automazione interfaccia utente
- test di UIA
- test di Microsoft Active Accessibility
- test di MSAA
- Strumenti di test di UIA
- Strumenti di test di automazione interfaccia utente
- Strumenti di test MSAA
- Strumenti di test di Microsoft Active Accessibility
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d2b85436735bfa08f8fc73cf4e465b11d71630
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "106299467"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a>Strumenti di accessibilità-AccChecker (controllo di accessibilità dell'interfaccia utente)

**AccChecker** (UI Accessibility Checker) verifica che i requisiti di accessibilità dell'interfaccia utente chiave siano soddisfatti nella progettazione e nell'implementazione di automazione interfaccia utente (UIA) o Microsoft Active ACCESSIBILITY (MSAA) indipendentemente dal framework dell'interfaccia utente sottostante. **AccChecker** include anche un set di verifiche di accessibilità Web.

**AccChecker** offre i seguenti livelli di funzionalità:

- Applicazione GUI Windows che supporta il test manuale, la registrazione di messaggi e la generazione dell'eliminazione.
- API da usare nei framework di test automatizzati.
- Applicazione console che supporta le automazioni di test non gestite per gli scenari in cui non è possibile usare l'API gestita **AccChecker** .

Tutti i livelli di funzionalità di **AccChecker** forniscono routine per la verifica dell'accesso a livello di codice di Microsoft Active Accessibility, della generazione di eventi a livello di codice, del layout di controllo e della navigazione **AccChecker** fornisce anche un servizio di trascrizione di base per la lettura dello schermo.

**AccChecker** viene installato con Windows Software Development Kit (SDK). Si trova nella \\ cartella bin \\ < *versione* > \\ <  > \\ della piattaforma AccChecker del percorso di installazione di SDK.

> [!NOTE]
> **AccChecker** è uno strumento legacy. È invece consigliabile usare [informazioni dettagliate sull'accessibilità](https://accessibilityinsights.io/) .

## <a name="requirements"></a>Requisiti

Richiede .NET Framework 2,0 o versione successiva.

**AccChecker** può essere usato per esaminare i dati di accessibilità nei sistemi che non dispongono di automazione interfaccia utente Microsoft, ma è possibile esaminare solo le proprietà di Microsoft Active Accessibility. Per esaminare l'automazione dell'interfaccia utente, è necessario che l'automazione interfaccia utente sia presente nel sistema. Per ulteriori informazioni, vedere la sezione "requisiti" di [automazione interfaccia utente](entry-uiauto-win32.md).

**AccChecker** viene installato come parte del set di strumenti completo in Windows SDK, ma non viene distribuito come download di exe separato. Il Windows SDK include tutti gli strumenti correlati all'accessibilità descritti in questa sezione. [Ottenere il Windows SDK.](https://developer.microsoft.com/) È anche disponibile un archivio di download dell'SDK collegato da tale pagina, se è necessaria una versione precedente.

## <a name="related-topics"></a>Argomenti correlati

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Controllare](inspect-objects.md)
- [Strumenti di test](testing-tools.md)
- [Verifica dell'automazione dell'interfaccia utente](ui-automation-verify.md)
