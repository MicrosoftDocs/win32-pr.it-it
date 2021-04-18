---
description: L'interfaccia ISampleGrabber viene esposta dal filtro Grabber di esempio. Consente a un'applicazione di recuperare singoli esempi di supporti mentre passano attraverso il grafico del filtro.
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: Interfaccia ISampleGrabber (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f6e923032e74f88dceb1c2465e27dab9423bae1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324414"
---
# <a name="isamplegrabber-interface"></a>Interfaccia ISampleGrabber

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L'interfaccia **ISampleGrabber** viene esposta dal filtro [**grabber di esempio**](sample-grabber-filter.md) . Consente a un'applicazione di recuperare singoli esempi di supporti mentre passano attraverso il grafico del filtro.

## <a name="members"></a>Membri

L'interfaccia **ISampleGrabber** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ISampleGrabber** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ISampleGrabber** dispone di questi metodi.



| Metodo                                                                | Descrizione                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) | Recupera il tipo di supporto per la connessione sul pin di input di Sample Grabber.<br/>                                        |
| [**GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md)           | Recupera una copia dell'esempio che il filtro ha ricevuto più di recente.<br/>                                                 |
| [**GetCurrentSample**](isamplegrabber-getcurrentsample.md)           | Non implementato.<br/>                                                                                                       |
| [**SetBufferSamples**](isamplegrabber-setbuffersamples.md)           | Specifica se copiare i dati di esempio in un buffer mentre passa attraverso il filtro.<br/>                                     |
| [**SetCallback**](isamplegrabber-setcallback.md)                     | Specifica un metodo di callback da chiamare sugli esempi in arrivo.<br/>                                                               |
| [**SetMediaType**](isamplegrabber-setmediatype.md)                   | Specifica il tipo di supporto per la connessione sul pin di input del grabber di esempio.<br/>                                    |
| [**SetOneShot**](isamplegrabber-setoneshot.md)                       | Specifica se il filtro [**grabber di esempio**](sample-grabber-filter.md) si arresta dopo la ricezione di un campione da parte del filtro.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso del grabber di esempio](using-the-sample-grabber.md)
</dt> </dl>

 

 
