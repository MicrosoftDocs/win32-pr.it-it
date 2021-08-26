---
description: Richiede di ottenere il contenuto di una trama affiancata come . File DDS (DirectDraw Surface).
MS-HAID: vspixengine.ITileRequest\_RequestTextureTileAsync\_EventID\_DWORD\_UINT\_UINT\_UINT\_UINT\_BSTR\_ITextureCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo ITileRequest::RequestTextureTileAsync
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E3F4FAC2-E7D9-4FDF-BE64-73D3EA175A8F
api_name:
- ITileRequest.RequestTextureTileAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0700be1f8d704a83dad39ee9b742a50baa3e9486
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631879"
---
# <a name="span-idvspixengineitilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dwordspanitilerequestrequesttexturetileasync-method"></a><span id="vspixengine.itilerequest_requesttexturetileasync_eventid_dword_uint_uint_uint_uint_bstr_itexturecallback_ptr_dword_dword"></span>Metodo ITileRequest::RequestTextureTileAsync

Richiede di ottenere il contenuto di una trama affiancata come . File DDS (DirectDraw Surface).

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestTextureTileAsync(
   EventID            eventID,
   DWORD              textureFileptr,
   UINT               tileSubresource,
   UINT               tileX,
   UINT               tileY,
   UINT               tileZ,
   BSTR               ddsFilename,
   ITextureCallback * pRequestCallback,
   DWORD              requestCookie,
   DWORD              progressIntervalMsecs
);
```

## <a name="parameters"></a>Parametri

*Eventid*   
Evento specificato a cui associare il contenuto del buffer (ad esempio, una destinazione di rendering può cambiare nel tempo).

*textureFileptr*   
Indirizzo dell'oggetto trama specificato.

*tileSubresource*   
Sottorisorsa specificata del riquadro.

*Tilex*   
Posizione X del riquadro specificata.

*tileY*   
Posizione Y del riquadro specificata.

*tileZ*   
Posizione Z del riquadro specificata.

*ddsFilename*   
Stringa COM che contiene il percorso del file con estensione dds in cui vengono scritti i risultati.

*pRequestCallback*   
Indirizzo del callback utilizzato per notificare i risultati all'host.

*requestCookie*   
Cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.

*progressIntervalMsecs*   
Non usato.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**ITileRequest**](/windows/desktop/direct3dtools/itilerequest)

 

 
