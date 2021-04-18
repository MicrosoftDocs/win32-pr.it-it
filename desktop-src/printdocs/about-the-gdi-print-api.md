---
description: Una delle funzionalità principali delle funzioni nell'API di stampa GDI è il supporto dell'indipendenza del dispositivo.
ms.assetid: 3efcc6d0-14f0-4605-9603-ccc7ad0cc895
title: Informazioni sull'API di stampa GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e6e8a34552a1198ebe618f463003fe28ded6aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316429"
---
# <a name="about-the-gdi-print-api"></a>Informazioni sull'API di stampa GDI

Una delle funzionalità principali delle funzioni nell'API di stampa GDI è il supporto dell'indipendenza del dispositivo. Anziché emettere comandi specifici del dispositivo per tracciare l'output su una stampante o un plotter particolare, un'applicazione chiama funzioni di alto livello dall'interfaccia GDI (Graphics Device Interface). Per stampare un'immagine bitmap, ad esempio, un'applicazione può chiamare la funzione [**BitBlt**](/windows/desktop/api/wingdi/nf-wingdi-bitblt) , fornendo le coordinate per la bitmap, nonché gli handle che identificano i contesti di dispositivo di origine e di destinazione. La chiamata a **BitBlt** viene quindi convertita in comandi di dispositivo RAW da parte di un driver della stampante. Un driver di dispositivo è una libreria di collegamento dinamico (DLL) che supporta l'interfaccia DDI (Device Driver Interface). Un driver di dispositivo genera comandi per i dispositivi non elaborati quando elabora le chiamate alle funzioni DDI eseguite dal motore di grafica. I comandi vengono elaborati dalla stampante quando viene stampata l'immagine. La sintassi, il numero e il tipo di questi comandi variano da dispositivo a dispositivo.

In questa panoramica vengono fornite informazioni sui seguenti argomenti.

<dl>

[Interfaccia di stampa predefinita](default-printing-interface.md)  
[Contesti di dispositivo stampante](printer-output.md)  
[Caratteri di escape della stampante](printer-escapes.md)  
[Visualizzazione e output WYSIWYG](wysiwyg-display-and-output.md)  
[DEVMODE per utente](per-user-devmode.md)  
</dl>

 

 
