---
description: L'interfaccia IStats fornisce i metodi che consentono di connettere un NPP alla rete, acquisire il traffico di rete, recuperare statistiche e disconnettere il NPP dalla rete. Questa interfaccia genera statistiche senza frame.
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: Interfaccia IStats (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 27a43f8ea2902af7e2847e032da18543ffdbb228c2aa3e49fde63ce7cd727512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119495011"
---
# <a name="istats-interface"></a>Interfaccia IStats

**L'interfaccia IStats** fornisce i metodi che consentono di connettere un NPP alla rete, acquisire il traffico di rete, recuperare statistiche e disconnettere il NPP dalla rete. Questa interfaccia genera statistiche senza frame.

## <a name="members"></a>Membri

**L'interfaccia IStats** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IStats** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IStats** include questi metodi.



| Metodo                                                                | Descrizione                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurare**](istats-configure.md)                                 | Configura il trigger, la corrispondenza dei criteri e le dimensioni del buffer del file di acquisizione.<br/>                                                                    |
| [**Connettere**](istats-connect.md)                                     | Connette il server dei criteri di rete alla rete.<br/>                                                                                                               |
| [**Disconnetti**](istats-disconnect.md)                               | Disconnette NPP dalla rete.<br/>                                                                                                          |
| [**GetControlState**](istats-getcontrolstate.md)                     | Recupera lo stato [*dell'acquisizione*](c.md), che indica se l'acquisizione è in esecuzione o sospesa.<br/>                        |
| [**GetConversationStatistics**](istats-getconversationstatistics.md) | Recupera le [*informazioni di*](s.md) sessione [*e stazione*](s.md) sull'acquisizione corrente.<br/> |
| [**GetTotalStatistics**](istats-gettotalstatistics.md)               | Estrae tempo, buffer, driver e altre statistiche di rete dall'acquisizione attualmente in esecuzione.<br/>                                                |
| [**Sospendi**](istats-pause.md)                                         | Arresta temporaneamente l'acquisizione corrente.<br/>                                                                                                         |
| [**QueryStations**](istats-querystations.md)                         | Recupera un elenco di tutti i computer che usano Network Monitor per acquisire dati in una subnet.<br/>                                                  |
| [**QueryStatus**](istats-querystatus.md)                             | Recupera lo stato di NPP.<br/>                                                                                                               |
| [**Riprendi**](istats-resume.md)                                       | Riavvia un'acquisizione sospesa.<br/>                                                                                                                     |
| [**Avvio**](istats-start.md)                                         | Avvia l'acquisizione.<br/>                                                                                                                            |
| [**Fermare**](istats-stop.md)                                           | Arresta l'acquisizione corrente.<br/>                                                                                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

