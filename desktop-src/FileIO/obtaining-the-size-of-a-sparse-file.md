---
description: Ottenere le dimensioni allocate o le dimensioni totali per un file usando la funzione GetCompressedFileSize o GetFileSize.
ms.assetid: 1894ea01-49ff-41e3-9912-1cd75966bd3f
title: Recupero delle dimensioni di un file di tipo sparse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94fbe79448c73a0d5e0e8f60d19eb33f63a71ce58fbc20e66786b9d23cd7f161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996867"
---
# <a name="obtaining-the-size-of-a-sparse-file"></a>Recupero delle dimensioni di un file di tipo sparse

Usare la [**funzione GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) per ottenere le dimensioni effettive allocate su disco per un file di tipo sparse. Questo totale non include le dimensioni delle aree deallocate perché sono state riempite con zeri. Usare la [**funzione GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) per determinare le dimensioni totali di un file, incluse le dimensioni delle aree di tipo sparse deallocate.

 

 



