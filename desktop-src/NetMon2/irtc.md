---
description: L'interfaccia IRTC fornisce i metodi usati per connettere l'oggetto NPP alla rete, acquisire il traffico di rete, recuperare le statistiche e disconnettere l'oggetto NPP dalla rete.
ms.assetid: 9252a9ba-2c3e-40b9-b8de-84ef5d4831a7
title: Interfaccia IRTC (Netmon. h)
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
ms.openlocfilehash: c937d7d9233b1df063a7cf4a12e57e909145b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967136"
---
# <a name="irtc-interface"></a>Interfaccia IRTC

L'interfaccia **IRTC** fornisce i metodi usati per connettere l'oggetto NPP alla rete, acquisire il traffico di rete, recuperare le statistiche e disconnettere l'oggetto NPP dalla rete. **IRTC** ottiene un'interfaccia per i punti di ingresso solo locali, necessari per attivare l'acquisizione in tempo reale. Questa interfaccia include un metodo che invia un callback a NPP.

## <a name="members"></a>Membri

L'interfaccia **IRTC** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IRTC** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IRTC** dispone di questi metodi.



| Metodo                                                              | Descrizione                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurare**](irtc-configure.md)                                 | Imposta il trigger, la corrispondenza dei criteri e le dimensioni del buffer dell'acquisizione.<br/>                                                                             |
| [**Connettersi**](irtc-connect.md)                                     | Connette l'oggetto NPP alla rete.<br/>                                                                                                             |
| [**Disconnetti**](irtc-disconnect.md)                               | Disconnette l'oggetto NPP dalla rete.<br/>                                                                                                        |
| [**GetControlState**](irtc-getcontrolstate.md)                     | Recupera lo stato dell' [*acquisizione*](c.md), che indica se l'acquisizione viene eseguita o sospesa.<br/>                      |
| [**GetConversationStatistics**](irtc-getconversationstatistics.md) | Recupera le informazioni sulla [*sessione*](s.md) e [*sulla stazione*](s.md) per l'acquisizione corrente.<br/> |
| [**GetTotalStatistics**](irtc-gettotalstatistics.md)               | Estrae tempo, buffer, driver e altre statistiche di rete dall'acquisizione attualmente in esecuzione.<br/>                                              |
| [**Sospendere**](irtc-pause.md)                                         | Interrompe temporaneamente l'acquisizione corrente.<br/>                                                                                                       |
| [**QueryStations**](irtc-querystations.md)                         | Recupera un elenco di tutti i computer in una subnet che utilizzano Network Monitor per acquisire i dati di rete.<br/>                                        |
| [**QueryStatus**](irtc-querystatus.md)                             | Recupera lo stato dell'oggetto NPP.<br/>                                                                                                             |
| [**Riprendi**](irtc-resume.md)                                       | Riavvia un'acquisizione sospesa.<br/>                                                                                                                   |
| [**Avvio**](irtc-start.md)                                         | Avvia un'acquisizione.<br/>                                                                                                                            |
| [**Interrompere**](irtc-stop.md)                                           | Arresta l'acquisizione corrente.<br/>                                                                                                                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

