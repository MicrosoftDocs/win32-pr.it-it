---
description: Impostazione delle preferenze di Deinterlace
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: Impostazione delle preferenze di Deinterlace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33dae356618653f501b56f8b7a7eeb98e24ee92eb196cac78466e8cd26c01610
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072575"
---
# <a name="setting-deinterlace-preferences"></a>Impostazione delle preferenze di Deinterlace

Video Mixing Renderer (VMR) supporta la deinterlacing accelerata dall'hardware, che migliora la qualità del rendering per i video interlacciati. Le funzionalità esatte disponibili dipendono dall'hardware sottostante. L'applicazione può eseguire una query per le funzionalità di dinterlacing dell'hardware e impostare le preferenze di deinterlacing tramite l'interfaccia [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) (VMR-7) o [**l'interfaccia IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) (VMR-9). La deinterlacing viene eseguita in base al flusso.

Esiste una differenza importante nel comportamento di interlacciamento tra VMR-7 e VMR-9. Nei sistemi in cui l'hardware grafico non supporta la deinterlacing avanzata, VMR-7 può eseguire il fall back alla sovrapposizione hardware e indica di usare una delnterlace in stile BOB. In questo caso, anche se la macchina virtuale segnala 30fps, il rendering del video viene effettivamente eseguito a 60 flip al secondo.

Ad eccezione del caso di VMR-7 con sovrimpressione hardware, la deinterlacing viene eseguita dal mixer della macchina virtuale. Il mixer usa l'interfaccia DDI (Deinterlacing Device Driver Interface) DirectX Video Acceleration (DXVA) per eseguire la deinterlacing. Questa DDI non è chiamabile dalle applicazioni e le applicazioni non possono sostituire la funzionalità di dinterlacing della macchina virtuale. Tuttavia, un'applicazione può selezionare la modalità di dinterlacing desiderata, come descritto in questa sezione.

> [!Note]  
> Questa sezione descrive i metodi **IVMRDeinterlaceControl9,** ma le versioni di VMR-7 sono quasi identiche.

 

Per ottenere le funzionalità di dinterlacing per un flusso video, eseguire le operazioni seguenti:

1.  Compilare una [**struttura VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) con una descrizione del flusso video. I dettagli su come compilare questa struttura sono disponibili in un secondo momento.
2.  Passare la struttura al [**metodo IVMRDeinterlaceControl9::GetNumberOfDeinterlaceModes.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) Chiamare due volte il metodo . La prima chiamata restituisce il numero di modalità deinterlace supportate dall'hardware per il formato specificato. Allocare una matrice di GUID di queste dimensioni e chiamare di nuovo il metodo , passando l'indirizzo della matrice. La seconda chiamata riempie la matrice con GUID. Ogni GUID identifica una modalità di deinterlacing.
3.  Per ottenere i limiti di una particolare modalità, chiamare il metodo [**IVMRDeinterlaceControl9::GetDeinterlaceModeCaps.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) Passare la stessa **struttura VMR9VideoDesc,** insieme a uno dei GUID della matrice. Il metodo riempie una [**struttura VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) con le funzionalità di modalità.

Il codice seguente illustra questi passaggi:


```C++
VMR9VideoDesc VideoDesc; 
DWORD dwNumModes = 0;
// Fill in the VideoDesc structure (not shown).
hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
    &dwNumModes, NULL);
if (SUCCEEDED(hr) && (dwNumModes != 0))
{
    // Allocate an array for the GUIDs that identify the modes.
    GUID *pModes = new GUID[dwNumModes];
    if (pModes)
    {
        // Fill the array.
        hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
            &dwNumModes, pModes);
        if (SUCCEEDED(hr))
        {
            // Loop through each item and get the capabilities.
            for (int i = 0; i < dwNumModes; i++)
            {
                VMR9DeinterlaceCaps Caps;
                hr = pDeinterlace->GetDeinterlaceModeCaps(pModes + i, 
                    &VideoDesc, &Caps);
                if (SUCCEEDED(hr))
                {
                    // Examine the Caps structure.
                }
            }
        }
        delete [] pModes;
    }
}
```



Ora l'applicazione può impostare la modalità di deinterlacing per il flusso usando i metodi seguenti:

-   Il [**metodo SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) imposta la modalità preferita. Usare GUID \_ NULL per disattivare la deinterlacing.
-   Il [**metodo SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) specifica il comportamento se la modalità richiesta non è disponibile.
-   Il [**metodo GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) restituisce la modalità preferita impostata.
-   Il [**metodo GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) restituisce la modalità effettiva in uso, che potrebbe essere una modalità di fallback, se la modalità preferita non è disponibile.

