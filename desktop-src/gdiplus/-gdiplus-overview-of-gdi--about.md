---
description: Windows GDI+ è il sottosistema del sistema operativo Windows XP o di Windows Server 2003 responsabile della visualizzazione di informazioni su schermi e stampanti. GDI+ è un'API esposta tramite un set di classi C++.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Panoramica delle GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ca4eadf9eaf27cbe35103753a49c4bc25d2974ee1051481b0b52787a6602e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830761"
---
# <a name="overview-of-gdi"></a>Panoramica delle GDI+

Windows GDI+ è il sottosistema del sistema operativo Windows XP o di Windows Server 2003 responsabile della visualizzazione di informazioni su schermi e stampanti. GDI+ è un'API esposta tramite un set di classi C++.

Come suggerisce il nome, GDI+ è il successore di Windows Graphics Device Interface (GDI), l'interfaccia del dispositivo grafico inclusa nelle versioni precedenti di Windows. Windows XP o Windows Server 2003 supporta GDI per la compatibilità con le applicazioni esistenti, ma i programmatori di nuove applicazioni devono usare GDI+ per tutte le esigenze grafiche perché GDI+ ottimizza molte delle funzionalità di GDI e fornisce anche funzionalità aggiuntive.

Un'interfaccia di dispositivo grafico, ad esempio GDI+, consente ai programmatori di applicazioni di visualizzare informazioni su uno schermo o su una stampante senza doversi preoccupare dei dettagli di un particolare dispositivo di visualizzazione. Il programmatore dell'applicazione effettua chiamate ai metodi forniti GDI+ classi e tali metodi a loro volta effettuano le chiamate appropriate a driver di dispositivo specifici. GDI+ isola l'applicazione dall'hardware grafico ed è questo isolamento che consente agli sviluppatori di creare applicazioni indipendenti dal dispositivo.

 

 



