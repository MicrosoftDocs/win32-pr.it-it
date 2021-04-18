---
description: Un'applicazione può decomprimere più file usando le funzioni LZOpenFile, LZCopy e LZClose.
ms.assetid: 582d57c7-70a4-4711-bae5-4abfb7a196b1
title: Decompressione di più file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 206c7c233a5e0fda70326a45dfcde4e4194586d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310033"
---
# <a name="decompressing-multiple-files"></a>Decompressione di più file

Un'applicazione può decomprimere più file eseguendo le attività seguenti:

1.  Aprire i file di origine chiamando la funzione [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .
2.  Aprire i file di destinazione chiamando [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
3.  Copiare i file di origine nei file di destinazione chiamando la funzione [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) .
4.  Chiudere i file chiamando la funzione [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .

 

 



