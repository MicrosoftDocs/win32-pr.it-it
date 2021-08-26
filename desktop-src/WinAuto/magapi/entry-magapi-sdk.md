---
title: API Magnification
description: L'API Ingrandimento consente alle applicazioni di ingrandire l'intero schermo o parti dello schermo e di applicare effetti di colore.
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 2a6c7a7ffb103b39c506c41b6b7b88f82319685226aff0d479558977caa9d46b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998435"
---
# <a name="magnification-api"></a>API Magnification

## <a name="purpose"></a>Scopo

L'API Ingrandimento consente alle applicazioni di ingrandire l'intero schermo o parti dello schermo e di applicare effetti di colore.

## <a name="where-applicable"></a>Se applicabile

Usando l'API Ingrandimentotion, gli sviluppatori possono creare applicazioni assistive-technology basate su Windows che ingrandiscino lo schermo e applicano effetti di colore al contenuto dello schermo ingrandito. Per gli utenti con problemi di vista, le dimensioni dell'immagine ingrandite e gli effetti di colore possono semplificare la visualizzazione e l'uso del computer.

## <a name="developer-audience"></a>Sviluppatori

L'API Di ingrandimento è progettata principalmente per gli sviluppatori C e C++ che conoscono Windows programmazione grafica e hanno familiarità con i concetti di programmazione grafica.

## <a name="run-time-requirements"></a>Requisiti di runtime

La versione iniziale dell'API Ingrandimentotion è supportata in Windows Vista e nei sistemi operativi successivi. Una seconda versione aggiunge funzionalità di ingrandimento a schermo intero ed è supportata in Windows 8 e versioni successive.

L'API è supportata da Magnification.dll. Per compilare l'applicazione, includere Ingrandimentotion.h e collegarsi a Ingrandimentotion.lib.

> [!Note]  
> L'API Ingrandimentotion non è supportata in WOW64. in altri, un'applicazione lente di ingrandimento a 32 bit non verrà eseguita correttamente in Windows a 64 bit.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|:---|:---|
| [Panoramica dell'API Di ingrandimento](magapi-intro.md)<br/> | Questo argomento descrive l'API Ingrandimentotion e spiega come usarla in un'applicazione.<br/> |
| [Riferimento](entry-magapi-ref.md)<br/>  | Questa sezione contiene informazioni di riferimento per l'API Ingrandimentotion.<br/>|
| [Esempi](magapi-samples-entry.md)<br/> | L'applicazione di esempio seguente illustra come usare l'API Ingrandimento per creare una lente di ingrandimento a schermo intero che ingrandi l'intero schermo e una lente di ingrandimento con finestra che ingrandi e visualizza una parte dello schermo in una finestra.<br/> |

## <a name="related-topics"></a>Argomenti correlati

[Sito Web accessibilità Microsoft](https://www.microsoft.com/accessibility/), [Accessibilità in Windows 10](/windows/apps/accessibility)
