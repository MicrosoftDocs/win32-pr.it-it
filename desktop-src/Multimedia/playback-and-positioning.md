---
title: Riproduzione e posizionamento
description: Riproduzione e posizionamento
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efbd6256fbd0d258f5d5c9d3da9b01c72a203dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298095"
---
# <a name="playback-and-positioning"></a>Riproduzione e posizionamento

Una serie di comandi MCI, ad esempio [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)), [**Stop**](stop.md) ([**MCI \_ Stop**](mci-stop.md)), [**pause**](pause.md) ([**MCI \_ pause**](mci-pause.md)), [**Resume**](resume.md) ([**MCI \_ Resume**](mci-resume.md)) e [**Seek**](seek.md) ([**MCI \_ Seek**](mci-seek.md)), influiscono sulla riproduzione o sul posizionamento di un file multimediale. Se un dispositivo MCI riceve un comando di riproduzione mentre è in corso un altro comando di riproduzione, accetta il comando e arresta o sostituisce il comando precedente.

Molti comandi MCI, ad esempio [**set**](set.md) ([**MCI \_ set**](mci-set.md)), non influiscono sulla riproduzione. Una notifica da uno di questi comandi non interferisce con i comandi di riproduzione o posizione in sospeso, purché le notifiche non vengano eseguite dalla stessa istanza del driver. È ad esempio possibile emettere un comando **set** o [**status**](status.md) ([**\_ stato MCI**](mci-status.md)) mentre un dispositivo esegue un comando **Seek** senza arrestare o sostituire il comando **Seek** .

Tuttavia, può essere presente una sola notifica in sospeso. Se, ad esempio, un'applicazione richiede una notifica per la **riproduzione** e segue la richiesta con **stato** "inizio posizione notifica", la notifica di **riproduzione** restituirà "sostituito" e la notifica del comando di stato restituirà al termine. In questo caso, tuttavia, il comando **Play** avrà esito positivo anche se l'applicazione non ha ricevuto la notifica.

 

 




