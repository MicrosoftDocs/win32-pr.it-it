---
description: Sono disponibili sette pennelli logici predefiniti gestiti dall'interfaccia GDI (Graphics Device Interface). Sono presenti anche 21 pennelli logici predefiniti gestiti dall'interfaccia di gestione della finestra (USER).
ms.assetid: ddbc6d54-47f6-4810-9d3a-feede80f2bed
title: Pennello azionario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522337752c2d81a92302d4a6a8f025393db1ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980527"
---
# <a name="stock-brush"></a>Pennello azionario

Sono disponibili sette pennelli logici predefiniti gestiti dall'interfaccia GDI (Graphics Device Interface). Sono presenti anche 21 pennelli logici predefiniti gestiti dall'interfaccia di gestione della finestra (USER).

Nella figura seguente sono illustrati i rettangoli disegnati usando i sette pennelli predefiniti.

![illustrazione che mostra sette caselle: una nera, tre tonalità di grigio e tre che risultano vuote](images/csbru-03.png)

Un'applicazione può recuperare un handle che identifica uno dei sette pennelli azionari chiamando la funzione [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) , specificando il tipo di pennello.

I 21 pennelli azionari gestiti dall'interfaccia di gestione della finestra corrispondono ai colori degli elementi della finestra quali menu, barre di scorrimento e pulsanti. Un'applicazione può ottenere un handle che identifica uno di questi pennelli chiamando la funzione [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) e specificando un valore di colore di sistema. Un'applicazione può recuperare il colore corrispondente a un particolare elemento della finestra chiamando la funzione [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) . Un'applicazione può impostare il colore corrispondente a un elemento della finestra chiamando la funzione [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) .

 

 
