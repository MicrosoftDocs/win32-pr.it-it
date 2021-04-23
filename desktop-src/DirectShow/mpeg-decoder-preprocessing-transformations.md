---
description: Trasformazioni di pre-elaborazione del decodificatore MPEG
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Trasformazioni di pre-elaborazione del decodificatore MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d7bcf8eeda8062606ce0046a55e34d3c2d90fe
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908899"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a>Trasformazioni di pre-elaborazione del decodificatore MPEG

**Letterbox e PanScan**

L'immagine 4x3 può essere formata mediante il riempimento della parte superiore e inferiore dell'immagine (detta immagine Letterbox) o estraendo una parte 4x3 dell'immagine (detta immagine PanScan). I menu e i flussi delle immagini secondarie sono sovrapposti all'immagine video finale. Le immagini con rapporto 16x9 vengono archiviate in un formato anamorfico 4x3. L'estensione del video di origine anamorfico 4x3 con proporzioni 720x480 a proporzioni 16x9 costituisce l'immagine originale dell'aspetto 16x9.

Di seguito è riportata una descrizione di come visualizzare correttamente ogni modalità e le relative evidenziazioni:

-   **Widescreen:** Il video di origine si estende nell'area più grande di 16x9 della finestra di output. Le evidenziazioni sono relative all'interno dell'area 16x9. Le barre nere devono essere aggiunte nella parte superiore e inferiore o ai lati per mantenere un'area 16x9.
-   **Analisi panoramica:** Dal video 16x9 usare l'offset orizzontale fornito nel flusso MPEG2 per estrarre una finestra secondaria 4x3. Posizionare la finestra secondaria 4x3 nell'area 4x3 più grande della finestra del client di output. Le coordinate dell'evidenziazione sono relative alla finestra di output 4x3 e non hanno alcuna relazione con il video 16x9 di origine. Le barre nere devono essere aggiunte nella parte superiore e inferiore o ai lati per mantenere un'area 4x3.
-   **Letterbox:** Calcolare l'area 4x3 più grande della finestra di output. Le barre nere devono essere aggiunte nella parte superiore e inferiore o ai lati per mantenere un'area 4x3. Il video anamorfico 4x3 di origine (che rappresenta un'immagine 16x9) viene posizionato nella finestra secondaria 16x9 più grande all'interno dell'area 4x3. Le barre nere devono essere aggiunte nella parte superiore e inferiore della finestra secondaria per mantenere un'area 16x9. Le coordinate dell'evidenziazione sono relative all'area 4x3 e non hanno alcuna relazione con il video 16x9 di origine. È possibile per un disco specificare un'evidenziazione che si trova all'esterno dell'area 16x9 (ma ancora nella finestra 4x3). Per il video 4x3, il video viene inserito nell'area di output 4x3 più grande della finestra del client di output. Le barre nere devono essere aggiunte nella parte superiore e inferiore o ai lati per mantenere un'area 4x3.

**Pre-elaborazione MPEG con lo strumento di spostamento DVD e VMR**

Attualmente al decodificatore viene passato un tipo di supporto FORMAT MPEG2 VIDEO (il cui blocco di formato punta \_ \_ a una struttura [**MPEG2VIDEOINFO).**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) Sui pin di output, il decodificatore produce un tipo di supporto FORMAT VideoInfo2, il cui blocco di formato punta \_ a una [**struttura VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) Il campo **dwReserved** della struttura è stato rinominato in **flag dwControls.**

Il **membro dwControlFlags** conterrà ora i nuovi bit.



| Label | Valore |
|--------------------------|------------|
| AMCONTROL \_ USATO          | 0x00000001 |
| AMCONTROL \_ PAD \_ TO \_ 4x3  | 0x00000002 |
| AMCONTROL \_ PAD \_ TO \_ 16x9 | 0x00000004 |



 

AMCONTROL \_ USED viene usato per verificare se questi nuovi flag sono supportati. Un filtro di origine deve impostare il flag AMCONTROL USED e verificare se \_ QueryAccept(MediaType) ha esito positivo sul pin downstream. Se viene rifiutato, non è possibile usare i flag AMCONTROL e dwReserved1 deve essere impostato su 0.

AMCONTROL PAD TO 4x3 indica che l'immagine deve essere riempita e visualizzata \_ \_ in \_ un'area 4x3.

AMCONTROL PAD TO 16x9 indica che l'immagine deve essere riempita e visualizzata \_ \_ in \_ un'area 16x9.

Il decodificatore deve copiare o elaborare i bit in modo blindato. Se il decodificatore esegue il letterboxing, deve modificare le proporzioni dei pixel, riempire l'immagine e rimuovere i bit AMCONTROL \_ \* corrispondenti.

MPEG2VIDEOINFO.dwFlags contiene ora tre flag per controllare la modalità di visualizzazione del contenuto:

-   `AMMPEG2_DoPanScan (0x00000001)`: se questo flag è impostato, il decodificatore video MPEG-2 deve ritagliare l'immagine di output in base ai vettori di scansione panoramica nell'estensione di visualizzazione dell'immagine e modificare le proporzioni dell'immagine in \_ \_ 4x3. Il vmr non deve ricevere un esempio 16x9 con questo flag. Un'implementazione semplice potrebbe modificare il rettangolo di origine per indicare un'area di origine di 540 larghezza con un bordo sinistro uguale all'offset di visualizzazione nell'estensione di \_ visualizzazione \_ dell'immagine.
-   `AMMPEG2_LetterboxAnalogOut (0x00000020)`: quando un decodificatore hardware visualizza questo flusso in un output video (in genere un connettore SVIDEO sulla scheda), deve applicare le regole per la visualizzazione di un campione 16x9 su un display 4x3.

    Un decodificatore software (o un decodificatore hardware che produce l'output inviato al VMR) ha due opzioni per l'elaborazione delle immagini:

    1.  Ignorare questo flag e passare il contenuto di VideoInfoHeader2 al VMR(il flag AMCONTROL PAD TO 4x3 sarà già impostato dallo strumento di navigazione \_ \_ \_ [DVD](dvd-navigator-filter.md) nell'esempio). La macchina virtuale risconterà un esempio di video 16x9 con il flag AMCONTROL PAD TO 4x3 impostato e un flusso di immagini secondarie \_ \_ \_ 4x3. L'applicazione deve impostare i rettangoli di destinazione normalizzati di output dei due flussi sulla stessa larghezza.
    2.  Convertire il flusso anamorfico in un'immagine 4x3 mediante il riempimento della parte superiore e inferiore dell'immagine e l'impostazione delle proporzioni dell'immagine su 4x3 (vedere Letterbox sopra) e rimuovendo AMCONTROL \_ PAD \_ a \_ 4x3 bit da VIDEOINFOHEADER2.

    I decodificatori DirectXVA che combinano i flussi video e di immagini secondarie devono elaborare questo flag. Se l'hardware non è in grado di ridimensionare l'immagine secondaria blended, il decodificatore deve produrre un flusso di immagini secondarie separato per la vmr per la fusione con il video.

-   `AMMPEG2_WidescreenAnalogOut (0x00000200)`: quando un decodificatore hardware visualizza questo flusso in un output video (in genere un connettore SVIDEO sulla scheda), deve presupporre un display 16x9 (anamorfico).

    Un decodificatore software (o un decodificatore hardware che produce l'output inviato al VMR) ha due opzioni per l'elaborazione di un'immagine anamorfica:

    1.  Ignorare questo flag e copiare il contenuto di VideoInfoHeader2 nella macchina virtuale. La macchina virtuale inserirà immagini da 4 x 3 a 16x9 se è impostata l'opzione AMCONTROL \_ PAD \_ TO \_ 16x9.
    2.  Riempire l'immagine di output in un'immagine 16x9 e rimuovere IL PAD AMCONTROL \_ \_ a \_ 16x9 bit.

La maggior parte dei decodificatori deve usare **GetMediaType** per rilevare una modifica del supporto sul pin di input e copiare il contenuto **VIDEOINFOHEADER2** (contenuto in **MPEG2INFOHEADER)** nel pin di output. Probabilmente elaelaborare solo il bit PanScan.

Il codice di esempio seguente illustra come copiare il **contenuto VIDEOINFOHEADER2** da un pin di input a un pin di output.


```C++
#include <dvdmedia.h>
HRESULT CopyMPeg2ToVideoInfoHeader2(CMediaSample* pInSample, CMediaSample* pOutSample)
{
    HRESULT hr = S_OK;
    // Check for a media type on the input sample.
    AM_MEDIA_TYPE* pInType;
    if (pInSample->GetMediaType(&pInType) == S_OK) 
    {
        // Make sure it's an MPEG2 Video format.
        if ((pInType->formattype == FORMAT_MPEG2_VIDEO) &&
            (pInType->cbFormat >= sizeof(MPEG2VIDEOINFO)))
        {
            hr = S_OK; // Initialize hr for the CMediaType constructor.
            CMediaType outType(*pInType, &hr);
            if (FAILED(hr))
            {
                DeleteMediaType( pInType );
                return hr;
            }

            // Set the format type GUID.
            outType.SetFormatType(&FORMAT_VideoInfo2);
                
            // Truncate the format block to include just the VIDEOINFOHEADER part.
            MPEG2VIDEOINFO *pMPeg2Header = (MPEG2VIDEOINFO*)pInType->pbFormat;
            BYTE *pVIH = (BYTE*)&pMPeg2Header->hdr;
            hr = (outType.SetFormat(pVIH, sizeof(VIDEOINFOHEADER2)) ? S_OK : E_OUTOFMEMORY);
            if (SUCCEEDED(hr))
            {
                hr = pOutSample->SetMediaType(&outType);
            }
        } 
        else 
        {
            ASSERT(FALSE); // Not a MPEG2 header.
            hr = VFW_E_INVALIDMEDIATYPE;
        }
        DeleteMediaType( pInType );
    } 

    return hr;
}
```



 

 



