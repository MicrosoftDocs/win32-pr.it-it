---
description: La funzione GetFileSize recupera le dimensioni di un file.
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: Determinazione delle dimensioni di un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf4185d0bb695d73dc3afd03bb1ee7d6fe95cf606960fbdc41c4ce0b33b732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150614"
---
# <a name="determining-the-size-of-a-file"></a>Determinazione delle dimensioni di un file

La [**funzione GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) recupera le dimensioni di un file.

Poiché l'implementazione file system NTFS dei file consente più flussi all'interno di un file, qualsiasi applicazione che accede ai file deve essere in grado di includere più flussi nel file. Se non viene verificata la presenza di più flussi in un file, l'applicazione può sottostimare le dimensioni totali del file, tra gli altri errori.

 

 



