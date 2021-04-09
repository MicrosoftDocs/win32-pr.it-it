---
title: Compressori di User-Selected
description: Compressori di User-Selected
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- Gestione compressione video (VCM), commediatori selezionati dall'utente
- VCM (Gestione compressione video), commediatori selezionati dall'utente
- ICCompressorChoose (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbba48b919265ea6e0bab2c3d891f628c4e660a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955633"
---
# <a name="user-selected-compressors"></a>Compressori di User-Selected

Quando si comprimono i dati, l'applicazione può usare la funzione [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) per creare una finestra di dialogo in cui l'utente può selezionare il compressore. È possibile specificare i flag per questa funzione per consentire all'utente di specificare la frequenza del fotogramma chiave e la velocità dei dati cinematografici o di visualizzare una finestra di anteprima.

Il compressore selezionato dall'utente viene aperto automaticamente e il relativo handle viene restituito nel membro HIC della struttura [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) specificata in **ICCompressorChoose**.

Se si usa **ICCompressorChoose**, usare la funzione [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) per chiudere il compressore e liberare tutte le risorse associate alla struttura **COMPVARS** .

 

 




