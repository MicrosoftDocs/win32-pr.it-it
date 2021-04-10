---
description: Ottenere la dimensione allocata o la dimensione totale per un file usando la funzione GetCompressedFileSize o Filesize.
ms.assetid: 1894ea01-49ff-41e3-9912-1cd75966bd3f
title: Recupero delle dimensioni di un file sparse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93a1c6a33f0d6913e0e6848e4593ea0e0bf0259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879698"
---
# <a name="obtaining-the-size-of-a-sparse-file"></a>Recupero delle dimensioni di un file sparse

Utilizzare la funzione [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) per ottenere la dimensione effettiva allocata sul disco per un file sparse. Il totale non include le dimensioni delle aree deallocate perché sono state riempite con zeri. Usare la funzione [**Filesize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) per determinare la dimensione totale di un file, incluse le dimensioni delle aree sparse deallocate.

 

 



