---
title: Scrittura Flussi in un file
description: Scrittura Flussi in un file
ms.assetid: a3766f8c-aaa6-4fc5-a306-54aee71018f1
keywords:
- Funzione AVIFileCreateStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaedd4103d2141ecaccde78462b2290cf5d5d37813b224c20101eacbe580d70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891761"
---
# <a name="writing-streams-to-a-file"></a>Scrittura Flussi in un file

È anche possibile creare un file contenente flussi di dati scrivendo un nuovo flusso di dati in un file.

È possibile creare un nuovo flusso in un file nuovo o esistente usando la [**funzione AVIFileCreateStream.**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) Questa funzione definisce un nuovo flusso in base alle caratteristiche descritte in una struttura [**AVISTREAMINFO,**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) crea un'interfaccia di flusso per il nuovo flusso, incrementa il conteggio dei riferimenti del flusso e restituisce l'indirizzo del puntatore dell'interfaccia di flusso.

Prima di scrivere il contenuto del flusso, è necessario specificare il formato del flusso. È possibile impostare il formato del flusso usando la [**funzione AVIStreamSetFormat.**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) Quando si imposta il formato di un flusso video, è necessario fornire a questa funzione una [**struttura BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente le informazioni appropriate. Quando si imposta il formato di un flusso audio, è necessario specificare una struttura [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) o [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) contenente le informazioni appropriate. Le informazioni da fornire alla funzione per altri tipi di flusso dipendono dal tipo di flusso e dal gestore del flusso.

È possibile scrivere il contenuto multimediale in un flusso usando la [**funzione AVIStreamWrite.**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite) Questa funzione copia i dati non elaborati da un buffer fornito dall'applicazione nel flusso specificato. Il gestore di file AVI predefinito aggiunge informazioni alla fine di un flusso. Il gestore WAVE predefinito può scrivere dati audio waveform all'interno di un flusso e alla fine di un flusso.

È possibile scrivere informazioni supplementari sul file o sul flusso non incluso nella funzione [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) o [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) usando le funzioni [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) e [**AVIStreamWriteData.**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata) È possibile registrare i dati applicabili all'intero file, ad esempio le informazioni sul copyright e la cronologia delle modifiche, **usando AVIFileWriteData.** È possibile registrare informazioni specifiche del flusso, ad esempio le impostazioni di compressione e decompressione, **usando AVIStreamWriteData.** Le informazioni supplementari vengono archiviate in blocchi separati all'interno del file.

È possibile chiudere il flusso dopo aver completato la scrittura nel nuovo flusso usando la [**funzione AVIStreamRelease.**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) Questa funzione cancella i buffer usati nella registrazione dei dati del flusso e completa e chiude tutti i blocchi di dati incompleti nel file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Operazioni di flusso](stream-operations.md)
</dt> </dl>

 

 