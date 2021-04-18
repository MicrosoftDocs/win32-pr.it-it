---
description: Buffer video non compressi
ms.assetid: be5ec8a8-2d0b-401b-9d05-fdb87ad8c864
title: Buffer video non compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24eda19136bf2dd7bc77f95d0efa6c48ca96e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310183"
---
# <a name="uncompressed-video-buffers"></a>Buffer video non compressi

Questo articolo descrive come usare i buffer multimediali che contengono frame video non compressi. In ordine di preferenza sono disponibili le opzioni seguenti. Non tutti i buffer multimediali supportano ogni opzione.

1.  Utilizzare la superficie Direct3D sottostante. (Si applica solo ai frame video archiviati nelle superfici Direct3D.)
2.  Usare l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .
3.  Usare l'interfaccia [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .

## <a name="use-the-underlying-direct3d-surface"></a>Usare la superficie Direct3D sottostante

Il fotogramma video potrebbe essere archiviato all'interno di una superficie Direct3D. In tal caso, è possibile ottenere un puntatore all'area chiamando [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) o [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) sull'oggetto buffer multimediale. Usare il servizio buffer di identificazione del servizio \_ \_ . Questo approccio è consigliato quando il componente che accede al frame video è progettato per l'uso di Direct3D. Ad esempio, un decodificatore video che supporta l'accelerazione video DirectX deve usare questo approccio.

Il codice seguente illustra come ottenere il puntatore **IDirect3DSurface9** da un buffer multimediale.


```C++
IDirect3DSurface9 *pSurface = NULL;

hr = MFGetService(
    pBuffer, 
    MR_BUFFER_SERVICE,
    __uuidof(IDirect3DSurface9), 
    (void**)&pSurface
    );

if (SUCCEEDED(hr))
{
    // Call IDirect3DSurface9 methods.
}
```



Gli oggetti seguenti supportano il servizio del **\_ \_ servizio buffer di Mr** :

-   [Buffer della superficie DirectX](directx-surface-buffer.md)
-   [Esempi video](video-samples.md)

## <a name="use-the-imf2dbuffer-interface"></a>Usare l'interfaccia IMF2DBuffer

Se il fotogramma video non è archiviato in una superficie Direct3D o il componente non è progettato per l'utilizzo di Direct3D, il successivo metodo consigliato per accedere al frame video consiste nell'eseguire una query sul buffer per l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) . Questa interfaccia è progettata specificamente per i dati di immagine. Per ottenere un puntatore a questa interfaccia, chiamare **QueryInterface** sul buffer multimediale. Non tutti gli oggetti buffer multimediali espongono questa interfaccia. Tuttavia, se un buffer multimediale espone l'interfaccia **IMF2DBuffer** , è consigliabile usare tale interfaccia per accedere ai dati, se possibile, invece di usare [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer). È comunque possibile usare l'interfaccia **IMFMediaBuffer** , ma potrebbe essere meno efficiente.

1.  Chiamare **QueryInterface** sul buffer multimediale per ottenere l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) .
2.  Chiamare [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) per accedere alla memoria per il buffer. Questo metodo restituisce un puntatore al primo byte della prima riga di pixel. Restituisce anche lo stride dell'immagine, ovvero il numero di byte dall'inizio di una riga di pixel all'inizio della riga successiva. Il buffer potrebbe contenere byte di riempimento dopo ogni riga di pixel, quindi lo stride potrebbe essere più ampio della larghezza dell'immagine in byte. Lo stride può anche essere negativo se l'immagine è orientata dal basso verso l'alto nella memoria. Per ulteriori informazioni, vedere [Image stride](image-stride.md).
3.  Mantieni il buffer bloccato solo quando devi accedere alla memoria. Sbloccare il buffer chiamando [**IMF2DBuffer:: Unlock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-unlock2d).

Non tutti i buffer multimediali implementano l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) . Se il buffer multimediale non implementa questa interfaccia, ovvero l'oggetto buffer restituisce E \_ nointerface nel passaggio 1, è necessario usare l'interfaccia [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) Interface, descritta di seguito.

## <a name="use-the-imfmediabuffer-interface"></a>Usare l'interfaccia IMFMediaBuffer

Se un buffer multimediale non espone l'interfaccia [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , usare l'interfaccia [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) . La semantica generale di questa interfaccia è descritta nell'argomento [uso dei buffer multimediali](working-with-media-buffers.md).

1.  Chiamare **QueryInterface** sul buffer multimediale per ottenere l'interfaccia [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .
2.  Chiamare [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) per accedere alla memoria del buffer. Questo metodo restituisce un puntatore alla memoria del buffer. Quando si usa il metodo **Lock** , lo stride è sempre lo stride minimo per il formato video in questione, senza ulteriori byte di riempimento.
3.  Mantieni il buffer bloccato solo quando devi accedere alla memoria. Sbloccare il buffer chiamando [**IMFMediaBuffer:: Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock).

