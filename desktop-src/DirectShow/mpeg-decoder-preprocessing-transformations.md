---
description: Trasformazioni di pre-elaborazione del decodificatore MPEG
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Trasformazioni di pre-elaborazione del decodificatore MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70df51b26ec3fa25d67a03a4e494869a2f25760
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747055"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a>Trasformazioni di pre-elaborazione del decodificatore MPEG

**Letterbox e PanScan**

L'immagine 4x3 può essere costituita dall'imbottitura della parte superiore e inferiore dell'immagine (detta immagine letterbox) o dall'estrazione di una parte 4x3 dell'immagine (denominata immagine PanScan). I menu e i flussi di sottoimmagine sono sovrapposti sopra l'immagine video finale. Le immagini del rapporto 16x9 vengono archiviate in un formato 4x3 Anamorfo. L'allungamento del video di origine 720x480 4x3 proporzionale a una proporzione 16x9 rappresenta l'immagine dell'aspetto 16x9 originale.

Di seguito è riportata una descrizione del modo in cui vengono visualizzate correttamente le modalità e le relative caratteristiche principali:

-   **Widescreen:** Il video di origine esteso nell'area 16x9 più grande della finestra di output. Le evidenziazioni sono relative all'interno dell'area 16x9. Le barre nere devono essere aggiunte alla parte superiore e inferiore o ai lati per mantenere un'area 16x9.
-   **Panoramica dell'analisi:** Dal video 16x9, usare l'offset orizzontale specificato nel flusso MPEG2 per estrarre una sottofinestra 4x3. Posizionare la sottofinestra 4x3 nell'area 4x3 più grande della finestra client di output. Le coordinate dell'evidenziazione sono relative alla finestra di output di 4x3 e non hanno alcuna relazione con il video 16x9 di origine. Le barre nere devono essere aggiunte alla parte superiore e inferiore o ai lati per mantenere un'area 4x3.
-   **Letterbox:** Calcola l'area 4x3 più grande della finestra di output. Le barre nere devono essere aggiunte alla parte superiore e inferiore o ai lati per mantenere un'area 4x3. Il video 4x3 Anamorfo di origine (che rappresenta un'immagine 16x9) viene inserito nella sottofinestra 16x9 più grande all'interno dell'area 4x3. Le barre nere devono essere aggiunte alla parte superiore e inferiore della sottofinestra per mantenere un'area 16x9. Le coordinate dell'evidenziazione sono relative all'area 4x3 e non hanno alcuna relazione con il video 16x9 di origine. È possibile che un disco specifichi un'evidenziazione che si trova al di fuori dell'area di 16x9 (ma ancora nella finestra 4x3). Per 4x3 video, il video viene inserito nell'area di output 4x3 più grande della finestra client di output. Le barre nere devono essere aggiunte alla parte superiore e inferiore o ai lati per mantenere un'area 4x3.

**Pre-elaborazione MPEG con DVD Navigator e VMR**

Al momento, al decodificatore viene passato un \_ \_ tipo di supporto video MPEG2 di formato (il cui blocco di formato punta a una struttura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) ). Nei pin di output, il decodificatore produce un formato \_ VideoInfo2 tipo di supporto, il cui blocco di formato punta a una struttura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Il campo **dwReserved** della struttura è stato rinominato in flag **dwControls** .

Il membro **dwControlFlags** conterrà ora i nuovi bit.



|                          |            |
|--------------------------|------------|
| AMCONTROL \_ usato          | 0x00000001 |
| AMCONTROL \_ Pad \_ \_ 4x3  | 0x00000002 |
| AMCONTROL \_ Pad \_ \_ 16x9 | 0x00000004 |



 

AMCONTROL \_ usato per verificare se questi nuovi flag sono supportati. Un filtro di origine deve impostare il \_ flag usato AMCONTROL e verificare se QueryAccept (mediaType) ha esito positivo sul pin downstream. Se viene rifiutato, non è possibile usare i flag AMCONTROL e dwReserved1 deve essere impostato su 0.

AMCONTROL \_ Pad \_ \_ 4x3 indica che l'immagine deve essere riempita e visualizzata in un'area 4x3.

