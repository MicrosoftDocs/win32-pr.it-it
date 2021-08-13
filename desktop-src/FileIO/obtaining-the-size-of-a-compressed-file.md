---
description: Per ottenere le dimensioni compresse di un file, usare la funzione GetCompressedFileSize.
ms.assetid: c6bfd221-f125-48b4-b38b-822a23639c40
title: Recupero delle dimensioni di un file compresso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3090272145c19ec5040a8df573a5100cad4d21b3fdc6f543e40d24f933dc3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648566"
---
# <a name="obtaining-the-size-of-a-compressed-file"></a>Recupero delle dimensioni di un file compresso

Usare la [**funzione GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) per ottenere le dimensioni compresse di un file. Se il file è compresso, le relative dimensioni compresse saranno inferiori alle dimensioni non compresse. Usare la [**funzione GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) per determinare le dimensioni non compresse di un file.

 

 



