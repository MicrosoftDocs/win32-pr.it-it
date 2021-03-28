---
description: Windows GDI+ è il sottosistema del sistema operativo Windows XP o Windows Server 2003 responsabile della visualizzazione di informazioni su schermate e stampanti. GDI+ è un'API esposta tramite un set di classi C++.
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: Panoramica di GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb6eb3885d33ad332ac61454525367788d7aed56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994189"
---
# <a name="overview-of-gdi"></a>Panoramica di GDI+

Windows GDI+ è il sottosistema del sistema operativo Windows XP o Windows Server 2003 responsabile della visualizzazione di informazioni su schermate e stampanti. GDI+ è un'API esposta tramite un set di classi C++.

Come suggerisce il nome, GDI+ è il successore di Windows Graphics Device Interface (GDI), l'interfaccia del dispositivo di grafica inclusa nelle versioni precedenti di Windows. Windows XP o Windows Server 2003 supporta GDI per la compatibilità con le applicazioni esistenti, ma i programmatori delle nuove applicazioni devono usare GDI+ per tutte le proprie esigenze grafiche, perché GDI+ ottimizza molte delle funzionalità di GDI e fornisce anche funzionalità aggiuntive.

Un'interfaccia del dispositivo grafica, ad esempio GDI+, consente ai programmatori di applicazioni di visualizzare informazioni su uno schermo o una stampante senza doversi preoccupare dei dettagli di un particolare dispositivo di visualizzazione. Il programmatore di applicazioni effettua chiamate ai metodi forniti dalle classi GDI+ e tali metodi a loro volta effettuano chiamate appropriate a driver di dispositivo specifici. GDI+ isola l'applicazione dall'hardware grafico ed è questo isolamento che consente agli sviluppatori di creare applicazioni indipendenti dal dispositivo.

 

 