Le pagine di riferimento del metodo forniscono altre informazioni.

**Uso della struttura VMR9VideoDesc**

Nella procedura descritta in precedenza, il primo passaggio consiste nel compilare una **struttura VMR9VideoDesc** con una descrizione del flusso video. Per iniziare, ottenere il tipo di supporto del flusso video. A tale scopo, chiamare [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) sul pin di input del filtro VMR. Verificare quindi se il flusso video è interlacciato. È possibile interlacciare solo i formati [**VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) Se il tipo di formato è FORMAT \_ VideoInfo, deve essere un frame progressivo. Se il tipo di formato è FORMAT VideoInfo2, controllare il \_ campo **dwInterlaceFlags** per il flag AMINTERLACE \_ IsInterlaced. La presenza di questo flag indica che il video è interlacciato.

Si supponga che la variabile **pBMI** sia un puntatore alla [**struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) nel blocco di formato. Impostare i valori seguenti nella **struttura VMR9VideoDesc:**

-   **dwSize:** impostare questo campo su `sizeof(VMR9VideoDesc)` .
-   **dwSampleWidth:** impostare questo campo su `pBMI->biWidth` .
-   **dwSampleHeight:** impostare questo campo su `abs(pBMI->biHeight)` .
-   **SampleFormat:** questo campo descrive le caratteristiche dell'interlacciato del tipo di supporto. Controllare il **campo dwInterlaceFlags** nella struttura **VIDEOINFOHEADER2** e impostare **SampleFormat** uguale al flag [**\_ SampleFormat VMR9**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) equivalente. Di seguito è riportata una funzione helper a tale scopo.
-   **InputSampleFreq:** questo campo fornisce la frequenza di input, che può essere calcolata dal campo **AvgTimePerFrame** nella **struttura VIDEOINFOHEADER2.** In generale, impostare **dwNumerator** su 100000000 e **dwDenominator** su **AvgTimePerFrame**. Tuttavia, è anche possibile verificare alcune frequenze di fotogrammi note:

    | Tempo medio per fotogramma | Frequenza fotogrammi (fps) | Numeratore | Denominatore |
    |------------------------|------------------|-----------|-------------|
    | 166833                 | 59.94 (NTSC)     | 60000     | 1001        |
    | 333667                 | 29.97 (NTSC)     | 30000     | 1001        |
    | 417188                 | 23.97 (NTSC)     | 24000     | 1001        |
    | 200000                 | 50.00 (PAL)      | 50        | 1           |
    | 400000                 | 25.00 (PAL)      | 25        | 1           |
    | 416667                 | 24.00 (Film)     | 24        | 1           |

    

     

-   **OutputFrameFreq:** questo campo fornisce la frequenza di output, che può essere calcolata dal valore **InputSampleFreq** e dalle caratteristiche di interfoliazione del flusso di input:
    -   Impostare **OutputFrameFreq.dwDenominator** su **InputSampleFreq.dwDenominator**.
    -   Se il video di input è interleaved, impostare **OutputFrameFreq.dwNumerator** su 2 x **InputSampleFreq.dwNumerator**. Dopo la deinterlacing, la frequenza dei fotogrammi è raddoppiata. In caso contrario, impostare il valore su **InputSampleFreq.dwNumerator**.
-   **dwFourCC:** impostare questo campo su `pBMI->biCompression` .

La funzione helper seguente converte i flag AMINTERLACE \_ *X* in [**valori \_ SampleFormat di VMR9:**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat)


```C++
#define IsInterlaced(x) ((x) & AMINTERLACE_IsInterlaced)
#define IsSingleField(x) ((x) & AMINTERLACE_1FieldPerSample)
#define IsField1First(x) ((x) & AMINTERLACE_Field1First)

VMR9_SampleFormat ConvertInterlaceFlags(DWORD dwInterlaceFlags)
{
    if (IsInterlaced(dwInterlaceFlags)) {
        if (IsSingleField(dwInterlaceFlags)) {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldSingleEven;
            }
            else {
                return VMR9_SampleFieldSingleOdd;
            }
        }
        else {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldInterleavedEvenFirst;
             }
            else {
                return VMR9_SampleFieldInterleavedOddFirst;
            }
        }
    }
    else {
        return VMR9_SampleProgressiveFrame;  // Not interlaced.
    }
}
```



 

 



