---
description: Il metodo GetBitmapBits recupera un fotogramma video all'ora del supporto specificata. Il frame restituito è sempre in formato RGB a 24 bit.
ms.assetid: b51df9d1-9c54-41bd-b0f8-ec290525deca
title: Metodo IMediaDet::GetBitmapBits (Qedit.h)
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
ms.openlocfilehash: 5c4a7332580d4e9a9fece5a66d390753566fbf54c615699663256c463cb401b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792001"
---
# <a name="imediadetgetbitmapbits-method"></a>Metodo IMediaDet::GetBitmapBits

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `GetBitmapBits` metodo recupera un fotogramma video all'ora del supporto specificata. Il frame restituito è sempre in formato RGB a 24 bit.

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

Ora in cui recuperare il fotogramma video, espresso in secondi.

</dd> <dt>

*pBufferSize* 
</dt> <dd>

Riceve le dimensioni del buffer necessarie. Se *pBuffer* è **NULL,** la variabile riceve le dimensioni del buffer necessarie per recuperare il frame. Se *pBuffer* non è **NULL,** questo parametro viene ignorato.

</dd> <dt>

*pBuffer* 
</dt> <dd>

Puntatore a un buffer che riceve una [**struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) seguita dai bit DIB.

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

Restituisce un **valore HRESULT.** I possibili valori sono i seguenti:



| Codice restituito                                                                                             | Descrizione                                                                                       |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                    | Operazione completata.<br/>                                                                               |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl>           | Impossibile aggiungere il [**filtro Grabber**](sample-grabber-filter.md) di esempio al grafico.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>           | Memoria insufficiente.<br/>                                                                   |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>               | Errore del puntatore **NULL.**<br/>                                                                |
| <dl> <dt>**E \_ IMPREVISTO**</dt> </dl>            | Errore imprevisto.<br/>                                                                      |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl> | Tipo di supporto non valido.<br/>                                                                    |



 

## <a name="remarks"></a>Commenti

Prima di chiamare questo metodo, impostare il nome file e il flusso chiamando [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) e [**IMediaDet::p ut \_ CurrentStream**](imediadet-put-currentstream.md).

Per determinare le dimensioni del buffer necessarie, chiamare questo metodo con *pBuffer* uguale a **NULL.** Le dimensioni vengono restituite nella variabile a cui punta *pBufferSize*. Creare quindi il buffer e chiamare di nuovo il metodo , con *pBuffer* uguale all'indirizzo del buffer. Quando il metodo viene restituito, il buffer contiene una **struttura BITMAPINFOHEADER** seguita dalla bitmap. La bitmap viene ridimensionata in base alle dimensioni specificate nei *parametri Width* *e Height.*

Questo metodo imposta il rilevatore multimediale in modalità di cattura bitmap. Dopo aver chiamato questo metodo, i vari metodi di informazioni sul flusso in **IMediaDet** non funzionano, a meno che non si crei una nuova istanza del rilevatore di supporti.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

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
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IMediaDet**](imediadet.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




