---
description: Configurazione dell'oggetto splitter di ASF
ms.assetid: 8e2ba659-e1f6-42be-afd6-21fc841dc8d3
title: Configurazione dell'oggetto splitter di ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7068f2c869f6c73447b3341baee7221cdf8efbacec47ecdfa3a584bfb456f199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606151"
---
# <a name="configuring-the-asf-splitter-object"></a>Configurazione dell'oggetto splitter di ASF

L'oggetto *separatore* ASF è un oggetto livello WMContainer che analizza l'oggetto dati ASF di un file ASF (Advanced Systems Format). Dopo aver creato e inizializzato la barra di divisione per analizzare l'oggetto dati ASF di un file multimediale, la barra di divisione deve essere configurata per generare esempi per flussi specifici. Chiamare [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) per selezionare i flussi necessari.

Facoltativamente, un'applicazione può anche configurarla per generare esempi in ordine inverso o per il contenuto protetto. Per impostare queste opzioni, chiamare [**IMFASFSplitter::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) e passare la combinazione bit per bit richiesta dei flag supportati. Prima di chiamare questo metodo, il client deve completare correttamente la [**chiamata IMFASFSplitter::Initialize.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) In caso contrario, **SetFlags ha** esito negativo con codice di errore **MF \_ E NOT \_ \_ INITIALIZED.** Per informazioni sull'inizializzazione della barra di divisione, vedere [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md).

Per verificare se questo flag è attualmente impostato nella barra di divisione, chiamare [**IMFASFSplitter::GetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getflags).

## <a name="selecting-streams-for-parsing"></a>Selezione Flussi per l'analisi

Durante il processo di inizializzazione tramite la chiamata [**IMFASFSplitter::Initialize,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) la barra di divisione rileva il numero di flussi e gli identificatori di flusso nel file ASF. Per impostazione predefinita, la barra di divisione non seleziona alcun flusso. L'applicazione deve selezionare i flussi chiamando [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams). Questo metodo accetta una matrice di numeri di flusso. Per ottenere il numero di flusso per un flusso, chiamare [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) sul profilo ASF o [**chiamare IMFStreamDescriptor::GetStreamIdentifier**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getstreamidentifier) sul descrittore di flusso. È possibile ottenere sia il profilo ASF che il descrittore di flusso dall'oggetto ContentInfo. Se il client passa un numero di flusso non riconosciuto dalla barra di divisione, ha esito negativo con un errore **MF \_ E \_ INVALIDSTREAMNUMBER.**

La [**chiamata a SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) cancella le selezioni precedenti. Qualsiasi flusso non specificato nella matrice non è selezionato. Per ottenere un elenco dei flussi attualmente selezionati, chiamare [**IMFASFSplitter::GetSelectedStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getselectedstreams). Questo metodo accetta un puntatore a una matrice, che il metodo riempie con i numeri di flusso. Se la dimensione della matrice è inferiore al numero di flussi selezionati, il metodo ha esito negativo con l'errore **MF \_ E \_ BUFFERTOOSMALL.** In questo caso, il metodo restituisce il numero di flussi selezionati nel *parametro pwNumStreams.* È quindi possibile usare questo numero per allocare una matrice delle dimensioni corrette e chiamare nuovamente il metodo .

Per un esempio di codice, vedere "Selezionare un flusso per l'analisi" in [Esercitazione: Lettura di un file ASF.](tutorial--reading-an-asf-file.md)

## <a name="reverse-playback-setting"></a>Impostazioni di riproduzione inversa

Durante il processo di inizializzazione della barra di divisione, determina se il contenuto asf supporta la riproduzione inversa. In caso contrario, la barra di divisione può essere configurata per generare campioni in ordine inverso impostando il flag **MFASF \_ SPLITTER \_ REVERSE.** Se il contenuto non supporta la riproduzione inversa, [**IMFASFSplitter::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags) restituisce **MF \_ E \_ INVALIDREQUEST,** ma il flag è impostato sulla barra di divisione.

Se la barra di divisione è configurata per l'analisi nella direzione inversa, la barra di divisione inizia sempre l'analisi alla fine del buffer che contiene l'oggetto dati ASF. Pertanto, per l'analisi inversa dell'offset dei dati e della lunghezza dei dati da analizzare, è necessario impostare in modo appropriato. Per informazioni sull'impostazione dei valori corretti, vedere [Generazione di esempi di flusso da un oggetto dati ASF esistente.](generating-stream-samples-from-an-existing-asf-data-object.md)

## <a name="protected-content-setting"></a>Impostazione del contenuto protetto

La barra di divisione può essere configurata per funzionare con il contenuto di crittografia a livello di pacchetto impostando **MFASF \_ SPLITTER \_ WMDRM** tramite [**IMFASFSplitter::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-setflags). Questo indica alla barra di divisione di distribuire esempi per il contenuto protetto da Windows Media Digital Rights Management (DRM). Quando questo flag è impostato, gli esempi generati dalla barra di divisione contengono le informazioni necessarie per decrittografare i dati multimediali e ricostruire i fotogrammi, ad esempio l'attributo [**MFSampleExtension \_ PacketCrossOffsets.**](mfsampleextension-packetcrossoffsets-attribute.md) Questo attributo è un BLOB che contiene una matrice **di valori DWORD.** Ogni **valore DWORD** fornisce i limiti di payload per il frame rispetto all'inizio del frame. Se questo attributo non è presente, il frame è contenuto in un singolo payload. In genere, gli esempi generati dalla barra di divisione contengono più buffer multimediali. L'applicazione può copiare tutti i buffer in un unico buffer contiguo chiamando [**IMFSample::ConvertToContiguousBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer). Il buffer risultante contiene il frame e il valore dell'attributo contiene offset in questo buffer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Barra di divisione ASF](asf-splitter.md)
</dt> </dl>

 

 



