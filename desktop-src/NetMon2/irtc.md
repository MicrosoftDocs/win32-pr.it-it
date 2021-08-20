---
description: L'interfaccia IRTC fornisce i metodi usati per connettere il NPP alla rete, acquisire il traffico di rete, recuperare statistiche e disconnettere il NPP dalla rete.
ms.assetid: 9252a9ba-2c3e-40b9-b8de-84ef5d4831a7
title: Interfaccia IRTC (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: f330892da5844305d4d1f3ffa3aee0bf6e9ef50fb2a1cd951c332e2b17eb3b12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132930"
---
# <a name="irtc-interface"></a>Interfaccia IRTC

**L'interfaccia IRTC** fornisce i metodi usati per connettere il NPP alla rete, acquisire il traffico di rete, recuperare le statistiche e disconnettere il NPP dalla rete. **IRTC** ottiene un'interfaccia per i punti di ingresso solo locali, necessari per eseguire l'acquisizione in tempo reale. Questa interfaccia include un metodo che esegue un callback al NPP.

## <a name="members"></a>Membri

**L'interfaccia IRTC** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IRTC** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IRTC** include questi metodi.



| Metodo                                                              | Descrizione                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurare**](irtc-configure.md)                                 | Imposta il trigger, la corrispondenza dei criteri e le dimensioni del buffer dell'acquisizione.<br/>                                                                             |
| [**Connettere**](irtc-connect.md)                                     | Connette il NPP alla rete.<br/>                                                                                                             |
| [**Disconnetti**](irtc-disconnect.md)                               | Disconnette il NPP dalla rete.<br/>                                                                                                        |
| [**GetControlState**](irtc-getcontrolstate.md)                     | Recupera lo stato [*dell'acquisizione*](c.md), che indica se l'acquisizione è in esecuzione o sospesa.<br/>                      |
| [**GetConversationStatistics**](irtc-getconversationstatistics.md) | Recupera le [*informazioni sulla*](s.md) sessione e [*sulla stazione*](s.md) per l'acquisizione corrente.<br/> |
| [**GetTotalStatistics**](irtc-gettotalstatistics.md)               | Estrae tempo, buffer, driver e altre statistiche di rete dall'acquisizione attualmente in esecuzione.<br/>                                              |
| [**Sospendi**](irtc-pause.md)                                         | Arresta temporaneamente l'acquisizione corrente.<br/>                                                                                                       |
| [**QueryStations**](irtc-querystations.md)                         | Recupera un elenco di tutti i computer in una subnet che usano Network Monitor per acquisire i dati di rete.<br/>                                        |
| [**QueryStatus**](irtc-querystatus.md)                             | Recupera lo stato del NPP.<br/>                                                                                                             |
| [**Riprendi**](irtc-resume.md)                                       | Riavvia un'acquisizione sospesa.<br/>                                                                                                                   |
| [**Avvio**](irtc-start.md)                                         | Avvia un'acquisizione.<br/>                                                                                                                            |
| [**Fermare**](irtc-stop.md)                                           | Arresta l'acquisizione corrente.<br/>                                                                                                                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

