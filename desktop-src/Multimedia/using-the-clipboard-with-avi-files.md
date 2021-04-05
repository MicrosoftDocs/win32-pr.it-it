---
title: Uso degli Appunti con file AVI
description: Uso degli Appunti con file AVI
ms.assetid: 76ef7cc9-9afd-462a-b9fe-2b62f8113a9a
keywords:
- AVIPutFileOnClipboard (funzione)
- AVIGetFromClipboard (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe46f463f22aa2d015d4ffd8496eb95c37053a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710621"
---
# <a name="using-the-clipboard-with-avi-files"></a>Uso degli Appunti con file AVI

Gli appunti forniscono un'archiviazione temporanea e pratica che un'applicazione può usare per copiare o trasferire file AVI. AVIFile include funzioni degli appunti che è possibile usare con i file di disco o di memoria.

È possibile copiare un file negli appunti usando la funzione [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) . Per scrivere un file negli Appunti in memoria o disco, usare la funzione [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) .

È possibile cancellare un file dagli appunti usando la funzione [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) . Questa funzione non cancella dagli Appunti altri tipi di informazioni, ad esempio testo. Se si utilizzano le funzioni degli Appunti nell'applicazione, cancellare gli appunti con **AVIClearClipboard** prima di chiudere l'applicazione o chiudere il file negli Appunti. È possibile chiamare **AVIClearClipboard** nell'applicazione indipendentemente dall'uso di **AVIPutFileOnClipboard** .

> [!Note]  
> Se l'applicazione copia un file negli Appunti e il file contiene dati di flusso che potrebbero cambiare, è possibile creare un file di memoria di flussi clonati usando la funzione [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) . È quindi possibile inserire il file negli Appunti e quindi rilasciare il file originale senza invalidarlo.

 

 

 




