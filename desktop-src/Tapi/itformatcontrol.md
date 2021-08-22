---
description: L'interfaccia ITFormatControl espone metodi che consentono a un'applicazione di recuperare informazioni relative al formato di un flusso di ricezione o trasmissione per una chiamata.
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: Interfaccia ITFormatControl (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab42a9cacdf7986a652fff4e15195fec5f6b1aa319f06b631ee992541db40b82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406051"
---
# <a name="itformatcontrol-interface"></a>Interfaccia ITFormatControl

\[Questa interfaccia non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

**L'interfaccia ITFormatControl** espone metodi che consentono a un'applicazione di recuperare informazioni relative al formato di un flusso di ricezione o trasmissione per una chiamata.

Questa interfaccia viene implementata dal provider di servizi [H323 ed](h323-msp.md) è esposta solo quando una chiamata usa questo provider di servizi.

## <a name="members"></a>Membri

**L'interfaccia ITFormatControl** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITFormatControl** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITFormatControl** include questi metodi.



| Metodo                                                                     | Descrizione                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**GetCurrentFormat**](itformatcontrol-getcurrentformat.md)               | Ottiene il formato multimediale del flusso corrente.<br/>                        |
| [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) | Ottiene il numero di funzionalità associate al formato corrente.<br/> |
| [**GetStreamCaps**](itformatcontrol-getstreamcaps.md)                     | Ottiene le funzionalità associate a un indice di formato specificato.<br/>         |
| [**ReleaseFormat**](itformatcontrol-releaseformat.md)                     | Rilascia la struttura associata al formato.<br/>                  |
| [**ReOrderCapabilities**](itformatcontrol-reordercapabilities.md)         | Imposta un nuovo ordine per le funzionalità di formato.<br/>                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

