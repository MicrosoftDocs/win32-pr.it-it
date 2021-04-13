---
title: Novità (controlli Windows)
description: In questo argomento vengono descritte le differenze di supporto per gli stili di visualizzazione e di visualizzazione tra Windows 8 e le versioni precedenti di Windows.
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b203152c8fae5b844eeab334870bf8efb04ac20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474819"
---
# <a name="whats-new-windows-controls"></a>Novità (controlli Windows)

In questo argomento vengono descritte le differenze di supporto per gli stili di visualizzazione e di visualizzazione tra Windows 8 e le versioni precedenti di Windows.

## <a name="through-windows-7"></a>Tramite Windows 7

Grazie a Windows 7, gli stili di visualizzazione sono attivati per impostazione predefinita, ma l'utente può disattivarli selezionando il tema classico di Windows o disattivando il servizio temi. Quando gli stili di visualizzazione sono spenti, tutte le interfacce utente ottengono l'aspetto classico e la maggior parte delle API degli stili di visualizzazione non sono disponibili. La modalità di visualizzazione degli stili di visualizzazione è stata mantenuta attraverso Windows 7 per supportare i diversi temi a contrasto elevato, oltre al tema Windows classico. Se si desidera supportare sia gli stili visivi che i temi a contrasto elevato nella stessa applicazione, in genere è necessario mantenere due percorsi di codice distinti per il rendering dei controlli.

## <a name="windows-8-and-later"></a>Windows 8 e versioni successive

In Windows 8 gli stili visivi non possono essere disattivati tramite la pagina **personalizzazione** delle **impostazioni del PC** oppure disattivando il servizio temi. La modalità classica di Windows non esiste più e la modalità a contrasto elevato è stata modificata per funzionare con gli stili di visualizzazione. A causa di queste modifiche, le applicazioni destinate solo a Windows 8 non necessitano più di due percorsi di codice distinti per supportare gli stili visivi e i temi a contrasto elevato.

Gli stili di visualizzazione in Windows 8 includono il supporto per la compatibilità con le versioni precedenti di Windows classico. Qualsiasi codice di rendering dell'interfaccia utente che funziona nelle versioni precedenti continuerà a funzionare in Windows 8 senza modifiche.

In Windows 8, se si desidera che l'applicazione supporti i temi a contrasto elevato basati sugli stili di visualizzazione, è necessario includere il GUID di Windows 8 nella sezione compatibilità del manifesto dell'applicazione. In caso contrario, il sistema presuppone che l'applicazione sia progettata per una versione precedente ed esegua il rendering dell'area client simulando i temi classici a contrasto elevato di Windows. Per ulteriori informazioni, vedere [supporto di contrasto elevato temi](supporting-high-contrast-themes.md).

Come nelle versioni precedenti, Windows 8 supporta sia la versione 5 che la versione 6 dei controlli comuni, con la versione 5 predefinita. Poiché solo la versione 6 supporta gli stili di visualizzazione, è necessario specificare la versione 6 nel manifesto dell'applicazione se si desidera applicare gli stili di visualizzazione ai controlli comuni nell'area client dell'applicazione. Per altre informazioni, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Abilitazione degli stili di visualizzazione](cookbook-overview.md)
</dt> <dt>

[Supporto di Contrasto elevato temi](supporting-high-contrast-themes.md)
</dt> <dt>

[Stili di visualizzazione](themes-overview.md)
</dt> <dt>

[Panoramica degli stili di visualizzazione](visual-styles-overview.md)
</dt> </dl>

 

 




