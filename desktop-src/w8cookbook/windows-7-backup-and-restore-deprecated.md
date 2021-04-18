---
title: Backup e ripristino di Windows 7 deprecato
description: Backup e ripristino di Windows 7 deprecato
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc20fa7ada55ada1f3c2f70c54955cec3d51666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "106300564"
---
# <a name="windows-7-backup-and-restore-deprecated"></a>Backup e ripristino di Windows 7 deprecato

## <a name="platform"></a>Piattaforma

**Client** -Windows 8 


## <a name="description"></a>Descrizione

Sebbene non esistano modifiche comportamentali al backup e al ripristino, questa funzione è deprecata e non verrà aggiornata. È stato usato raramente e la relativa funzionalità è stata sostituita dalla nuova funzionalità di cronologia file. Verrà fornito in Windows 8 e gli appassionati che hanno eseguito l'aggiornamento da Windows 7 a Windows 8 o dipendono da backup e ripristino oppure il backup delle immagini del disco sarà ancora in grado di usarlo. Tuttavia, tutti i punti di accesso per il backup e il ripristino, ad eccezione del pannello di controllo, sono stati rimossi. L'applet del pannello di controllo utilizzata da backup e ripristino è stata rinominata ripristino file di Windows 7.

Non sarà più necessario che gli OEM che impostavano la chiave del registro di sistema per disabilitare la notifica di backup nelle relative immagini.

Non è consigliabile usare entrambe le funzionalità nello stesso momento. Cronologia file controlla se la pianificazione del backup esiste ed è attiva e se ne trova una, non consente agli utenti di attivarla. In questo caso, gli utenti che desiderano utilizzare la cronologia file dovranno eliminare la pianificazione di backup di Windows.

## <a name="manifestation"></a>Manifestazione

I flussi di lavoro possono essere interrotti e la documentazione che fa riferimento al metodo precedente per accedere alla funzionalità di backup e ripristino di Windows deve essere aggiornata per riflettere queste modifiche.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Le app che potrebbero attivare il backup e il ripristino devono essere riscritte per verificare se la cronologia file è attiva e consentire agli utenti di scegliere il metodo preferito.

 

 




