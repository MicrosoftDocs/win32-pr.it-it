---
description: L'interfaccia ITCallQualityControl espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo della qualità della chiamata.
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: Interfaccia ITCallQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447e2f34db76ba15ecaec9e7bc03a0d2d398c493
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328237"
---
# <a name="itcallqualitycontrol-interface"></a>Interfaccia ITCallQualityControl

\[ Questa interfaccia non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITCallQualityControl** espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo della qualità della chiamata.

Questa interfaccia viene implementata da [IPConf msp](ipconf-msp.md) e [H323 msp](h323-msp.md). Viene esposto solo quando una chiamata utilizza questi provider di servizi.

## <a name="members"></a>Membri

L'interfaccia **ITCallQualityControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITCallQualityControl** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITCallQualityControl** dispone di questi metodi.



| Metodo                                            | Descrizione                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [**Ottieni**](itcallqualitycontrol-get.md)           | Ottiene il valore di una [proprietà del controllo della qualità della chiamata](callqualityproperty.md)specificata.<br/>                  |
| [**GetRange**](itcallqualitycontrol-getrange.md) | Ottiene l'intervallo di valori validi per una determinata [proprietà del controllo di qualità della chiamata](callqualityproperty.md).<br/> |
| [**Set**](itcallqualitycontrol-set.md)           | Imposta il valore di una [proprietà del controllo della qualità della chiamata](callqualityproperty.md)specificata.<br/>                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