È sempre consigliabile evitare di chiamare [**IMFMediaBuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) se il buffer espone [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer), perché il metodo **Lock** può forzare l'oggetto buffer sul frame video in un blocco di memoria contiguo e quindi nuovamente. D'altra parte, se il buffer non supporta **IMF2DBuffer**, **IMFMediaBuffer:: Lock** probabilmente non genererà una copia.

Calcolare lo stride minimo dal tipo di supporto come segue:

-   Lo stride minimo potrebbe essere archiviato nell'attributo [**\_ \_ \_ stride predefinito di MF mt**](mf-mt-default-stride-attribute.md) .
-   Se l' **attributo \_ \_ \_ stride predefinito di MF mt** non è impostato, chiamare la funzione [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) per calcolare lo stride per i formati video più comuni.
-   Se la funzione [**MFGetStrideForBitmapInfoHeader**](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader) non riconosce il formato, è necessario calcolare lo stride in base alla definizione del formato. In tal caso, non esiste alcuna regola generale; è necessario avere informazioni dettagliate sulla definizione del formato.

Il codice seguente illustra come ottenere lo stride predefinito per i formati video più comuni.


```C++
HRESULT GetDefaultStride(IMFMediaType *pType, LONG *plStride)
{
    LONG lStride = 0;

    // Try to get the default stride from the media type.
    HRESULT hr = pType->GetUINT32(MF_MT_DEFAULT_STRIDE, (UINT32*)&lStride);
    if (FAILED(hr))
    {
        // Attribute not set. Try to calculate the default stride.

        GUID subtype = GUID_NULL;

        UINT32 width = 0;
        UINT32 height = 0;

        // Get the subtype and the image size.
        hr = pType->GetGUID(MF_MT_SUBTYPE, &subtype);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = MFGetStrideForBitmapInfoHeader(subtype.Data1, width, &lStride);
        if (FAILED(hr))
        {
            goto done;
        }

        // Set the attribute for later reference.
        (void)pType->SetUINT32(MF_MT_DEFAULT_STRIDE, UINT32(lStride));
    }

    if (SUCCEEDED(hr))
    {
        *plStride = lStride;
    }

done:
    return hr;
}
```



A seconda dell'applicazione, è possibile sapere in anticipo se un determinato buffer multimediale supporta [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , ad esempio se è stato creato il buffer. In caso contrario, è necessario essere pronti a utilizzare una delle due interfacce del buffer.

Nell'esempio seguente viene illustrata una classe helper che nasconde alcuni di questi dettagli. Questa classe dispone di un metodo LockBuffer che chiama [**Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) o [**Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) e restituisce un puntatore all'inizio della prima riga di pixel. Questo comportamento corrisponde al metodo **Lock2D** . Il metodo LockBuffer accetta lo stride predefinito come parametro di input e restituisce lo stride effettivo come parametro di output.


```C++
class CBufferLock
{
public:
    CBufferLock(IMFMediaBuffer *pBuffer) : m_p2DBuffer(NULL), m_bLocked(FALSE)
    {
        m_pBuffer = pBuffer;
        m_pBuffer->AddRef();

        m_pBuffer->QueryInterface(IID_IMF2DBuffer, (void**)&m_p2DBuffer);
    }

    ~CBufferLock()
    {
        UnlockBuffer();
        SafeRelease(&m_pBuffer);
        SafeRelease(&m_p2DBuffer);
    }

    HRESULT LockBuffer(
        LONG  lDefaultStride,    // Minimum stride (with no padding).
        DWORD dwHeightInPixels,  // Height of the image, in pixels.
        BYTE  **ppbScanLine0,    // Receives a pointer to the start of scan line 0.
        LONG  *plStride          // Receives the actual stride.
        )
    {
        HRESULT hr = S_OK;

        // Use the 2-D version if available.
        if (m_p2DBuffer)
        {
            hr = m_p2DBuffer->Lock2D(ppbScanLine0, plStride);
        }
        else
        {
            // Use non-2D version.
            BYTE *pData = NULL;

            hr = m_pBuffer->Lock(&pData, NULL, NULL);
            if (SUCCEEDED(hr))
            {
                *plStride = lDefaultStride;
                if (lDefaultStride < 0)
                {
                    // Bottom-up orientation. Return a pointer to the start of the
                    // last row *in memory* which is the top row of the image.
                    *ppbScanLine0 = pData + abs(lDefaultStride) * (dwHeightInPixels - 1);
                }
                else
                {
                    // Top-down orientation. Return a pointer to the start of the
                    // buffer.
                    *ppbScanLine0 = pData;
                }
            }
        }

        m_bLocked = (SUCCEEDED(hr));

        return hr;
    }
    
    void UnlockBuffer()
    {
        if (m_bLocked)
        {
            if (m_p2DBuffer)
            {
                (void)m_p2DBuffer->Unlock2D();
            }
            else
            {
                (void)m_pBuffer->Unlock();
            }
            m_bLocked = FALSE;
        }
    }

private:
    IMFMediaBuffer  *m_pBuffer;
    IMF2DBuffer     *m_p2DBuffer;

    BOOL            m_bLocked;
};
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stride immagine](image-stride.md)
</dt> <dt>

[Buffer multimediali](media-buffers.md)
</dt> </dl>

 

 



