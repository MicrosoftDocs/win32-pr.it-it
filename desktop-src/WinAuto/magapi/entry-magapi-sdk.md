---
title: API Magnification
description: L'API di ingrandimento consente alle applicazioni di ingrandire l'intero schermo o parti dello schermo e di applicare gli effetti dei colori.
ms.assetid: 644af100-82ec-4450-b809-cede9b388cb4
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 7e6c652c2cca8e3c5675b390e93b70ad0b522a44
ms.sourcegitcommit: 541c08d5d36109b754f39bf89e57404f007c5f63
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/08/2020
ms.locfileid: "103857974"
---
# <a name="magnification-api"></a>API Magnification

## <a name="purpose"></a>Scopo

L'API di ingrandimento consente alle applicazioni di ingrandire l'intero schermo o parti dello schermo e di applicare gli effetti dei colori.

## <a name="where-applicable"></a>Se applicabile

Utilizzando l'API di ingrandimento, gli sviluppatori possono creare applicazioni per la tecnologia per l'accessibilità basate su Windows che ingrandiscono lo schermo e applicano effetti cromatici al contenuto della schermata ingrandita. Per gli utenti con ipovisione, le dimensioni delle immagini ingrandite e gli effetti dei colori consentono di semplificare la visualizzazione e l'utilizzo del computer.

## <a name="developer-audience"></a>Sviluppatori

L'API di ingrandimento è progettata principalmente per gli sviluppatori C e C++ che conoscono la programmazione Windows e conoscono i concetti di programmazione della grafica.

## <a name="run-time-requirements"></a>Requisiti di runtime

La versione iniziale dell'API di ingrandimento è supportata in Windows Vista e nei sistemi operativi successivi. Una seconda versione aggiunge funzionalità di ingrandimento a schermo intero ed è supportata in Windows 8 e versioni successive.

L'API è supportata da Magnification.dll. Per compilare l'applicazione, includere ingrandimento. h e collegamento a ingrandimento. lib.

> [!Note]  
> L'API di ingrandimento non è supportata in WOW64; ovvero, un'applicazione di Magnifier a 32 bit non verrà eseguita correttamente in Windows a 64 bit.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|:---|:---|
| [Panoramica dell'API di ingrandimento](magapi-intro.md)<br/> | Questo argomento descrive l'API di ingrandimento e spiega come usarlo in un'applicazione.<br/> |
| [Riferimento](entry-magapi-ref.md)<br/>  | Questa sezione contiene informazioni di riferimento per l'API di ingrandimento.<br/>|
| [Esempi](magapi-samples-entry.md)<br/> | Nell'applicazione di esempio seguente viene illustrato come utilizzare l'API di ingrandimento per creare una lente di ingrandimento a schermo intero che consente di ingrandire l'intero schermo e una lente di ingrandimento a finestra che ingrandisce e visualizza una parte della schermata in una finestra.<br/> |

## <a name="related-topics"></a>Argomenti correlati

[Sito Web Microsoft Accessibility](https://www.microsoft.com/accessibility/), [accessibilità in Windows 10](/windows/apps/accessibility)
