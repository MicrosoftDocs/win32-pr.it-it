---
description: L'interfaccia ITCallQualityControl espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo della qualità delle chiamate.
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: Interfaccia ITCallQualityControl (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cb31452f6f4693e8bfbf725a5ddae7d7305868c2603806895c98e16df4d3e86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061009"
---
# <a name="itcallqualitycontrol-interface"></a>Interfaccia ITCallQualityControl

\[Questa interfaccia non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

**L'interfaccia ITCallQualityControl** espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo della qualità delle chiamate.

Questa interfaccia viene implementata da [IPConf MSP](ipconf-msp.md) e [H323 MSP.](h323-msp.md) Viene esposto solo quando una chiamata utilizza questi provider di servizi.

## <a name="members"></a>Membri

**L'interfaccia ITCallQualityControl** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITCallQualityControl** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITCallQualityControl** include questi metodi.



| Metodo                                            | Descrizione                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**Ottieni**](itcallqualitycontrol-get.md)           | Ottiene il valore di una determinata proprietà [del controllo qualità delle chiamate.](callqualityproperty.md)<br/>                  |
| [**GetRange**](itcallqualitycontrol-getrange.md) | Ottiene l'intervallo di valori validi per una determinata proprietà [del controllo qualità delle chiamate.](callqualityproperty.md)<br/> |
| [**Impostare**](itcallqualitycontrol-set.md)           | Imposta il valore di una determinata proprietà [del controllo qualità delle chiamate.](callqualityproperty.md)<br/>                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

