---
description: Esiste un'altra classe di eventi asincroni oltre a quelli descritti in precedenza.
ms.assetid: eaf4b014-1cab-4707-b750-9088e745083e
title: Eventi spontanei asincroni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd923ba7759ca88994fbf541c9f912ec660a7552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314638"
---
# <a name="asynchronous-spontaneous-events"></a>Eventi spontanei asincroni

Esiste un'altra classe di eventi asincroni oltre a quelli descritti in precedenza. Questi eventi sono "spontanei" nel senso che non sono risultati diretti delle richieste corrispondenti. Questi eventi vengono rilevati in questi casi come quando arriva una chiamata in ingresso o quando una chiamata in uscita passa da uno "squillo" a uno stato di "risposta". Quando TAPI Inizializza innanzitutto le interazioni con TSPI per un particolare dispositivo, passa un puntatore a una routine di callback da chiamare per la segnalazione di eventi spontanei. Insieme a questo puntatore di procedura è un handle di dispositivo che il provider di servizi include come uno dei parametri effettivi per il callback.

 

 



