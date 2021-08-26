---
description: Una delle principali funzionalità delle funzioni nell'API di stampa GDI è il supporto dell'indipendenza dei dispositivi.
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: Informazioni sull'API di stampa GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3aa7ea0ecfdd96237fb330868ddf2d9619aa24ee0d2f27a940c789a581a6c8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951011"
---
# <a name="about-the-gdi-print-api"></a>Informazioni sull'API di stampa GDI

Una delle principali funzionalità delle funzioni nell'API di stampa GDI è il supporto dell'indipendenza dei dispositivi. Anziché eseguire comandi specifici del dispositivo per disegnare l'output su una stampante o un tracciatore specifico, un'applicazione chiama funzioni di alto livello dall'interfaccia GDI (Graphics Device Interface). Ad esempio, per stampare un'immagine bitmap, un'applicazione può chiamare la funzione [**BitBlt,**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) fornendo le coordinate per la bitmap e gestisce l'identificazione dei contesti di dispositivo di origine e di destinazione. La chiamata a **BitBlt** viene quindi convertita in comandi di dispositivo non elaborati da un driver della stampante. Un driver di dispositivo è una libreria a collegamento dinamico (DLL) che supporta l'interfaccia DDI (Device Driver Interface). Un driver di dispositivo genera comandi di dispositivo non elaborati quando elabora le chiamate alle funzioni DDI effettuate dal motore di grafica. I comandi vengono elaborati dalla stampante quando stampa l'immagine. La sintassi, il numero e il tipo di questi comandi variano da dispositivo a dispositivo.

Questa panoramica fornisce informazioni sugli argomenti seguenti.

<dl>

[Interfaccia di stampa predefinita](default-printing-interface.md)  
[Contesti di dispositivo della stampante](printer-output.md)  
[Escape della stampante](printer-escapes.md)  
[Visualizzazione e output WYSIWYG](wysiwyg-display-and-output.md)  
[DEVMODE per utente](per-user-devmode.md)  
</dl>

 

 
