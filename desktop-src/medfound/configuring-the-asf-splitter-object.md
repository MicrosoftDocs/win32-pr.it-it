---
description: Configurazione dell'oggetto Splitter ASF
ms.assetid: 8e2ba659-e1f6-42be-afd6-21fc841dc8d3
title: Configurazione dell'oggetto Splitter ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f27885e602dd52012808d330d997f9b7a7e983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127958"
---
# <a name="configuring-the-asf-splitter-object"></a>Configurazione dell'oggetto Splitter ASF

L'oggetto *splitter* ASF è un oggetto livello WMContainer che analizza l'oggetto dati ASF di un file di formato Advanced Systems (ASF). Dopo la creazione e l'inizializzazione della barra di divisione per analizzare l'oggetto dati ASF di un file multimediale, è necessario configurare la barra di divisione in modo da generare esempi per flussi specifici. Chiamare [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) per selezionare i flussi richiesti.

Facoltativamente, un'applicazione può anche configurarla per generare esempi in ordine inverso o generare esempi per il contenuto protetto. Per impostare queste opzioni, chiamare [**IMFASFSplitter:: Seflags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) e passare la combinazione bit per bit obbligatoria dei flag supportati. Prima di chiamare questo metodo, il client deve completare correttamente la chiamata [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) ; in caso contrario, i **flag** non riusciranno con il codice di errore **MF \_ E \_ non \_ inizializzato** . Per informazioni sull'inizializzazione della barra di divisione, vedere [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md).

Per verificare se questo flag è attualmente impostato sulla barra di divisione, chiamare [**IMFASFSplitter:: GetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getflags).

## <a name="selecting-streams-for-parsing"></a>Selezione dei flussi per l'analisi

Durante il processo di inizializzazione tramite la chiamata a [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) , la barra di divisione rileva il numero di flussi e gli identificatori di flusso nel file ASF. Per impostazione predefinita, nessun flusso viene selezionato dalla barra di divisione. L'applicazione deve selezionare i flussi chiamando [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams). Questo metodo accetta una matrice di numeri di flusso. Per ottenere il numero di flusso per un flusso, chiamare [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) nel profilo ASF o chiamare [**IMFStreamDescriptor:: GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) sul descrittore del flusso. È possibile ottenere sia il profilo ASF che il descrittore di flusso dall'oggetto ContentInfo. Se il client passa un numero di flusso non riconosciuto dalla barra di divisione, l'operazione ha esito negativo con un errore **MF \_ E \_ INVALIDSTREAMNUMBER** .

La chiamata di [**SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) Cancella le selezioni precedenti. Qualsiasi flusso non specificato nella matrice non è selezionato. Per ottenere un elenco dei flussi attualmente selezionati, chiamare [**IMFASFSplitter:: GetSelectedStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getselectedstreams). Questo metodo accetta un puntatore a una matrice, che il metodo compila con i numeri dei flussi. Se la dimensione della matrice è inferiore al numero di flussi selezionati, il metodo ha esito negativo con l'errore **MF \_ E \_ BUFFERTOOSMALL** . In questo caso, il metodo restituisce il numero di flussi selezionati nel parametro *pwNumStreams* . È quindi possibile usare questo numero per allocare una matrice delle dimensioni corrette e chiamare nuovamente il metodo.

Per un esempio di codice, vedere "selezionare un flusso per l'analisi" in [esercitazione: lettura di un file ASF](tutorial--reading-an-asf-file.md).

## <a name="reverse-playback-setting"></a>Impostazione della riproduzione inversa

Durante il processo di inizializzazione della barra di divisione, determina se il contenuto ASF supporta la riproduzione inversa. In caso contrario, la barra di divisione può essere configurata in modo da generare esempi in ordine inverso impostando il flag **MFASF \_ splitter \_ inverso** . Se il contenuto non supporta la riproduzione inversa, [**IMFASFSplitter:: Seflags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) restituisce **MF \_ E \_ INVALIDREQUEST**, ma il flag viene impostato sulla barra di divisione.

Se la barra di divisione è configurata in modo da essere analizzata nella direzione inversa, la barra di divisione inizia sempre l'analisi alla fine del buffer che contiene l'oggetto dati ASF. Pertanto, per l'analisi inversa dell'offset dei dati e la lunghezza dei dati da analizzare, è necessario impostare in modo appropriato. Per informazioni sull'impostazione dei valori corretti, vedere [generazione di esempi di flusso da un oggetto dati ASF esistente](generating-stream-samples-from-an-existing-asf-data-object.md).

## <a name="protected-content-setting"></a>Impostazione del contenuto protetto

La barra di divisione può essere configurata per funzionare con il contenuto di crittografia a livello di pacchetto impostando la **\_ barra di divisione MFASF \_ WMDRM** tramite [**IMFASFSplitter:: Flags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags). In questo modo viene indicato alla barra di divisione di fornire esempi per il contenuto protetto da Windows Media Digital Rights Management (DRM). Quando questo flag è impostato, gli esempi generati dal separatore contengono informazioni necessarie per decrittografare i dati multimediali e ricostruire i frame, ad esempio l'attributo [**\_ PacketCrossOffsets di MFSampleExtension**](mfsampleextension-packetcrossoffsets-attribute.md) . Questo attributo è un BLOB che contiene una matrice di **DWORD** s. Ogni **DWORD** fornisce i limiti del payload per il frame rispetto all'inizio del frame. Se questo attributo non è presente, il frame è contenuto in un singolo payload. In genere, gli esempi generati dal separatore contengono più buffer multimediali, l'applicazione può copiare tutti i buffer in un buffer contiguo chiamando [**IMFSample:: ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer). Il buffer risultante contiene il frame e il valore dell'attributo contiene gli offset in questo buffer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Barra di divisione ASF](asf-splitter.md)
</dt> </dl>

 

 



