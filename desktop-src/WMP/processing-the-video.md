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
# <a name="processing-the-video"></a>Elaborazione del video

I dettagli del video di elaborazione variano a seconda del formato; non rientra nell'ambito di questa documentazione per fornire questi dettagli. In generale, l'obiettivo del plug-in è modificare i dati relativi ai colori nel buffer di input e quindi copiare i dati nel buffer di output.

Il plug-in di esempio elabora due tipi di formati video: YUV e RGB.

Per i video YUV, le informazioni sul colore rosso e blu sono codificate nei valori di i e V e il livello di luminanza è rappresentato dal valore Y. il valore verde è codificato e può essere recuperato usando un algoritmo. Il plug-in di esempio modifica semplicemente i valori utente e V in modo da influire sul livello di colore. Ogni byte U o V ha un valore compreso tra 0 e 255. Il plug-in innanzitutto regola ogni valore per essere rappresentato da un intervallo compreso tra-128 e 127, quindi ridimensiona il valore in base al fattore di scala specificato. Infine, il codice regola nuovamente il valore per l'intervallo da zero a 255 originale e copia i dati nel buffer di output. Il codice di esempio seguente elabora il video di UYVY. In questo formato, ogni altro byte è un valore U o Y.


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



Per il video RGB, le informazioni relative al colore e alla luminanza vengono codificate come valori separati rosso, verde e blu. Il plug-in di esempio calcola la media dei tre valori per determinare il valore per Gray, quindi regola ogni valore di colore usando il fattore di scala fornito. Anche in questo caso, i valori devono essere normalizzati per l'intervallo da-128 a 127 prima del ridimensionamento. Il codice seguente da Process32Bit Mostra il processo per RGB32:


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



Per ulteriori informazioni sui formati video, vedere il [sito Web FourCC](../directshow/fourcc-codes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in video DSP**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 