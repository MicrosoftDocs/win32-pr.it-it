---
title: Riproduzione e posizionamento
description: Riproduzione e posizionamento
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9993c2ed4402184d2b15d5c3e54bb0137d1e7a3fe34f8cca36559ca329ada9d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892971"
---
# <a name="playback-and-positioning"></a>Riproduzione e posizionamento

Diversi comandi MCI, ad esempio play [**(**](play.md) [**MCI \_ PLAY**](mci-play.md)), [**stop**](stop.md) ([**MCI \_ STOP**](mci-stop.md)), [**pause**](pause.md) ([**MCI \_ PAUSE**](mci-pause.md)), [**resume**](resume.md) ([**MCI \_ RESUME**](mci-resume.md)) e [**seek**](seek.md) ([**MCI \_ SEEK**](mci-seek.md)), influiscono sulla riproduzione o sul posizionamento di un file multimediale. Se un dispositivo MCI riceve un comando di riproduzione mentre è in corso un altro comando di riproduzione, accetta il comando e arresta o sostituisce il comando precedente.

Molti comandi MCI, ad esempio [**set**](set.md) ([**MCI \_ SET**](mci-set.md)), non influiscono sulla riproduzione. Una notifica da uno di questi comandi non interferisce con i comandi di posizione o riproduzione in sospeso, purché le notifiche non siano eseguite dalla stessa istanza del driver. Ad esempio, è possibile eseguire un **comando set** o [**status**](status.md) [**(MCI \_ STATUS)**](mci-status.md)mentre un dispositivo esegue un comando **seek** senza arrestare o sostituisce il **comando seek.**

Tuttavia, può essere presente una sola notifica in sospeso. Ad esempio, se un'applicazione  richiede una notifica per la riproduzione e  segue tale richiesta con stato **"notifica** della posizione di inizio", la notifica di riproduzione restituirà "sostituita" e la notifica per il comando di stato restituirà al termine. In questo caso, tuttavia, il **comando play** avrà comunque esito positivo, anche se l'applicazione non ha ricevuto la notifica.

 

 




