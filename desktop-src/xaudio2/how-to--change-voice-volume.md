---
description: In questo argomento viene illustrato come è possibile modificare il volume di una voce a livello generale, a ogni canale di output o tra ogni canale di una voce e un'altra voce nel relativo oggetto Send.
ms.assetid: 40004128-4abb-4bcd-fe76-91276be8abec
title: 'Procedura: modificare il volume vocale'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a307c5585e56fb6dc4dbdc40386c6844607498ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757694"
---
# <a name="how-to-change-voice-volume"></a><span data-ttu-id="99d82-103">Procedura: modificare il volume vocale</span><span class="sxs-lookup"><span data-stu-id="99d82-103">How to: Change Voice Volume</span></span>

<span data-ttu-id="99d82-104">In questo argomento viene illustrato come è possibile modificare il volume di una voce a livello generale, a ogni canale di output o tra ogni canale di una voce e un'altra voce nel relativo oggetto [**Send**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span><span class="sxs-lookup"><span data-stu-id="99d82-104">This topic shows you how you can change the volume of a voice at an overall level, at each output channel, or between each channel of a voice and another voice in its [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span></span>

## <a name="to-set-an-overall-volume-level-for-the-voices-input"></a><span data-ttu-id="99d82-105">Per impostare un livello di volume complessivo per l'input della voce</span><span class="sxs-lookup"><span data-stu-id="99d82-105">To set an overall volume level for the voice's input</span></span>

-   <span data-ttu-id="99d82-106">Utilizzare la funzione [**sevolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) .</span><span class="sxs-lookup"><span data-stu-id="99d82-106">Use the [**SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume) function.</span></span>

    ```
    pSourceVoice->SetVolume(1.0);
    ```

    

## <a name="to-set-the-volume-of-the-voices-output-channels"></a><span data-ttu-id="99d82-107">Per impostare il volume dei canali di output della voce</span><span class="sxs-lookup"><span data-stu-id="99d82-107">To set the volume of the voice's output channels</span></span>

1.  <span data-ttu-id="99d82-108">Creare una matrice di numeri a virgola mobile contenenti i volumi desiderati di tutti i canali di output nella voce.</span><span class="sxs-lookup"><span data-stu-id="99d82-108">Create an array of floating point numbers that contain the desired volumes of all the output channels in the voice.</span></span>

    <span data-ttu-id="99d82-109">La matrice avrà una voce per ogni canale nella voce.</span><span class="sxs-lookup"><span data-stu-id="99d82-109">The array will have one entry for each channel in the voice.</span></span>

    ```
    float SourceVoiceChannelVolumes[1] = {1.0};
    ```

    

2.  <span data-ttu-id="99d82-110">Utilizzare la funzione [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) per impostare il volume dei canali di output.</span><span class="sxs-lookup"><span data-stu-id="99d82-110">Use the [**SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes) function to set the volume of the output channels.</span></span>

    ```
    hr = pSourceVoice->SetChannelVolumes(1,SourceVoiceChannelVolumes);
    ```

    

## <a name="to-set-the-volume-of-connections"></a><span data-ttu-id="99d82-111">Per impostare il volume delle connessioni</span><span class="sxs-lookup"><span data-stu-id="99d82-111">To set the volume of connections</span></span>

<span data-ttu-id="99d82-112">Impostare il volume di connessione tra la voce e una voce nel relativo oggetto [**Send**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span><span class="sxs-lookup"><span data-stu-id="99d82-112">Set the connection volume between the voice and a voice in its [**sendlist**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends).</span></span>

1.  <span data-ttu-id="99d82-113">Creare una matrice di numeri a virgola mobile che definisce una matrice di output se la voce Invia a un'altra voce.</span><span class="sxs-lookup"><span data-stu-id="99d82-113">Create an array of floating point numbers that defines an output matrix if the voice sends to another voice.</span></span>

    > [!Note]  
    > <span data-ttu-id="99d82-114">La matrice deve contenere un numero di voci uguale ai canali vocali di origine × canali vocali di destinazione.</span><span class="sxs-lookup"><span data-stu-id="99d82-114">The array must have a number of entries equal to source voice channels × destination voice channels.</span></span> <span data-ttu-id="99d82-115">In questo esempio, il mapping viene da una voce con un canale a una voce con due canali.</span><span class="sxs-lookup"><span data-stu-id="99d82-115">In this example, the mapping is from a voice with one channel to a voice with two channels.</span></span>

     

    ```
    float outputMatrix[2] = {1.0f,0.05f};
    ```

    

2.  <span data-ttu-id="99d82-116">Utilizzare la funzione [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) per impostare la matrice di output.</span><span class="sxs-lookup"><span data-stu-id="99d82-116">Use the [**SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix) function to set the output matrix.</span></span>

    ```
    pSourceVoice->SetOutputMatrix(pSubmixVoice,1,2,outputMatrix);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="99d82-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="99d82-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99d82-118">Guida alla programmazione di XAudio2</span><span class="sxs-lookup"><span data-stu-id="99d82-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="99d82-119">Procedura: Creare un grafico di elaborazione audio di base</span><span class="sxs-lookup"><span data-stu-id="99d82-119">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="99d82-120">Controllo volume e pitch XAudio2</span><span class="sxs-lookup"><span data-stu-id="99d82-120">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
