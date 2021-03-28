---
description: Tipi di carattere da più file di risorse
ms.assetid: 4625fe62-d55d-4828-9174-975a731a8f62
title: Tipi di carattere da più file di risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3802705ba4b199fa00d2cc2961d3c4472c4e365
ms.sourcegitcommit: fa5c081bf792b119a7bb92182cde1f85ca75967b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/17/2021
ms.locfileid: "104996449"
---
# <a name="fonts-from-multiple-resource-files"></a>Tipi di carattere da più file di risorse

In genere, un tipo di carattere è contenuto in un singolo file di risorse del tipo di carattere. Tuttavia, le informazioni relative ad alcuni tipi di carattere vengono distribuite tra diversi file. Ad esempio, digitare 1 più tipi di carattere Master richiedono due file:

-   . PFM per le metriche dei tipi di carattere
-   . PFB per i bit del carattere

Per aggiungere un tipo di carattere da più file al sistema, usare le funzioni [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) o [**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) . Il parametro *lpszFileName* in queste funzioni deve puntare a una stringa che contiene i nomi file separati dalla barra verticale o dalla pipe ( \| ). Per specificare, ad esempio, abcxxxxx. PFM e abcxxxxx. PFB per un tipo di carattere 1, utilizzare la stringa "abcxxxxx. PFM \| abcxxxxx. pfb".

[**AddFontResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) differisce da [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) in quanto l'applicazione che chiama **AddFontResourceEx** può specificare il tipo di carattere come privato o non enumerabile.

Per aggiungere un tipo di carattere da un'immagine di memoria, usare [**AddFontMemResourceEx**](/windows/win32/api/wingdi/nf-wingdi-addfontmemresourceex). Questo consente a un'applicazione di usare un tipo di carattere incorporato in un documento o in una pagina Web.

Per rimuovere un tipo di carattere che proviene da più file di risorse, chiamare [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) o [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa), a seconda della funzione utilizzata per aggiungere il tipo di carattere. È necessario specificare gli stessi flag utilizzati per aggiungere il tipo di carattere. Per rimuovere un tipo di carattere aggiunto da un'immagine di memoria, utilizzare [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex).

L'uso di un tipo di carattere che deriva da più file di risorse del tipo di carattere è identico a quello di un singolo file di risorse.

 

 
