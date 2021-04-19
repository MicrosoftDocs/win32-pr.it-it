---
description: Il metodo GetBitmapBits recupera un frame video al momento del supporto specificato. Il frame restituito è sempre in formato RGB a 24 bit.
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: 'Metodo IMediaDet:: GetBitmapBits (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetBitmapBits
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95aea5281f77b32868e0f0856bc63063e4f08639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332028"
---
# <a name="imediadetgetbitmapbits-method"></a>Metodo IMediaDet:: GetBitmapBits

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetBitmapBits` metodo recupera un frame video al momento del supporto specificato. Il frame restituito è sempre in formato RGB a 24 bit.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetBitmapBits(
   double StreamTime,
   long   *pBufferSize,
   char   *pBuffer,
   long   Width,
   long   Height
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StreamTime* 
</dt> <dd>

Tempo di recupero del fotogramma video, in secondi.

</dd> <dt>

*pBufferSize* 
</dt> <dd>

Riceve le dimensioni del buffer richieste. Se *pbuffer* è **null**, la variabile riceve la dimensione del buffer necessaria per recuperare il frame. Se *pbuffer* non è **null**, questo parametro viene ignorato.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Puntatore a un buffer che riceve una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguita dai bit DIB.

</dd> <dt>

*Larghezza* 
</dt> <dd>

Larghezza dell'immagine video, in pixel.

</dd> <dt>

*Altezza* 
</dt> <dd>

Altezza dell'immagine video, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I possibili valori sono i seguenti:



| Codice restituito                                                                                             | Descrizione                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                    | Esito positivo.<br/>                                                                               |
| <dl> <dt>**E \_ NOinterface**</dt> </dl>           | Non è stato possibile aggiungere il filtro [**grabber di esempio**](sample-grabber-filter.md) al grafo.<br/> |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>           | Memoria insufficiente.<br/>                                                                   |
| <dl> <dt>**\_puntatore E**</dt> </dl>               | Errore puntatore **null** .<br/>                                                                |
| <dl> <dt>**E \_ imprevisto**</dt> </dl>            | Errore imprevisto.<br/>                                                                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo di supporto non valido.<br/>                                                                    |



 

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, impostare il nome e il flusso del file chiamando [**IMediaDet::p UT \_ filename**](imediadet-put-filename.md) e [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md).

Per determinare le dimensioni del buffer necessario, chiamare questo metodo con *pbuffer* uguale a **null**. La dimensione viene restituita nella variabile a cui punta *pBufferSize*. Creare quindi il buffer e chiamare di nuovo il metodo, con *pbuffer* uguale all'indirizzo del buffer. Quando il metodo viene restituito, il buffer contiene una struttura **BITMAPINFOHEADER** seguita dalla bitmap. La bitmap viene ridimensionata alle dimensioni specificate nei parametri *Width* e *Height* .

Questo metodo inserisce il rilevatore multimediale in modalità di cattura bitmap. Una volta che questo metodo è stato chiamato, i vari metodi di informazioni sui flussi in **IMediaDet** non funzionano, a meno che non si crei una nuova istanza del rilevamento multimediale.

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="examples"></a>Esempio

Il codice seguente usa il `GetBitmapBits` metodo per creare una bitmap indipendente dal dispositivo.


```C++
long size;
hr = pDet->GetBitmapBits(0, &size, 0, width, height);
if (SUCCEEDED(hr)) 
{
    char *pBuffer = new char[size];
    if (!pBuffer)
        return E_OUTOFMEMORY;
    try {
        hr = pDet->GetBitmapBits(0, 0, pBuffer, width, height);
    }
    catch (...) {
        delete [] pBuffer;
        throw;
    }
    if (SUCCEEDED(hr))
    {
        BITMAPINFOHEADER *bmih = (BITMAPINFOHEADER*)pBuffer;
        HDC hdcDest = GetDC(0);
        
        // Find the address of the start of the image data.
        void *pData = pBuffer + sizeof(BITMAPINFOHEADER);
        
        // Note: In general a BITMAPINFOHEADER can include extra color
        // information at the end, so calculating the offset to the image
        // data is not generally correct. However, the IMediaDet interface
        // always returns an RGB-24 image with no extra color information.
        
        BITMAPINFO bmi;
        ZeroMemory(&bmi, sizeof(BITMAPINFO));
        CopyMemory(&(bmi.bmiHeader), bmih, sizeof(BITMAPINFOHEADER));
        HBITMAP hBitmap = CreateDIBitmap(hdcDest, bmih, CBM_INIT, 
            pData, &bmi, DIB_RGB_COLORS);
    }
    delete[] pBuffer;
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IMediaDet**](imediadet.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




