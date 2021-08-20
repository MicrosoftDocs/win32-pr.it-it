---
description: Un'applicazione può decomprimere più file usando le funzioni LZOpenFile, LZCopy e LZClose.
ms.assetid: 582d57c7-70a4-4711-bae5-4abfb7a196b1
title: Decompressione di più file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e2d7aef19dc79d4ebc78c1b04bff77ffbbe0fc19ec68daec6d54fe7040e735
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117998031"
---
# <a name="decompressing-multiple-files"></a>Decompressione di più file

Un'applicazione può decomprimere più file eseguendo le attività seguenti:

1.  Aprire i file di origine chiamando la [**funzione LZOpenFile.**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea)
2.  Aprire i file di destinazione chiamando [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
3.  Copiare i file di origine nei file di destinazione chiamando la [**funzione LZCopy.**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy)
4.  Chiudere i file chiamando la [**funzione LZClose.**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose)

 

 



