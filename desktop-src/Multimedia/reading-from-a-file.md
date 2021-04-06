---
title: Lettura da un file
description: Lettura da un file
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- AVIFileInfo (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1ffe866e454a898c5c3b91c7721c24f6a861ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045131"
---
# <a name="reading-from-a-file"></a>Lettura da un file

È possibile recuperare informazioni su un file aperto utilizzando la funzione [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) . Questa funzione riempie la struttura [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) con informazioni quali la velocità massima dei dati, il numero di flussi nel file, se il file usa un indice e se il file è protetto da copyright.

Per recuperare informazioni supplementari in un file AVI, usare la funzione [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) . Le informazioni supplementari sono applicabili all'intero file e non sono incluse nelle intestazioni dei file normali. Ad esempio, il nome della società o della persona che possiede il copyright di un file può essere costituito da informazioni supplementari. Le informazioni supplementari non rispettano un formato specifico; può trattarsi di un file specifico. **AVIFileReadData** restituisce le informazioni supplementari in un buffer fornito dall'applicazione.

 

 




