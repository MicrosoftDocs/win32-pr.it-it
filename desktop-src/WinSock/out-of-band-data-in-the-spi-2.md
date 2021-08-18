---
description: I provider di servizi che supportano l'astrazione dei dati fuori banda (OOB) per i socket di tipo flusso devono rispettare la semantica in questa sezione.
ms.assetid: 83ed881f-8474-445e-8fb5-9635138a63dd
title: Dati fuori banda nell'spi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858e2845e9fbe198dc7af7a70edfad8a4ac429f8f1abe84289b87a779f6e478b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741052"
---
# <a name="out-of-band-data-in-the-spi"></a>Dati fuori banda nell'spi

I provider di servizi che supportano l'astrazione dei dati fuori banda (OOB) per i socket di tipo flusso devono rispettare la semantica in questa sezione. Verrà descritta la gestione dei dati OOB in modo indipendente dal protocollo. Per una descrizione dei dati OOB implementati usando dati urgenti nei provider di servizi TCP/IP, vedere gli allegati [Winsock.](winsock-annexes.md) L'uso di [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) si applica anche a [**WSPRecvFrom.**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))

 

 
