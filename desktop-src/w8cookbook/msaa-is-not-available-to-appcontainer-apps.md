---
title: MSAA non è disponibile per le app di Windows Store
description: MSAA non è disponibile per le app di Windows Store
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e9c1221850b1fa97a3a0d5fcef119c21277486
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104047497"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a>MSAA non è disponibile per le app di Windows Store

## <a name="platform"></a>Piattaforma

**Client** -Windows 8 


## <a name="description"></a>Descrizione

Windows 8 non supporta MSAA (Microsoft Active Accessibility) per la lettura o l'automazione dei dati accessibili dalle app di Windows Store. È consigliabile usare l'API di automazione interfaccia utente (UIA), disponibile a partire da Windows 7. Poiché non sono presenti funzionalità di app di Windows Store, non sono presenti implementazioni che sono interessate da questa modifica. Questa operazione ha effetto solo sulle nuove app e funzionalità scritte per Windows 8. Gli sviluppatori possono comunque utilizzare MSAA per esporre i propri dati di accessibilità. Se i dati MSAA sono forniti dal provider di app di Windows Store, i client di UIA saranno comunque in grado di leggere e automatizzare i dati.

Per semplificare l'API per le app di Windows Store 8Windows, abbiamo deciso di supportare solo l'automazione dell'interfaccia utente come client per queste app. I client di UIA possono leggere i provider UIA in modo nativo, senza alcuna conversione. I client di UIA possono leggere i provider MSAA come tradotti tramite il proxy UIA-to-MSAA. Questo consente di ridurre il carico di test per gli sviluppatori di app di Windows Store.

L'eliminazione del supporto per i provider MSAA ridurrebbe ulteriormente la matrice di test, ma sono presenti app principali ancora basate su MSAA e non si desidera renderle inaccessibili.

## <a name="manifestation"></a>Manifestazione

Gli sviluppatori di app di Windows Store non saranno in grado di accedere ai dettagli di MSAA all'interno del modello di app.

## <a name="solution"></a>Soluzione

Non è necessario creare nuovi casi automatizzati in MSAA per le funzionalità delle app di Windows Store.

Se è necessario interagire con le app di Windows Store, è possibile cambiare tutti gli strumenti predefiniti esistenti che usano MSAA in UIA. Gli sviluppatori di app di Windows Store devono usare l'API di automazione interfaccia utente.

## <a name="resources"></a>Risorse

-   [Nozioni fondamentali sull'automazione interfaccia utente](../winauto/entry-uiauto-win32.md)

 

 