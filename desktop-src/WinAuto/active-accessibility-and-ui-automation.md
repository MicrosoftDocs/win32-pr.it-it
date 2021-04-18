---
title: Active Accessibility e automazione interfaccia utente
description: Microsoft Active Accessibility è progettato per l'utilizzo con Windows XP e i sistemi operativi precedenti.
ms.assetid: 8eb36d2c-0c2f-4311-8690-52ce070c9f33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2483f4f6679926ef2f87c380d4ac0febcc88652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298879"
---
# <a name="active-accessibility-and-ui-automation"></a>Active Accessibility e automazione interfaccia utente

Microsoft Active Accessibility è progettato per l'utilizzo con Windows XP e i sistemi operativi precedenti. Gli sviluppatori di controlli personalizzati e di applicazioni client tecnologiche accessibili per Windows XP e Windows Vista dovrebbero prendere in considerazione l'uso di [automazione interfaccia utente](entry-uiauto-win32.md) Microsoft.

Automazione interfaccia utente Microsoft è un sistema completo che fornisce informazioni più precise sull'interfaccia utente e offre all'utente la possibilità di interagire con i controlli. In particolare, fornisce un supporto migliorato per il testo.

Un set di oggetti proxy fornisce supporto per l'automazione dell'interfaccia utente per i controlli standard di Microsoft Win32 e Windows Form. È disponibile un supporto più completo per i controlli specificamente scritti con l'automazione dell'interfaccia utente, inclusi gli elementi Windows Presentation Foundation nativi (WPF), che non supportano direttamente Microsoft Active Accessibility. I controlli personalizzati che supportano l'automazione dell'interfaccia utente possono essere scritti in codice gestito o non gestito.

I client Microsoft Active Accessibility hanno accesso limitato, tramite un livello di bridging, agli elementi dell'interfaccia utente che supportano solo l'automazione dell'interfaccia utente. Per ulteriori informazioni, vedere [Appendice G: Active Accessibility Bridge per l'automazione interfaccia utente](appendix-g--active-accessibility-bridge-to-ui-automation.md).

Per ulteriori informazioni sulle analogie e le differenze tra Active Accessibility Microsoft e l'automazione dell'interfaccia utente, vedere [confronto tra microsoft Active Accessibility e automazione interfaccia utente](microsoft-active-accessibility-and-ui-automation-compared.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Per iniziare](getting-started.md)
</dt> <dt>

[Automazione interfaccia utente](entry-uiauto-win32.md)
</dt> </dl>

 

 




