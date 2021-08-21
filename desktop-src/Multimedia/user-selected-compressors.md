---
title: User-Selected Concis
description: User-Selected Concis
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- gestione compressione video(VCM), file selezionati dall'utente
- VCM (Video Compression Manager),user-selected all'utente
- Funzione ICCompressorChoose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c855acb1ecd69876009d0cc3eb6a3b3f4129cc252183e40c5b2d00289be82842
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370801"
---
# <a name="user-selected-compressors"></a>User-Selected Concis

Quando si comprimono i dati, l'applicazione può usare la funzione [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) per creare una finestra di dialogo in cui l'utente può selezionare il tutto. È possibile specificare flag per questa funzione per consentire all'utente di specificare la frequenza dei fotogrammi chiave e la frequenza dei dati dei film oppure per visualizzare una finestra di anteprima.

L'elemento selezionato dall'utente viene aperto automaticamente e il relativo handle viene restituito nel membro hic della struttura [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) specificata in **ICCompressorChoose.**

Se si usa **ICCompressorChoose,** usare la funzione [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) per chiudere il campo e liberare tutte le risorse associate alla **struttura COMPVARS.**

 

 




