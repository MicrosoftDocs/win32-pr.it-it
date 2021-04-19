---
description: ITStreamQualityControl espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo della qualità del flusso.
ms.assetid: b9ecf24a-c87e-44a6-9e20-aa7bf7619314
title: Interfaccia ITStreamQualityControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a85eccc907ef2c8f4c0b67c2a32244004dbdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329324"
---
# <a name="itstreamqualitycontrol-interface"></a>Interfaccia ITStreamQualityControl

\[ Questa interfaccia non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

**ITStreamQualityControl** espone metodi che consentono a un'applicazione di ottenere e impostare parametri per il controllo della qualità del flusso.

Questa interfaccia viene implementata da [IPConf msp](ipconf-msp.md) e [H323 msp](h323-msp.md). Viene esposto solo quando una chiamata utilizza questi provider di servizi.

## <a name="members"></a>Membri

L'interfaccia **ITStreamQualityControl** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITStreamQualityControl** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITStreamQualityControl** dispone di questi metodi.



| Metodo                                              | Descrizione                                                                                                 |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**Ottieni**](itstreamqualitycontrol-get.md)           | Ottiene il valore di una [proprietà di qualità del flusso](streamqualityproperty.md)specificata.<br/>                  |
| [**GetRange**](itstreamqualitycontrol-getrange.md) | Ottiene l'intervallo di valori validi per una determinata [proprietà di qualità del flusso](streamqualityproperty.md).<br/> |
| [**Set**](itstreamqualitycontrol-set.md)           | Imposta il valore di una [proprietà di qualità del flusso](streamqualityproperty.md)specificata.<br/>                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

