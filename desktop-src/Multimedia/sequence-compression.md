---
title: Compressione sequenza
description: Compressione sequenza
ms.assetid: ea24088d-6a52-4d4e-8496-5b6a6616f684
keywords:
- Gestione compressione video (VCM), compressione sequenza
- VCM (Video Compression Manager), compressione sequenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8485c31361540ae0e0e9569453bc610d10d88d3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955418"
---
# <a name="sequence-compression"></a>Compressione sequenza

L'applicazione può usare le funzioni [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe), [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)e [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) per comprimere una sequenza di frame. Queste funzioni usano i dati archiviati nella struttura [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) . Le applicazioni usano la funzione [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) per consentire all'utente di selezionare un compressore, aprirlo e impostare i parametri di compressione nella struttura **COMPVARS** ; Tuttavia, le applicazioni possono impostare manualmente i parametri nella struttura.

Prima che un'applicazione possa iniziare a comprimere una sequenza di frame, deve usare **ICSeqCompressFrameStart** per allocare le risorse necessarie. Una volta allocate le risorse, l'applicazione può usare **ICSeqCompressFrame** per comprimere singolarmente ogni frame. La frequenza dei fotogrammi e la frequenza del fotogramma chiave usati nella compressione della sequenza vengono specificati nei membri della struttura **COMPVARS** . Il valore restituito per **ICSeqCompressFrame** punta ai dati compressi.

Quando un'applicazione termina la compressione di una sequenza, può usare **ICSeqCompressFrameEnd** per liberare le risorse di sistema allocate per **ICSeqCompressFrameStart**. Per liberare le risorse allocate per la struttura **COMPVARS** , l'applicazione può usare la funzione [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) .

 

 




