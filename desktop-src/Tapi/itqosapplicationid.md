---
description: L'interfaccia ITQOSApplicationID espone un metodo che consente a un'applicazione di ottenere l'identificatore QOS per la chiamata corrente.
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: Interfaccia ITQOSApplicationID (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d4067d7a476e2a402c278b22dcee21b6542919396178350e73017d56ba92258
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126281"
---
# <a name="itqosapplicationid-interface"></a>Interfaccia ITQOSApplicationID

\[Questa interfaccia non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

**L'interfaccia ITQOSApplicationID** espone un metodo che consente a un'applicazione di ottenere l'identificatore QOS per la chiamata corrente.

Questa interfaccia viene implementata da [IPConf MSP](ipconf-msp.md) ed è esposta solo quando una chiamata utilizza ipconferenza.

## <a name="members"></a>Membri

**L'interfaccia ITQOSApplicationID** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITQOSApplicationID** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITQOSApplicationID** include questi metodi.



| Metodo                                                                | Descrizione                         |
|:----------------------------------------------------------------------|:------------------------------------|
| [**SetQOSApplicationID**](itqosapplicationid-setqosapplicationid.md) | Imposta l'identificatore QOS.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

