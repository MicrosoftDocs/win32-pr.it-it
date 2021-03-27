---
description: "Le funzioni seguenti consentono a un'applicazione di salvare, ripristinare e reimpostare un contesto di dispositivo: SaveDC, RestoreDC e ResetDC."
ms.assetid: 22837876-2665-49c6-908e-80e107fc09f4
title: Salvataggio, ripristino e reimpostazione di un contesto di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2714360c07f4a4eca354ede5b460864cc897e58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979791"
---
# <a name="saving-restoring-and-resetting-a-device-context"></a>Salvataggio, ripristino e reimpostazione di un contesto di dispositivo

Le funzioni seguenti consentono a un'applicazione di salvare, ripristinare e reimpostare un contesto di dispositivo: [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc), [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)e [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca). La funzione SaveDC registra in uno stack GDI speciale gli oggetti grafici del controller di dominio corrente, i relativi attributi e le modalità grafiche. Un'applicazione di disegno può chiamare questa funzione prima che un utente inizi a disegnare e salvare lo stato originale dell'applicazione fornendo uno Slate pulito per l'utente. Per tornare a questo stato originale, l'applicazione chiama la funzione RestoreDC.

[**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca) viene fornito per reimpostare i dati del controller di dominio della stampante. Un'applicazione chiama questa funzione per reimpostare l'orientamento della carta, il formato della carta, il fattore di scala di output, il numero di copie da stampare, l'origine (o il contenitore) della carta, la modalità duplex e così via. In genere, un'applicazione chiama questa funzione dopo che un utente ha modificato una delle opzioni della stampante e il sistema ha emesso un messaggio [**WM \_ DEVMODECHANGE**](wm-devmodechange.md) .

 

 