AMCONTROL \_ Pad \_ \_ 16x9 indica che l'immagine deve essere riempita e visualizzata in un'area 16x9.

Il decodificatore deve copiare o elaborare in modo cieco i bit. Se il decodificatore esegue il letterboxing, deve modificare le proporzioni dei pixel, riempire l'immagine e rimuovere i bit AMCONTROL corrispondenti \_ \* .

MPEG2VIDEOINFO. dwFlags contiene ora tre flag per il controllo della modalità di visualizzazione del contenuto:

-   `AMMPEG2_DoPanScan (0x00000001)`: Se questo flag è impostato, il decodificatore MPEG-2 video dovrebbe ritagliare l'immagine di output in base ai vettori di analisi panoramica nell' \_ \_ estensione per la visualizzazione dell'immagine e modificare le proporzioni dell'immagine in 4x3. VMR non deve ricevere un esempio 16x9 con questo flag. Un'implementazione semplice potrebbe modificare il rettangolo di origine per indicare un'area di origine di 540 Wide con un bordo sinistro uguale all'offset di visualizzazione nell'estensione per la visualizzazione dell'immagine \_ \_ .
-   `AMMPEG2_LetterboxAnalogOut (0x00000020)`: Quando un decodificatore hardware Visualizza questo flusso in un output video (in genere un connettore SVIDEO sulla scheda), deve applicare le regole per la visualizzazione di un esempio 16x9 in una visualizzazione 4x3.

    Un decodificatore software (o un decodificatore hardware che produce output inviato a VMR) dispone di due opzioni per l'elaborazione delle immagini:

    1.  Ignorare questo flag e passare il contenuto di VideoInfoHeader2 a VMR (il \_ flag AMCONTROL \_ \_ su 4x3 sarà già impostato dal [navigatore DVD](dvd-navigator-filter.md) nell'esempio). VMR incontrerà un esempio video 16x9 con AMCONTROL \_ Pad \_ per \_ 4x3 flag impostati e un flusso di sottoimmagine 4x3. L'applicazione deve impostare i rettangoli di destinazione normalizzati di output dei due flussi in modo che abbiano la stessa larghezza.
    2.  Convertire il flusso Anamorfo in un'immagine 4x3, affiancando la parte superiore e inferiore dell'immagine e impostando le proporzioni dell'immagine su 4x3 (vedere la cassetta post precedente) e rimuovendo il \_ riquadro AMCONTROL \_ in \_ 4x3 bit da VIDEOINFOHEADER2.

    I decodificatori DirectXVA che combinano i flussi video e subpicture dovranno elaborare questo flag. Se l'hardware non è in grado di ridimensionare la sottoimmagine sfumata, il decodificatore deve produrre un flusso di sottoimmagine separato affinché VMR si mescoli con il video.

-   `AMMPEG2_WidescreenAnalogOut (0x00000200)`: Quando un decodificatore hardware Visualizza questo flusso in un output video (in genere un connettore SVIDEO sulla scheda), deve presupporre una visualizzazione 16x9 (Anamorfo).

    Un decodificatore software (o un decodificatore hardware che produce output inviato a VMR) dispone di due opzioni per l'elaborazione di un'immagine anamorfica:

    1.  Ignorare questo flag e copiare il contenuto di VideoInfoHeader2 in VMR. VMR comporterà il riempimento delle immagini 4x3 in 16x9 se il \_ riquadro AMCONTROL è \_ \_ impostato su 16x9.
    2.  Aggiungere l'immagine di output a un'immagine 16x9 e rimuovere AMCONTROL \_ Pad \_ \_ 16x9 bit.

La maggior parte dei decodificatori deve usare **GetMediaType** per rilevare una modifica del supporto del PIN di input e copiare il contenuto di **VIDEOINFOHEADER2** (contenuto nel **MPEG2INFOHEADER**) nel pin di output. Probabilmente verranno elaborati solo il bit PanScan.

Il codice di esempio seguente mostra come copiare il contenuto di **VIDEOINFOHEADER2** da un pin di input in un pin di output.


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



 

 



