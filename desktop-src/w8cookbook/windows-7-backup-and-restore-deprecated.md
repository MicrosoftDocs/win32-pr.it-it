---
title: Windows 7 Backup e ripristino deprecati
description: Windows 7 Backup e ripristino deprecati
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5975483797423515a4c04a35f8766de241553cb98a386bd53adcc7970977f7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211230"
---
# <a name="windows-7-backup-and-restore-deprecated"></a>Windows 7 Backup e ripristino deprecati

## <a name="platform"></a>Piattaforma

**Client** : Windows 8 


## <a name="description"></a>Descrizione

Anche se non sono state apportate modifiche di comportamento a Backup e ripristino, questa funzione è deprecata e non verrà aggiornata. È stato usato raramente e le relative funzionalità sono state sostituite dalla nuova Cronologia file funzionalità. Sarà disponibile in Windows 8 e gli appassionati che hanno eseguito l'aggiornamento da Windows 7 a Windows 8 o dipendono dal backup e ripristino o dal backup dell'immagine del disco saranno comunque in grado di usarlo. Tuttavia, tutti i punti di accesso a Backup e ripristino, ad eccezione del Pannello di controllo, sono stati rimossi. L Pannello di controllo applet usata da Backup e ripristino è stata rinominata Windows 7 Ripristino file.

Gli OEM che impostavano la chiave del Registro di sistema per disabilitare la notifica di backup nelle immagini non dovranno più farlo.

Non è consigliabile usare entrambe le funzionalità contemporaneamente. Cronologia file verifica se la pianificazione del backup esiste ed è attiva e, se ne trova una, non consente agli utenti di attivarla. In questo caso, gli utenti che vogliono usare Cronologia file necessario eliminare la Windows Backup pianificazione.

## <a name="manifestation"></a>Manifestazione

I flussi di lavoro possono essere interrotti e la documentazione che fa riferimento al metodo precedente per l'accesso alla funzionalità Windows Backup e ripristino dovrà essere aggiornata per riflettere queste modifiche.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Le app che potrebbero attivare backup e ripristino devono essere riscritte per verificare se Cronologia file è attivata e consentire agli utenti di scegliere il metodo preferito.

 

 




