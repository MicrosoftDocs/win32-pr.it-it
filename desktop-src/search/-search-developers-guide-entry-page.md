---
description: Le terze parti possono creare applicazioni che eseguono query sull'indice per i dati a livello di programmazione e possono estendere la ricerca di Windows per indicizzare i dati da formati di file personalizzati e archivi dati.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Guida per gli sviluppatori di Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61593f47e081059966936a99a7d2baea114df92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484444"
---
# <a name="windows-search-developers-guide"></a>Guida per gli sviluppatori di Windows Search

Le terze parti possono creare applicazioni che eseguono query sull'indice per i dati a livello di programmazione e possono estendere la ricerca di Windows per indicizzare i dati da formati di file personalizzati e archivi dati. Per creare applicazioni Windows Search, gli sviluppatori di terze parti devono implementare prima di tutto un archivio dati Shell per ottenere un'esperienza utente ragionevole. Per ulteriori informazioni, vedere [implementazione delle interfacce di oggetti della cartella di base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

È inoltre necessario scaricare il [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) per le librerie di ricerca di Windows. Gli [esempi di Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contengono esempi di codice utili e un assembly di interoperabilità per lo sviluppo con codice gestito. Per ulteriori informazioni sull'utilizzo degli esempi di codice, vedere [esempi di codice di Windows Search](-search-3x-wds-sampleentry.md).

Questa sezione è organizzata nel modo seguente:

- [Gestione dell'indice](-search-3x-wds-mngidx-overview.md)
- [Esecuzione di query sull'indice a livello di codice](-search-3x-wds-qryidx-overview.md)
- [Estensione dell'indice](-search-3x-wds-extidx-overview.md)
- [Estensione delle risorse della lingua](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a>Risorse aggiuntive

- Per le bacheche dei messaggi di discussione e domande supportate dalla community sulle tecnologie di ricerca, vedere il [Forum MSDN relativo allo sviluppo per Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
- Per scaricare gli esempi di codice di ricerca:
  - [Esempi di Windows Search](-search-samples-ovw.md)
- Per scaricare il Windows SDK:
  - Per Windows 10: [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)
  - Per Windows 7: [Windows SDK per Windows 7 e .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

## <a name="related-topics"></a>Argomenti correlati

[Panoramica di Windows Search](-search-3x-wds-overview.md)

[Informazioni di riferimento su Windows Search](-search-reference-entry-page.md)

[Esempi di codice di Windows Search](-search-samples-ovw.md)

[Ricerca federata in Windows](-search-federated-search-overview.md)

[Tecnologie di ricerca correlate](-search-3x-wds-sampleentry.md)

[Glossario di Windows Search](search-glossary.md)
