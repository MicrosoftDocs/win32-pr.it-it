---
title: Scrittura di flussi in un file
description: Scrittura di flussi in un file
ms.assetid: a3766f8c-aaa6-4fc5-a306-54aee71018f1
keywords:
- AVIFileCreateStream (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370df08534bbdde870f6d28c828d47935abd80db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725543"
---
# <a name="writing-streams-to-a-file"></a>Scrittura di flussi in un file

È anche possibile creare un file contenente i flussi di dati scrivendo un nuovo flusso di dati in un file.

È possibile creare un nuovo flusso in un file nuovo o esistente usando la funzione [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) . Questa funzione definisce un nuovo flusso in base alle caratteristiche descritte in una struttura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) , crea un'interfaccia di flusso per il nuovo flusso, incrementa il conteggio dei riferimenti del flusso e restituisce l'indirizzo del puntatore a interfaccia di flusso.

Prima di scrivere il contenuto del flusso, è necessario specificare il formato del flusso. È possibile impostare il formato del flusso tramite la funzione [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) . Quando si imposta il formato di un flusso video, è necessario fornire questa funzione con una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenente le informazioni appropriate. Quando si imposta il formato di un flusso audio, è necessario fornire una struttura [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) o [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) contenente le informazioni appropriate. Le informazioni che è necessario fornire alla funzione per altri tipi di flusso dipendono dal tipo di flusso e dal gestore del flusso.

È possibile scrivere il contenuto multimediale in un flusso usando la funzione [**AVIStreamWrite**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite) . Questa funzione copia i dati non elaborati da un buffer fornito dall'applicazione nel flusso specificato. Il gestore di file AVI predefinito aggiunge informazioni alla fine di un flusso. Il gestore WAVE predefinito può scrivere i dati audio della forma d'onda all'interno di un flusso e alla fine di un flusso.

È possibile scrivere informazioni supplementari sul file o sul flusso che non è incluso nella funzione [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) o [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) usando le funzioni [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) e [**AVIStreamWriteData**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata) . È possibile registrare i dati applicabili all'intero file, ad esempio le informazioni sul copyright e la cronologia delle modifiche, usando **AVIFileWriteData**. È possibile registrare informazioni specifiche del flusso, ad esempio le impostazioni di compressione e decompressione, usando **AVIStreamWriteData**. Le informazioni supplementari vengono archiviate in blocchi distinti all'interno del file.

È possibile chiudere il flusso dopo aver completato la scrittura nel nuovo flusso tramite la funzione [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) . Questa funzione Cancella i buffer usati per la registrazione dei dati del flusso e completa e chiude tutti i blocchi di dati incompleti nel file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Operazioni di flusso](stream-operations.md)
</dt> </dl>

 

 