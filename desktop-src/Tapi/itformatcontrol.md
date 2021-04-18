---
description: L'interfaccia ITFormatControl espone metodi che consentono a un'applicazione di recuperare informazioni sul formato di un flusso di ricezione o trasmissione per una chiamata.
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: Interfaccia ITFormatControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0735e7bfaf5222948cef5e047530a35cb19a125
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332005"
---
# <a name="itformatcontrol-interface"></a>Interfaccia ITFormatControl

\[ Questa interfaccia non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITFormatControl** espone metodi che consentono a un'applicazione di recuperare informazioni sul formato di un flusso di ricezione o trasmissione per una chiamata.

Questa interfaccia viene implementata da [H323 msp](h323-msp.md) ed è esposta solo quando una chiamata utilizza questo provider di servizi.

## <a name="members"></a>Membri

L'interfaccia **ITFormatControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITFormatControl** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITFormatControl** dispone di questi metodi.



| Metodo                                                                     | Descrizione                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**GetCurrentFormat**](itformatcontrol-getcurrentformat.md)               | Ottiene il formato multimediale del flusso corrente.<br/>                        |
| [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) | Ottiene il numero di funzionalità associate al formato corrente.<br/> |
| [**GetStreamCaps**](itformatcontrol-getstreamcaps.md)                     | Ottiene le funzionalità associate a un indice di formato specificato.<br/>         |
| [**ReleaseFormat**](itformatcontrol-releaseformat.md)                     | Rilascia la struttura associata al formato.<br/>                  |
| [**ReOrderCapabilities**](itformatcontrol-reordercapabilities.md)         | Imposta un nuovo ordine per le funzionalità di formattazione.<br/>                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

