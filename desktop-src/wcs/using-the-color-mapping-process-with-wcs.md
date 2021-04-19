---
title: Uso del processo di mapping dei colori con WCS
description: Il mapping dei colori WCS è basato sui profili di dispositivo.
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- Sistema colori Windows (WCS), mapping colori
- WCS (sistema di colori Windows), mapping colori
- Gestione colori immagine, mapping colori
- Gestione colori, mapping colori
- colori, mapping colori
- mapping colori
- Windows Color System (WCS), profili di dispositivo
- WCS (sistema di colori Windows), profili di dispositivo
- Gestione colori immagine, profili dispositivo
- gestione dei colori, profili di dispositivo
- colori, profili di dispositivo
- Windows Color System (WCS), profili
- WCS (Windows Color System), profili
- Gestione colori immagine, profili
- gestione dei colori, profili
- colori, profili
- profili di dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 428b09749f3781def44e56ff6cea0539259d0464
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2021
ms.locfileid: "106320133"
---
# <a name="using-the-color-mapping-process-with-wcs"></a>Uso del processo di mapping dei colori con WCS

Il mapping dei colori WCS è basato sui [profili di dispositivo](d.md). Questi vengono forniti dai fornitori di dispositivi hardware a colori e installati durante l'installazione di un dispositivo. Quando il mapping dei colori viene usato da un programma applicativo, WCS accede al profilo del dispositivo dell'immagine per ottenere le informazioni necessarie per convertire l'immagine nei PC. La conversione viene eseguita dal CMM.

Un profilo di dispositivo può essere incorporato nell'immagine stessa. Il profilo del dispositivo si sposta quindi con l'immagine, anche in Internet. Un utente non ha bisogno del dispositivo di origine per ottenere un mapping accurato dei colori. Se un'immagine non ha un profilo di dispositivo, lo spazio sRGB viene usato come valore predefinito. Per ulteriori informazioni, vedere [utilizzo di gestione colori in Internet](using-color-management-on-the-internet.md).

Si noti che le applicazioni che utilizzano WCS non devono mai incorporare il profilo sRGB in un'immagine. Lo spazio dei colori di sRGB fornisce uno spazio di colore standardizzato che è portabile in tutti i dispositivi. È automaticamente disponibile per gli utenti di Windows 98 e versioni successive, nonché per Windows 2000 e versioni successive. Pertanto, non è necessario spostarsi con l'immagine.

Quando i colori dell'immagine si trovano nei [PC](p.md), WCS accede al profilo di dispositivo del dispositivo di destinazione. Ottiene il CMM per convertire i colori dell'immagine dai PC alla gamma del dispositivo di destinazione.

Il mapping dei colori più complesso può essere eseguito anche con WCS. Ad esempio, può essere usato per avere un'idea dell'aspetto di un'immagine creata in uno schermo video quando viene stampata su una stampante laser a risoluzione elevata. L'esempio è più complesso se è presente solo una stampante inkjet standard in cui visualizzarne l'anteprima. È possibile convertire l'immagine dalla gamma dello schermo alla gamma della stampante a getto d'inchiostro. Da qui può essere convertito nella gamma della stampante laser. L'immagine risultante può essere stampata sulla stampante a getto d'inchiostro. Naturalmente, l'immagine potrebbe essere a una risoluzione superiore quando viene stampata sulla stampante laser con colori. Tuttavia, i colori dell'immagine di correzione stampata sulla stampante inkjet sarebbero una corrispondenza vicina ai colori che la stampante laser avrebbe stampato.

Il modo in cui vengono eseguite le conversioni nell'esempio consiste nel convertire i colori dell'immagine dal gamut dello schermo ai PC. Una volta convertiti i colori delle immagini nei PC, il profilo del dispositivo della stampante inkjet viene usato per trasformarli nella gamma della stampante inkjet. Successivamente, verrà usata la trasformazione gamut per PC per riportare i colori ai PC. A questo punto, il profilo di dispositivo della stampante laser viene usato per convertire i colori dai PC alla gamma della stampante laser.

La possibilità di trasformare facilmente i colori da una gamma di dispositivi ai PC e viceversa consente di riprovare i colori delle immagini per un dispositivo di output di un colore.

Nell'esempio precedente, la descrizione è leggermente diversa dalla procedura effettiva per maggiore chiarezza. In realtà, tutte le trasformazioni indicate nel paragrafo precedente verrebbero concatenate in una singola trasformazione.

 

 




