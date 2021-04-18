---
description: Funzione proxy per il metodo CreateDecoderFromFilename.
ms.assetid: 12c60899-0fe0-47d0-9026-48c74df328ef
title: Funzione IWICImagingFactory_CreateDecoderFromFilename_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateDecoderFromFilename_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3497d71475198d035a496909e65c47df6c5f8b8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319121"
---
# <a name="iwicimagingfactory_createdecoderfromfilename_proxy-function"></a>IWICImagingFactory \_ CreateDecoderFromFilename- \_ funzione proxy

Funzione proxy per il metodo [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICImagingFactory_CreateDecoderFromFilename_Proxy(
  _In_        IWICImagingFactory  *pFactory,
  _In_        LPCWSTR             wzFilename,
  _In_  const GUID                *pguidVendor,
  _In_        DWORD               dwDesiredAccess,
  _In_        WICDecodeOptions    metadataOptions,
  _Out_       IWICBitmapDecoder   **ppIDecoder
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFactory* \[ in\]
</dt> <dd>

Tipo: **IWICImagingFactory \** _

</dd> <dt>

_wzFilename * \[ in\]
</dt> <dd>

Tipo: **LPCWSTR**

Puntatore a una stringa con terminazione null che specifica il nome di un oggetto da creare o aprire.

</dd> <dt>

*pguidVendor* \[ in\]
</dt> <dd>

Tipo: **const \* GUID* _

GUID del fornitore per il decodificatore.

</dd> <dt>

_dwDesiredAccess * \[ in\]
</dt> <dd>

Tipo: **DWORD**

Accesso all'oggetto, che può essere letto, scritto o entrambi.

Per ulteriori informazioni, vedere file di [sicurezza e accesso \[ \] ai file](../fileio/file-security-and-access-rights.md).

</dd> <dt>

*metadataOptions* \[ in\]
</dt> <dd>

Tipo: **[ **WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions)**

[**WICDecodeOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) da utilizzare durante la creazione del decodificatore.

</dd> <dt>

*ppIDecoder* \[ out\]
</dt> <dd>

Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\*\***

Puntatore che riceve un puntatore al nuovo [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, \[ solo app desktop di Windows Vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

