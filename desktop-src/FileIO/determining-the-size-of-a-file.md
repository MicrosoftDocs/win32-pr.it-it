---
description: La funzione Filesize recupera le dimensioni di un file.
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: Determinazione delle dimensioni di un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f7205c47fe25b223dbcc12322516ff2b162fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967631"
---
# <a name="determining-the-size-of-a-file"></a>Determinazione delle dimensioni di un file

La funzione [**Filesize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) recupera le dimensioni di un file.

Poiché l'implementazione del file system NTFS dei file consente più flussi all'interno di un file, qualsiasi applicazione scritta che accede ai file deve tenere conto della possibilità che l'autore del file possa includere più flussi nel file. Se non vengono controllati più flussi in un file, l'applicazione può sottovalutare la dimensione totale del file, tra gli altri errori.

 

 



