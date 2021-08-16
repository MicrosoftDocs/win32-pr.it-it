---
title: Elaborazione del video
description: Elaborazione del video
ms.assetid: 2fa337dd-34c0-4a09-8c20-21f6103627dd
keywords:
- Windows Media Player plug-in, DSP video
- plug-in, DSP video
- plug-in per l'elaborazione di segnali digitali, elaborazione video
- plug-in DSP, elaborazione video
- plug-in DSP video, elaborazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea168199270cfe8029b7b9303a7745db2c255f4268252a5bd80472a73c6f2f29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334024"
---
# <a name="processing-the-video"></a>Elaborazione del video

I dettagli dell'elaborazione del video variano per ogni formato. è oltre l'ambito di questa documentazione fornire questi dettagli. In senso generale, l'obiettivo del plug-in è modificare i dati sui colori nel buffer di input e quindi copiare i dati nel buffer di output.

Il plug-in di esempio elabora due tipi di formati video: YUV e RGB.

Per il video YUV, le informazioni sul colore rosso e blu vengono codificate nei valori you e V e il livello di luminance è rappresentato dal valore Y. il valore verde è codificato e può essere recuperato usando un algoritmo. Il plug-in di esempio modifica semplicemente i valori di you e V per influire sul livello di colore. Ogni byte U o V ha un valore compreso tra zero e 255. Il plug-in regola prima ogni valore in modo che sia rappresentato da un intervallo compreso tra -128 e 127 e quindi ridimensiona il valore in base al fattore di scala fornito. Infine, il codice regola nuovamente il valore per l'intervallo originale da zero a 255 e copia i dati nel buffer di output. Il codice di esempio seguente elabora il video UYVY. In questo formato, ogni altro byte è un valore U o Y.


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



Per il video RGB, le informazioni sul colore e sulla luminanza vengono codificate come valori rosso, verde e blu separati. Il plug-in di esempio calcola la media dei tre valori per determinare il valore per il grigio e quindi regola ogni valore di colore usando il fattore di scala fornito. Ancora una volta, i valori devono essere normalizzati per l'intervallo da -128 a 127 prima del ridimensionamento. Il codice seguente di Process32Bit illustra il processo per RGB32:


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



Per altre informazioni sui formati video, vedere il sito Web [FourCC.](../directshow/fourcc-codes.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in DSP video**](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 