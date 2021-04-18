---
description: L'interfaccia ITQOSApplicationID espone un metodo che consente a un'applicazione di ottenere l'identificatore QOS per la chiamata corrente.
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: Interfaccia ITQOSApplicationID (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23df8da80798cc52ecd73b4f29288812f3774d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333658"
---
# <a name="itqosapplicationid-interface"></a>Interfaccia ITQOSApplicationID

\[ Questa interfaccia non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITQOSApplicationID** espone un metodo che consente a un'applicazione di ottenere l'identificatore QoS per la chiamata corrente.

Questa interfaccia viene implementata da [IPConf msp](ipconf-msp.md) ed è esposta solo quando una chiamata utilizza la conferenza IP.

## <a name="members"></a>Membri

L'interfaccia **ITQOSApplicationID** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITQOSApplicationID** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITQOSApplicationID** dispone di questi metodi.



| Metodo                                                                | Descrizione                         |
|:----------------------------------------------------------------------|:------------------------------------|
| [**SetQOSApplicationID**](itqosapplicationid-setqosapplicationid.md) | Imposta l'identificatore QOS.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|--------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                         |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

