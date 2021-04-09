---
description: XAudio2 viene inizializzato per la riproduzione audio creando un'istanza del motore XAudio2 e creando una voce Master.
ms.assetid: 4db2e7fc-0a87-0344-a07c-3abf2b21af32
title: 'Procedura: Inizializzare XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a613c1ae2b7c3a7f0c55ab5349a0a605aaeb2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879594"
---
# <a name="how-to-initialize-xaudio2"></a><span data-ttu-id="16341-103">Procedura: Inizializzare XAudio2</span><span class="sxs-lookup"><span data-stu-id="16341-103">How to: Initialize XAudio2</span></span>

<span data-ttu-id="16341-104">XAudio2 viene inizializzato per la riproduzione audio creando un'istanza del motore XAudio2 e creando una voce Master.</span><span class="sxs-lookup"><span data-stu-id="16341-104">XAudio2 is initialized for audio playback by creating an instance of the XAudio2 engine, and creating a mastering voice.</span></span>

<span data-ttu-id="16341-105">**Per inizializzare XAudio2**</span><span class="sxs-lookup"><span data-stu-id="16341-105">**To initialize XAudio2**</span></span>

1.  <span data-ttu-id="16341-106">Assicurarsi di aver inizializzato COM.</span><span class="sxs-lookup"><span data-stu-id="16341-106">Make sure you have initialized COM.</span></span> <span data-ttu-id="16341-107">Per un'app di Windows Store, questa operazione viene eseguita come parte dell'inizializzazione del Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="16341-107">For a Windows Store app, this is done as part of initializing the Windows Runtime.</span></span> <span data-ttu-id="16341-108">In caso contrario, usare [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="16341-108">Otherwise, use [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  <span data-ttu-id="16341-109">Usare la funzione [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) per creare un'istanza del motore XAudio2.</span><span class="sxs-lookup"><span data-stu-id="16341-109">Use the [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) function to create an instance of the XAudio2 engine.</span></span>

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  <span data-ttu-id="16341-110">Usare il metodo [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) per creare una voce di master.</span><span class="sxs-lookup"><span data-stu-id="16341-110">Use the [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) method to create a mastering voice.</span></span>

    <span data-ttu-id="16341-111">Le voci di Master incapsulano un dispositivo audio.</span><span class="sxs-lookup"><span data-stu-id="16341-111">The mastering voices encapsulates an audio device.</span></span> <span data-ttu-id="16341-112">Si tratta della destinazione finale per tutti i file audio che passano attraverso un grafo audio.</span><span class="sxs-lookup"><span data-stu-id="16341-112">It is the ultimate destination for all audio that passes through an audio graph.</span></span>

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a><span data-ttu-id="16341-113">Note per le app di Windows Store</span><span class="sxs-lookup"><span data-stu-id="16341-113">Notes for Windows Store apps</span></span>

<span data-ttu-id="16341-114">Si consiglia di utilizzare un [puntatore intelligente](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) per gestire la durata degli oggetti XAUDIO2 in modo sicuro in un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="16341-114">We recommend that you make use of a [smart pointer](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) to manage the lifetime of XAUDIO2 objects in an exception safe manner.</span></span> <span data-ttu-id="16341-115">Per le app di Windows Store, è possibile usare il modello di puntatore intelligente [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) dalla libreria di modelli C++ Windows Runtime (WRL).</span><span class="sxs-lookup"><span data-stu-id="16341-115">For Windows Store apps, you can use the [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) smart pointer template from the Windows Runtime C++ Template Library (WRL).</span></span>


```C++
Microsoft::WRL::ComPtr<IXAudio2> XAudio2;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &XAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    throw Platform::Exception::CreateException(hr);

IXAudio2MasteringVoice* pMasterVoice = nullptr;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
    return hr;
```



> [!Note]  
> <span data-ttu-id="16341-116">Verificare che tutti gli oggetti figlio XAUDIO2 siano completamente rilasciati prima di rilasciare l'oggetto [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .</span><span class="sxs-lookup"><span data-stu-id="16341-116">Ensure that all XAUDIO2 child objects are fully released before you release the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="16341-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16341-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16341-118">Introduzione XAudio2</span><span class="sxs-lookup"><span data-stu-id="16341-118">XAudio2 Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="16341-119">Procedura: Caricare file di dati audio in XAudio2</span><span class="sxs-lookup"><span data-stu-id="16341-119">How to: Load Audio Data Files in XAudio2</span></span>](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="16341-120">Procedura: Riprodurre un suono con XAudio2</span><span class="sxs-lookup"><span data-stu-id="16341-120">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 
