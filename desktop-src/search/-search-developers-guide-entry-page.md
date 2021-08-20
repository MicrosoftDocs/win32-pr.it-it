---
description: Terze parti possono creare applicazioni che esetendono i dati nell'indice a livello di codice e possono estendere Windows ricerca per indicizzare i dati da formati di file personalizzati e archivi dati.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Windows Guida per gli sviluppatori di ricerca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84773f23f5e82ce5cbb15c163b0ff2421f9b7c92b18129c9875729be37518b02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117864190"
---
# <a name="windows-search-developers-guide"></a>Windows Guida per gli sviluppatori di ricerca

Terze parti possono creare applicazioni che esetendono i dati nell'indice a livello di codice e possono estendere Windows ricerca per indicizzare i dati da formati di file personalizzati e archivi dati. Per creare Windows applicazioni di ricerca, gli sviluppatori di terze parti devono prima implementare un archivio dati shell per ottenere un'esperienza utente ragionevole. Per altre informazioni, vedere [Implementazione delle interfacce dell'oggetto cartella di base](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

È anche necessario scaricare [l'SDK Windows per](https://msdn.microsoft.com/windowsvista/bb980924.aspx) le librerie Windows ricerca. Gli [Windows sdk di ricerca contengono](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) esempi di codice utili e un assembly di interoperabilità per lo sviluppo con codice gestito. Per altre informazioni sull'uso degli esempi di codice, [Windows esempi di codice di ricerca](-search-3x-wds-sampleentry.md).

Questa sezione è organizzata come segue:

- [Gestione dell'indice](-search-3x-wds-mngidx-overview.md)
- [Esecuzione di query sull'indice a livello di codice](-search-3x-wds-qryidx-overview.md)
- [Estensione dell'indice](-search-3x-wds-extidx-overview.md)
- [Estensione delle risorse del linguaggio](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a>Risorse aggiuntive

- Per le bacheche per domande e discussioni supportate dalla community sulle tecnologie di ricerca, vedere [forum MSDN: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).
- Per scaricare gli esempi di codice di ricerca:
  - [Windows Esempi di ricerca](-search-samples-ovw.md)
- Per scaricare Windows SDK:
  - Per Windows 10: [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)
  - Per Windows 7: [Windows SDK per Windows 7 e .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

## <a name="related-topics"></a>Argomenti correlati

[Panoramica di Windows Search](-search-3x-wds-overview.md)

[Windows Informazioni di riferimento sulla ricerca](-search-reference-entry-page.md)

[Windows Esempi di codice di ricerca](-search-samples-ovw.md)

[Ricerca federata in Windows](-search-federated-search-overview.md)

[Tecnologie di ricerca correlate](-search-3x-wds-sampleentry.md)

[Windows Glossario di ricerca](search-glossary.md)
