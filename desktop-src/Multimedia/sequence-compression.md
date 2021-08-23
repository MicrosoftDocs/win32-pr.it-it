---
title: Compressione di sequenza
description: Compressione di sequenza
ms.assetid: ea24088d-6a52-4d4e-8496-5b6a6616f684
keywords:
- gestione compressione video(VCM), compressione di sequenze
- VCM (gestione compressione video), compressione della sequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c930c1f2a3e73e21e63195129221aaa28017e5a8d59122be9d8cbf956b828bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688871"
---
# <a name="sequence-compression"></a>Compressione di sequenza

L'applicazione può usare le funzioni [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe), [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)e [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) per comprimere una sequenza di fotogrammi. Queste funzioni usano i dati archiviati nella [**struttura COMPVARS.**](/windows/desktop/api/Vfw/ns-vfw-compvars) Le applicazioni usano [**la funzione ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) per consentire all'utente di selezionare un proiettore, aprirlo e impostare i parametri di compressione nella **struttura COMPVARS.** Tuttavia, le applicazioni possono impostare i parametri nella struttura manualmente.

Prima che un'applicazione possa iniziare a comprimere una sequenza di frame, deve usare **ICSeqCompressFrameStart** per allocare le risorse necessarie. Dopo l'allocazione delle risorse, l'applicazione può **usare ICSeqCompressFrame** per comprimere singolarmente ogni frame. La frequenza dei fotogrammi e la frequenza dei fotogrammi chiave usati per comprimere la sequenza sono specificate nei membri della **struttura COMPVARS.** Il valore restituito **per ICSeqCompressFrame** punta ai dati compressi.

Quando un'applicazione termina la compressione di una sequenza, può usare **ICSeqCompressFrameEnd** per liberare le risorse di sistema allocate per **ICSeqCompressFrameStart.** Per liberare le risorse allocate per la **struttura COMPVARS,** l'applicazione può usare la [**funzione ICCompressorFree.**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)

 

 




