---
description: L'interfaccia ISampleGrabber viene esposta dal filtro Sample Grabber. Consente a un'applicazione di recuperare singoli campioni multimediali mentre si spostano nel grafico dei filtri.
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: Interfaccia ISampleGrabber (Qedit.h)
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
ms.openlocfilehash: 485301d58da6ca48bf43414fd9907048943ab8868c514132e2887fef29e5d2b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817645"
---
# <a name="isamplegrabber-interface"></a>Interfaccia ISampleGrabber

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

**L'interfaccia ISampleGrabber** viene esposta dal [**filtro Sample Grabber.**](sample-grabber-filter.md) Consente a un'applicazione di recuperare singoli campioni multimediali mentre si spostano nel grafico dei filtri.

## <a name="members"></a>Membri

**L'interfaccia ISampleGrabber** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ISampleGrabber** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ISampleGrabber** include questi metodi.



| Metodo                                                                | Descrizione                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**GetConnectedMediaType**](isamplegrabber-getconnectedmediatype.md) | Recupera il tipo di supporto per la connessione sul pin di input di Sample Grabber.<br/>                                        |
| [**GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md)           | Recupera una copia dell'esempio ricevuto più di recente dal filtro.<br/>                                                 |
| [**GetCurrentSample**](isamplegrabber-getcurrentsample.md)           | Non implementato.<br/>                                                                                                       |
| [**SetBufferSamples**](isamplegrabber-setbuffersamples.md)           | Specifica se copiare i dati di esempio in un buffer mentre passano attraverso il filtro.<br/>                                     |
| [**SetCallback**](isamplegrabber-setcallback.md)                     | Specifica un metodo di callback da chiamare sugli esempi in ingresso.<br/>                                                               |
| [**SetMediaType**](isamplegrabber-setmediatype.md)                   | Specifica il tipo di supporto per la connessione sul pin di input di Sample Grabber.<br/>                                    |
| [**SetOneShot**](isamplegrabber-setoneshot.md)                       | Specifica se il filtro [**Sample Grabber**](sample-grabber-filter.md) si interrompe dopo che il filtro ha ricevuto un campione.<br/> |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso del grabber di esempio](using-the-sample-grabber.md)
</dt> </dl>

 

 
