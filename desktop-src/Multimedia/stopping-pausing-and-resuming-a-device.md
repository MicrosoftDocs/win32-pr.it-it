---
title: Arresto, sospensione e ripresa di un dispositivo
description: Arresto, sospensione e ripresa di un dispositivo
ms.assetid: df9ca4ab-4711-44dd-a058-909f291a1652
keywords:
- Comando MCI_STOP
- Comando MCI_PAUSE
- Comando MCI_RESUME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddcd9618608226dec108d62754964fe6401d429
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710702"
---
# <a name="stopping-pausing-and-resuming-a-device"></a>Arresto, sospensione e ripresa di un dispositivo

Il comando [**Stop**](stop.md) ([**MCI \_ Stop**](mci-stop.md)) sospende la riproduzione o la registrazione di un dispositivo. Molti dispositivi supportano anche il comando [**Sospendi**](pause.md) ([**\_ pausa MCI**](mci-pause.md)). La differenza tra l' **arresto** e la **pausa** dipende dal dispositivo. In genere **Sospendi** sospende l'operazione ma lascia il dispositivo pronto per riprendere la riproduzione o la registrazione immediatamente.

L'uso del comando [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)) o [**record**](record.md) ([**\_ record MCI**](mci-record.md)) per riavviare un dispositivo Reimposta i percorsi specificati con i flag "to" (MCI \_ to) e "from" (MCI \_ from) prima che il dispositivo sia stato sospeso o arrestato. Senza il flag "from", questi comandi reimpostano la posizione iniziale sulla posizione corrente. Senza il flag "a", reimpostano la posizione finale alla fine del supporto. Per continuare a eseguire la riproduzione o la registrazione senza reimpostare una posizione di arresto precedentemente specificata, usare il flag "to" del comando **Play** o **record** per specificare una posizione finale.

Alcuni dispositivi supportano il comando [**Resume**](resume.md) ([**MCI \_ Resume**](mci-resume.md)) per riavviare un dispositivo sospeso. Questo comando non modifica i percorsi "to" e "from" specificati con il comando **Play** o **record** che precedeva il comando [**pause**](pause.md) .

 

 




