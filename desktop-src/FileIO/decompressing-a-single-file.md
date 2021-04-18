---
description: Un'applicazione può decomprimere un singolo file compresso usando le funzioni LZOpenFile, LZCopy e LZClose.
ms.assetid: e43df292-ed56-4023-92e8-de261e3b58a1
title: Decompressione di un singolo file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d8da6ee4ee80e42d6ff70c3d9c50efdc572f97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310036"
---
# <a name="decompressing-a-single-file"></a>Decompressione di un singolo file

Un'applicazione può decomprimere un singolo file compresso eseguendo le attività seguenti:

1.  Aprire il file di origine chiamando la funzione [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .
2.  Aprire il file di destinazione chiamando [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
3.  Copiare il file di origine nel file di destinazione chiamando la funzione [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) e passando gli handle restituiti da [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
4.  Chiudere i file chiamando la funzione [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .

 

 



