---
description: I provider di servizi che supportano l'astrazione dei dati fuori banda (OOB) per i socket di tipo flusso devono rispettare la semantica in questa sezione.
ms.assetid: 83ed881f-8474-445e-8fb5-9635138a63dd
title: Dati fuori banda in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9808fa301073bcbb06be23a9487c2a1fa4f14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049479"
---
# <a name="out-of-band-data-in-the-spi"></a>Dati fuori banda in SPI

I provider di servizi che supportano l'astrazione dei dati fuori banda (OOB) per i socket di tipo flusso devono rispettare la semantica in questa sezione. Viene descritta la gestione dei dati di OOB in modo indipendente dal protocollo. Per una descrizione dei dati di OOB implementati con i dati urgenti nei provider di servizi TCP/IP, vedere gli [allegati di Winsock](winsock-annexes.md) . Nell'esempio seguente l'uso di [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) si applica anche a [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)).

 

 
