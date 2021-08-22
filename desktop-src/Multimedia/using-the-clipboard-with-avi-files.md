---
title: Uso degli Appunti con i file AVI
description: Uso degli Appunti con i file AVI
ms.assetid: 76ef7cc9-9afd-462a-b9fe-2b62f8113a9a
keywords:
- Funzione AVIPutFileOnClipboard
- Funzione AVIGetFromClipboard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 579f7eeed3b5b7397e248bb1c9090bc086cb715c591ec436af5de7d885551c14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687841"
---
# <a name="using-the-clipboard-with-avi-files"></a>Uso degli Appunti con i file AVI

Gli Appunti forniscono un comodo spazio di archiviazione temporaneo che un'applicazione può usare per copiare o trasferire file AVI. AVIFile include le funzioni degli Appunti che è possibile usare con i file su disco o di memoria.

È possibile copiare un file negli Appunti usando la [**funzione AVIPutFileOnClipboard.**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) Per scrivere un file che si trova negli Appunti in memoria o su disco, usare la [**funzione AVIGetFromClipboard.**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard)

È possibile cancellare un file dagli Appunti usando la [**funzione AVIClearClipboard.**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) Questa funzione non cancella altri tipi di informazioni, ad esempio testo, dagli Appunti. Se si usano le funzioni degli Appunti nell'applicazione, cancellare gli Appunti con **AVIClearClipboard** prima di chiudere l'applicazione o chiudere il file negli Appunti. È possibile chiamare **AVIClearClipboard** nell'applicazione indipendentemente dal fatto che sia stato usato **AVIPutFileOnClipboard.**

> [!Note]  
> Se l'applicazione copia un file negli Appunti e il file contiene dati di flusso che potrebbero cambiare, è possibile creare un file di memoria dei flussi clonati usando la [**funzione AVIMakeFileFromStreams.**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) È quindi possibile inserire il file negli Appunti e quindi rilasciare il file originale senza invalidarlo.

 

 

 




