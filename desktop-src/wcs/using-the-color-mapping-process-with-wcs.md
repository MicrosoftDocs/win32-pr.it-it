---
title: Utilizzo del processo di mapping dei colori con WCS
description: Il mapping dei colori WCS si basa sui profili di dispositivo.
ms.assetid: df4d390e-0c9e-40dc-864a-2177934895db
keywords:
- Windows Sistema di colori (WCS), mapping dei colori
- WCS (Windows Color System),mapping dei colori
- gestione dei colori delle immagini, mapping dei colori
- gestione dei colori, mapping dei colori
- colori, mapping dei colori
- mapping dei colori
- Windows Sistema colori (WCS), profili dispositivo
- WCS (Windows Color System),profili dispositivo
- gestione dei colori delle immagini, profili di dispositivo
- gestione dei colori, profili di dispositivo
- colori, profili di dispositivo
- Windows Sistema colori (WCS), profili
- WCS (Windows Color System),profiles
- gestione dei colori delle immagini, profili
- gestione dei colori, profili
- colori, profili
- profili di dispositivo
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe785af9fa4160c2aa1e54c6765857edc9c7aacb1a8fa40a0ad04e634b4ab602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119934261"
---
# <a name="using-the-color-mapping-process-with-wcs"></a>Utilizzo del processo di mapping dei colori con WCS

Il mapping dei colori WCS si basa sui [profili di dispositivo](d.md). Questi vengono forniti dai fornitori di dispositivi hardware a colori e installati quando viene installato un dispositivo. Quando il mapping dei colori viene usato da un programma applicativo, WCS accede al profilo di dispositivo dell'immagine per ottenere le informazioni necessarie per convertire l'immagine nel PCS. La conversione viene eseguita da CMM.

Un profilo di dispositivo può essere incorporato nell'immagine stessa. Il profilo del dispositivo viene quindi in viaggio con l'immagine, anche attraverso Internet. Un utente non ha bisogno del dispositivo di origine per ottenere un mapping dei colori accurato. Se un'immagine non ha un profilo di dispositivo, lo spazio sRGB viene usato come impostazione predefinita. Per altri dettagli, vedere [Using Color Management on the Internet (Uso della gestione dei colori in Internet).](using-color-management-on-the-internet.md)

Si noti che le applicazioni che usano WCS non devono mai incorporare il profilo sRGB in un'immagine. Lo spazio colore sRGB fornisce uno spazio colori standardizzato portabile in tutti i dispositivi. È automaticamente disponibile per gli utenti di Windows 98 e versioni successive, nonché Windows 2000 e versioni successive. Pertanto, non è necessario che viaggi con l'immagine.

Quando i colori dell'immagine sono nel [PCS,](p.md)WCS accede al profilo del dispositivo di destinazione. Ottiene il CMM per convertire i colori dell'immagine da PCS alla gamma del dispositivo di destinazione.

Il mapping dei colori più complesso può essere eseguito anche con WCS. Ad esempio, può essere usato per avere un'idea dell'aspetto di un'immagine creata su uno schermo video quando viene stampata su una stampante a colori ad alta risoluzione. L'esempio diventa più complesso se è presente solo una stampante ink ink standard in cui visualizzarne l'anteprima. L'immagine può essere convertita dalla gamma dello schermo alla gamma della stampante ink ink ink ink. Da qui può essere convertito nella gamma della stampante printer. L'immagine risultante può essere stampata sulla stampante ink ink ink. Naturalmente, l'immagine sarebbe a una risoluzione più elevata quando viene stampata sulla stampante color bitmap. Tuttavia, i colori dell'immagine di prova stampata sulla stampante ink sono molto vicini ai colori stampati dalla stampante blu.

Il modo in cui vengono completate le conversioni nell'esempio è convertire i colori dell'immagine dalla gamma dello schermo nel PCS. Dopo la conversione dei colori dell'immagine nel PCS, il profilo del dispositivo della stampante ink ink viene usato per trasformarli nella gamma della stampante ink ink. Successivamente, la trasformazione da gamut a PCS viene usata per spostare di nuovo i colori nel PCS. Da qui, viene usato il profilo del dispositivo della stampante a colori per convertire i colori da PCS alla gamma della stampante printer.

La possibilità di trasformare facilmente i colori da una gamma di dispositivi al PCS e di nuovo consente ai colori delle immagini destinati a un dispositivo di output a colori di essere a prova in quasi tutti gli altri.

Nell'esempio precedente la descrizione varia leggermente dalla procedura effettiva per maggiore chiarezza. In realtà, tutte le trasformazioni indicate nel paragrafo precedente verrebbero concatenate in un'unica trasformazione.

 

 




