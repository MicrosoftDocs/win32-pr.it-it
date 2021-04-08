---
title: Elaborazione del video
description: Elaborazione del video
ms.assetid: 2fa337dd-34c0-4a09-8c20-21f6103627dd
keywords:
- Plug-in di Windows Media Player, video DSP
- plug-in, video DSP
- plug-in per l'elaborazione di segnali digitali, elaborazione video
- Plug-in DSP, elaborazione video
- plug-in di video DSP, elaborazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a8d21aaa3999d05ea3628ff341c74379b07a6dd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046926"
---
# <a name="processing-the-video"></a><span data-ttu-id="2272f-108">Elaborazione del video</span><span class="sxs-lookup"><span data-stu-id="2272f-108">Processing the Video</span></span>

<span data-ttu-id="2272f-109">I dettagli del video di elaborazione variano a seconda del formato; non rientra nell'ambito di questa documentazione per fornire questi dettagli.</span><span class="sxs-lookup"><span data-stu-id="2272f-109">The details of processing video vary for each format; it is beyond the scope of this documentation to provide these details.</span></span> <span data-ttu-id="2272f-110">In generale, l'obiettivo del plug-in è modificare i dati relativi ai colori nel buffer di input e quindi copiare i dati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="2272f-110">In a general sense, the goal of the plug-in is to change the color data in the input buffer and then copy the data to the output buffer.</span></span>

<span data-ttu-id="2272f-111">Il plug-in di esempio elabora due tipi di formati video: YUV e RGB.</span><span class="sxs-lookup"><span data-stu-id="2272f-111">The sample plug-in processes two types of video formats: YUV and RGB.</span></span>

<span data-ttu-id="2272f-112">Per i video YUV, le informazioni sul colore rosso e blu sono codificate nei valori di i e V e il livello di luminanza è rappresentato dal valore Y. il valore verde è codificato e può essere recuperato usando un algoritmo.</span><span class="sxs-lookup"><span data-stu-id="2272f-112">For YUV video, the red and blue color information is encoded in the U and V values and the luminance level is represented by the Y value; the green value is encoded and can be recovered by using an algorithm.</span></span> <span data-ttu-id="2272f-113">Il plug-in di esempio modifica semplicemente i valori utente e V in modo da influire sul livello di colore.</span><span class="sxs-lookup"><span data-stu-id="2272f-113">The sample plug-in simply changes the U and V values to affect the color level.</span></span> <span data-ttu-id="2272f-114">Ogni byte U o V ha un valore compreso tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="2272f-114">Each U or V byte has a value between zero and 255.</span></span> <span data-ttu-id="2272f-115">Il plug-in innanzitutto regola ogni valore per essere rappresentato da un intervallo compreso tra-128 e 127, quindi ridimensiona il valore in base al fattore di scala specificato.</span><span class="sxs-lookup"><span data-stu-id="2272f-115">The plug-in first adjusts each value to be represented by a range from -128 to 127, and then scales the value by the supplied scale factor.</span></span> <span data-ttu-id="2272f-116">Infine, il codice regola nuovamente il valore per l'intervallo da zero a 255 originale e copia i dati nel buffer di output.</span><span class="sxs-lookup"><span data-stu-id="2272f-116">Finally, the code adjusts the value again for the original zero-to-255 range and copies the data to the output buffer.</span></span> <span data-ttu-id="2272f-117">Il codice di esempio seguente elabora il video di UYVY.</span><span class="sxs-lookup"><span data-stu-id="2272f-117">The following example code processes UYVY video.</span></span> <span data-ttu-id="2272f-118">In questo formato, ogni altro byte è un valore U o Y.</span><span class="sxs-lookup"><span data-stu-id="2272f-118">In this format, every other byte is a U or Y value.</span></span>


```C++
while( dwHeight-- )
{
    DWORD x = dwWidth; 

        while( x-- )
        {
        // Scale the U and V bytes to 128.
        // Just copy the Y bytes.
        if( x%2 )
        {
            pbTarget[x] = pbSource[x];
        }
        else
        {
            long temp = (long)((pbSource[x] - 128) * m_fScaleFactor);

            // Truncate if exceeded full scale.
            if (temp > 127)
            temp = 127;
            if (temp < -128)
            temp = -128;

            pbTarget[x] = temp + 128;
        }
    }

    // Move the pointers to the next row.
    pbSource += lStrideIn;
    pbTarget += lStrideOut;
}

```



<span data-ttu-id="2272f-119">Per il video RGB, le informazioni relative al colore e alla luminanza vengono codificate come valori separati rosso, verde e blu.</span><span class="sxs-lookup"><span data-stu-id="2272f-119">For RGB video, the color and luminance information is encoded as separate red, green, and blue values.</span></span> <span data-ttu-id="2272f-120">Il plug-in di esempio calcola la media dei tre valori per determinare il valore per Gray, quindi regola ogni valore di colore usando il fattore di scala fornito.</span><span class="sxs-lookup"><span data-stu-id="2272f-120">The sample plug-in computes the average of the three values to determine the value for gray, and then adjusts each color value by using the supplied scale factor.</span></span> <span data-ttu-id="2272f-121">Anche in questo caso, i valori devono essere normalizzati per l'intervallo da-128 a 127 prima del ridimensionamento.</span><span class="sxs-lookup"><span data-stu-id="2272f-121">Once again, the values must be normalized for the -128 to 127 range before scaling.</span></span> <span data-ttu-id="2272f-122">Il codice seguente da Process32Bit Mostra il processo per RGB32:</span><span class="sxs-lookup"><span data-stu-id="2272f-122">The following code from Process32Bit shows the process for RGB32:</span></span>


```C++
while( dwHeight-- )
{
    RGBQUAD* pPixelIn = (RGBQUAD*)pbSource;
    RGBQUAD* pPixelOut = (RGBQUAD*)pbTarget;

    for( DWORD x = 0; x < dwWidth; x++ )
    {
    // Get the color bytes.
    long lBlue = (long) pPixelIn[x].rgbBlue;
    long lGreen = (long) pPixelIn[x].rgbGreen;
    long lRed = (long) pPixelIn[x].rgbRed;

    // Compute the average for gray.
    long lAverage = ( lBlue + lGreen + lRed ) / 3;

    // Scale the colors to the average.
    pPixelOut[x].rgbBlue = (BYTE)( ( lBlue - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbGreen = (BYTE)( ( lGreen - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbRed = (BYTE)( ( lRed - lAverage ) * m_fScaleFactor  + lAverage );
    pPixelOut[x].rgbReserved = pPixelIn[x].rgbReserved;
    }

    // Move the pointers to the next row.
    pbSource += lStrideIn;
    pbTarget += lStrideOut;
}

```



<span data-ttu-id="2272f-123">Per ulteriori informazioni sui formati video, vedere il [sito Web FourCC](../directshow/fourcc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="2272f-123">For more information about video formats, see the [FourCC website](../directshow/fourcc-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="2272f-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2272f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2272f-125">**Implementazione di un plug-in video DSP**</span><span class="sxs-lookup"><span data-stu-id="2272f-125">**Implementing a Video DSP Plug-in**</span></span>](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 