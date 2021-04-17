---
description: Questo argomento descrive i passaggi minimi necessari per riprodurre dati audio caricati in precedenza in XAudio2.
ms.assetid: 5172b31c-d2af-45aa-5bd4-b62502f3c047
title: 'Procedura: Riprodurre un suono con XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ee2636ae9b6513dba9a479d63e0fd14be2c198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526881"
---
# <a name="how-to-play-a-sound-with-xaudio2"></a><span data-ttu-id="c6cfa-103">Procedura: Riprodurre un suono con XAudio2</span><span class="sxs-lookup"><span data-stu-id="c6cfa-103">How to: Play a Sound with XAudio2</span></span>

<span data-ttu-id="c6cfa-104">Questo argomento descrive i passaggi minimi necessari per riprodurre dati audio caricati in precedenza in XAudio2.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-104">This topic describes the minimum steps required to play previously-loaded audio data in XAudio2.</span></span> <span data-ttu-id="c6cfa-105">Dopo l'inizializzazione di XAudio2 (vedere [procedura: inizializzare XAudio2](how-to--initialize-xaudio2.md)) e caricare i dati audio (vedere Procedura: [caricare file di dati audio in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), è possibile riprodurre un suono creando una voce di origine e passandovi i dati audio.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-105">After you initialize XAudio2 (see [How to: Initialize XAudio2](how-to--initialize-xaudio2.md)) and load the audio data (see How to: [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), you can play a sound by creating a source voice and passing audio data to it.</span></span>

## <a name="to-play-a-sound"></a><span data-ttu-id="c6cfa-106">Per riprodurre un suono</span><span class="sxs-lookup"><span data-stu-id="c6cfa-106">To play a sound</span></span>

1.  <span data-ttu-id="c6cfa-107">Inizializzare il motore XAudio2 seguendo i passaggi descritti in [procedura: inizializzare XAudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="c6cfa-107">Initialize the XAudio2 engine by following the steps described in [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>
2.  <span data-ttu-id="c6cfa-108">Popolare una struttura del [**\_ buffer**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) e XAUDIO2 attenendosi alla procedura descritta in [procedura: caricare file di dati audio in XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="c6cfa-108">Populate a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure by following the steps described in [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="c6cfa-109">A seconda del formato dei dati audio, potrebbe essere necessario utilizzare una struttura di dati più grande contenente una struttura [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) al posto di un **WAVEFORMATEX**.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-109">Depending on the format of the audio data, you may need to use a larger data structure containing a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) structure in place of a **WAVEFORMATEX**.</span></span> <span data-ttu-id="c6cfa-110">Per ulteriori informazioni, vedere la pagina di riferimento di **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="c6cfa-110">See the **WAVEFORMATEX** reference page for more information.</span></span>

     

3.  <span data-ttu-id="c6cfa-111">Creare una voce di origine chiamando il metodo [**IXAudio2:: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) in un'istanza del motore XAudio2.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-111">Create a source voice by calling the [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) method on an instance of the XAudio2 engine.</span></span> <span data-ttu-id="c6cfa-112">Il formato della voce è specificato dai valori impostati in una struttura [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) .</span><span class="sxs-lookup"><span data-stu-id="c6cfa-112">The format of the voice is specified by the values set in a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) structure.</span></span>
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  <span data-ttu-id="c6cfa-113">Inviare un [**\_ buffer XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) alla voce di origine usando la funzione [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).</span><span class="sxs-lookup"><span data-stu-id="c6cfa-113">Submit an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) to the source voice using the function [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).</span></span>
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > <span data-ttu-id="c6cfa-114">I dati di esempio audio a cui i punti del *buffer* sono ancora di proprietà dell'app e devono rimanere allocati e accessibili fino a quando il suono smette di essere riprodotto.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-114">The audio sample data to which *buffer* points is still 'owned' by the app and must remain allocated and accessible until the sound stops playing.</span></span>

     

5.  <span data-ttu-id="c6cfa-115">Usare la funzione [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) per avviare la voce di origine.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-115">Use the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function to start the source voice.</span></span> <span data-ttu-id="c6cfa-116">Dato che tutte le voci XAudio2 inviano l'output alla voce Master per impostazione predefinita, l'audio dalla voce di origine si sposta automaticamente sul dispositivo audio selezionato in fase di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-116">Since all XAudio2 voices send their output to the mastering voice by default, audio from the source voice automatically makes its way to the audio device selected at initialization.</span></span> <span data-ttu-id="c6cfa-117">In un grafico audio più complesso, la voce di origine deve specificare la voce a cui deve essere inviato l'output.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-117">In a more complicated audio graph, the source voice would have to specify the voice to which its output should be sent.</span></span>
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a><span data-ttu-id="c6cfa-118">Note per le app di Windows Store</span><span class="sxs-lookup"><span data-stu-id="c6cfa-118">Notes for Windows Store apps</span></span>

<span data-ttu-id="c6cfa-119">Si consiglia di utilizzare un [puntatore intelligente](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) per gestire la durata degli oggetti XAUDIO2 in modo sicuro in un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-119">We recommend that you make use of a [smart pointer](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) to manage the lifetime of XAUDIO2 objects in an exception safe manner.</span></span> <span data-ttu-id="c6cfa-120">Per le app di Windows Store, è possibile usare il modello di puntatore intelligente [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) dalla libreria di modelli C++ Windows Runtime (WRL).</span><span class="sxs-lookup"><span data-stu-id="c6cfa-120">For Windows Store apps, you can use the [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) smart pointer template from the Windows Runtime C++ Template Library (WRL).</span></span>


```
Microsoft::WRL::ComPtr<IXAudio2SourceVoice> SourceVoice;
HRESULT hr;
if( FAILED(hr = pXAudio2->CreateSourceVoice( &SourceVoice, (WAVEFORMATEX*)&wfx ) ) )
    throw Platform::Exception::CreateException(hr); 

if( FAILED(hr = SourceVoice->SubmitSourceBuffer( &buffer ) ) )
    throw Platform::Exception::CreateException(hr); 

if ( FAILED(hr = SourceVoice->Start( 0 ) ) )
    throw Platform::Exception::CreateException(hr);
```



> [!Note]  
> <span data-ttu-id="c6cfa-121">Prima di rilasciare l'oggetto [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) , verificare che tutti i puntatori intelligenti per gli oggetti XAUDIO2 siano stati completamente rilasciati.</span><span class="sxs-lookup"><span data-stu-id="c6cfa-121">Ensure that all smart pointers to XAUDIO2 objects are fully released before you release the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c6cfa-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6cfa-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6cfa-123">Introduzione XAudio2</span><span class="sxs-lookup"><span data-stu-id="c6cfa-123">XAudio2 Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="c6cfa-124">Procedura: Inizializzare XAudio2</span><span class="sxs-lookup"><span data-stu-id="c6cfa-124">How to: Initialize XAudio2</span></span>](how-to--initialize-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="c6cfa-125">Procedura: Caricare file di dati audio in XAudio2</span><span class="sxs-lookup"><span data-stu-id="c6cfa-125">How to: Load Audio Data Files in XAudio2</span></span>](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 
