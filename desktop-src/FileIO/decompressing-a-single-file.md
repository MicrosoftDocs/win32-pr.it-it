---
description: Un'applicazione può decomprimere un singolo file compresso usando le funzioni LZOpenFile, LZCopy e LZClose.
ms.assetid: e43df292-ed56-4023-92e8-de261e3b58a1
title: Decompressione di un singolo file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99152a36a2846bfe35a9d92bc3d8fd2eb6b5c3a7f0877179262801a9141bcc61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150837"
---
# <a name="decompressing-a-single-file"></a>Decompressione di un singolo file

Un'applicazione può decomprimere un singolo file compresso eseguendo le attività seguenti:

1.  Aprire il file di origine chiamando la [**funzione LZOpenFile.**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea)
2.  Aprire il file di destinazione chiamando [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
3.  Copiare il file di origine nel file di destinazione chiamando la [**funzione LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) e passando gli handle restituiti da [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
4.  Chiudere i file chiamando la [**funzione LZClose.**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose)

 

 



