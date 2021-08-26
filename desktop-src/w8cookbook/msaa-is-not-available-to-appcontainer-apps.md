---
title: MsAA non è disponibile per le app Windows Store
description: MsAA non è disponibile per le app Windows Store
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eabfd0f855cc4d3940a68fd18e69c4ca2a93774ccdbd0fb1868d2f8f489abea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935081"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a>MsAA non è disponibile per le app Windows Store

## <a name="platform"></a>Piattaforma

**Client** : Windows 8 


## <a name="description"></a>Descrizione

Windows 8 non supporta MSAA (Microsoft Active Accessibility) per la lettura o l'automazione dei dati accessibili dalle app Windows Store. È Automazione interfaccia utente usare invece l'API di Windows (UIA), disponibile a partire da Windows 7. Poiché non sono presenti funzionalità Windows app dello Store, non sono presenti implementazioni esistenti interessate da questa modifica. Questo influisce solo sulle nuove app e funzionalità scritte per Windows 8. Gli sviluppatori possono comunque usare MSAA per esporre i dati di accessibilità. Se i dati MSAA vengono forniti dal provider di app Windows Store, i client con accesso all'interfaccia utente saranno comunque in grado di leggere e automatizzare i dati.

Per semplificare l'API per Windows 8App di Windows Store, è stato deciso di supportare solo Automazione interfaccia utente come client per queste app. I client con accesso all'interfaccia utente possono leggere i provider di automazione interfaccia utente in modo nativo, senza conversione. I client con accesso all'interfaccia utente possono leggere i provider MSAA tradotti tramite il proxy da interfaccia utente a msaa. In questo modo si riduce il carico di test per Windows sviluppatori di app dello Store.

L'eliminazione del supporto per i provider MSAA ridurrebbe ulteriormente la matrice di test, ma esistono app principali ancora basate su MSAA e non si vuole renderle inaccessibili.

## <a name="manifestation"></a>Manifestazione

Windows Gli sviluppatori di app dello Store non saranno in grado di accedere ai dettagli di MSAA all'interno del modello di app.

## <a name="solution"></a>Soluzione

Non è necessario creare nuovi casi automatizzati in MSAA per le funzionalità delle Windows Store.

Passare da uno strumento all'altro esistente che usa MSAA all'interfaccia utente se è necessario interagire con Windows Store. Windows Gli sviluppatori di app dello Store devono usare l Automazione interfaccia utente API.

## <a name="resources"></a>Risorse

-   [Nozioni fondamentali sull'automazione interfaccia utente](../winauto/entry-uiauto-win32.md)

 

 