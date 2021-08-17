---
title: Novità (controlli Windows)
description: In questo argomento vengono descritte le differenze nel supporto per stili di visualizzazione e tema tra Windows 8 e le versioni precedenti di Windows .
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7801eea011aabb05663cc2e29f18e0dd58edc9fddc4f32014fcffb96c559cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957550"
---
# <a name="whats-new-windows-controls"></a>Novità (controlli Windows)

In questo argomento vengono descritte le differenze nel supporto per stili di visualizzazione e tema tra Windows 8 e le versioni precedenti di Windows .

## <a name="through-windows-7"></a>Fino Windows 7

Tramite Windows 7, gli stili di visualizzazione sono attivati per impostazione predefinita, ma l'utente può disattivarli selezionando il tema classico Windows o disattivando il servizio Temi. Quando gli stili di visualizzazione sono disattivati, tutta l'interfaccia utente ottiene l'aspetto classico e la maggior parte delle API degli stili di visualizzazione non è disponibile. Gli stili di visualizzazione disattivati sono stati mantenuti Windows 7 per supportare i vari temi a contrasto elevato, nonché Windows tema classico. Se si vuole supportare sia gli stili di visualizzazione che i temi a contrasto elevato nella stessa applicazione, in genere è necessario mantenere due percorsi di codice separati per i controlli di rendering.

## <a name="windows-8-and-later"></a>Windows 8 e versioni successive

In Windows 8 gli stili di visualizzazione non possono  essere disattivati tramite la pagina Personalizzazione del **pc** Impostazioni o disattivando il servizio Temi. Windows La modalità classica non esiste più e la modalità a contrasto elevato è stata modificata per funzionare con gli stili di visualizzazione. A causa di queste modifiche, le applicazioni che hanno come destinazione Windows 8 non necessitano più di due percorsi di codice separati per supportare gli stili di visualizzazione e i temi a contrasto elevato.

Gli stili di visualizzazione in Windows 8 supportano la compatibilità con le versioni precedenti Windows modalità tema classica. Qualsiasi codice di rendering dell'interfaccia utente che funziona nelle versioni precedenti continuerà a funzionare Windows 8 senza modifiche.

In Windows 8, se si vuole che l'applicazione supporti i temi a contrasto elevato basati su stili di visualizzazione, è necessario includere il GUID di Windows 8 nella sezione di compatibilità del manifesto dell'applicazione. In caso contrario, il sistema presuppone che l'applicazione sia progettata per una versione precedente ed esegue il rendering dell'area client simulando Windows classici a contrasto elevato. Per altre informazioni, vedere [Supporto dei Contrasto elevato .](supporting-high-contrast-themes.md)

Come nelle versioni precedenti, Windows 8 supporta sia la versione 5 che la versione 6 dei controlli comuni, con la versione 5 come predefinita. Poiché solo la versione 6 supporta gli stili di visualizzazione, è necessario specificare la versione 6 nel manifesto dell'applicazione se si vuole che gli stili di visualizzazione siano applicati ai controlli comuni nell'area client dell'applicazione. Per altre informazioni, vedere [Abilitazione degli stili di visualizzazione.](cookbook-overview.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Abilitazione degli stili di visualizzazione](cookbook-overview.md)
</dt> <dt>

[Supporto dei Contrasto elevato personalizzati](supporting-high-contrast-themes.md)
</dt> <dt>

[Stili di visualizzazione](themes-overview.md)
</dt> <dt>

[Panoramica degli stili di visualizzazione](visual-styles-overview.md)
</dt> </dl>

 

 




