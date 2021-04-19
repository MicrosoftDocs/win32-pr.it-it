---
description: L'interfaccia IStats fornisce i metodi usati per connettere un NPP alla rete, acquisire il traffico di rete, recuperare le statistiche e disconnettere l'oggetto NPP dalla rete. Questa interfaccia genera statistiche senza frame.
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: Interfaccia IStats (Netmon. h)
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
ms.openlocfilehash: b64816589e3d4d0a2e3ace7be5c895e3d2cf22f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308167"
---
# <a name="istats-interface"></a>Interfaccia IStats

L'interfaccia **IStats** fornisce i metodi usati per connettere un NPP alla rete, acquisire il traffico di rete, recuperare le statistiche e disconnettere l'oggetto NPP dalla rete. Questa interfaccia genera statistiche senza frame.

## <a name="members"></a>Membri

L'interfaccia **IStats** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . Gli **Istat** hanno anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IStats** ha questi metodi.



| Metodo                                                                | Descrizione                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurare**](istats-configure.md)                                 | Configura il trigger, la corrispondenza dei criteri e le dimensioni del buffer del file di acquisizione.<br/>                                                                    |
| [**Connettersi**](istats-connect.md)                                     | Connette l'oggetto NPP alla rete.<br/>                                                                                                               |
| [**Disconnetti**](istats-disconnect.md)                               | Disconnette l'oggetto NPP dalla rete.<br/>                                                                                                          |
| [**GetControlState**](istats-getcontrolstate.md)                     | Recupera lo stato dell' [*acquisizione*](c.md), che indica se l'acquisizione viene eseguita o sospesa.<br/>                        |
| [**GetConversationStatistics**](istats-getconversationstatistics.md) | Recupera le informazioni sulla [*sessione*](s.md) e sulla [*stazione*](s.md) relative all'acquisizione corrente.<br/> |
| [**GetTotalStatistics**](istats-gettotalstatistics.md)               | Estrae tempo, buffer, driver e altre statistiche di rete dall'acquisizione attualmente in esecuzione.<br/>                                                |
| [**Sospendere**](istats-pause.md)                                         | Interrompe temporaneamente l'acquisizione corrente.<br/>                                                                                                         |
| [**QueryStations**](istats-querystations.md)                         | Recupera un elenco di tutti i computer che utilizzano Network Monitor per acquisire i dati in una subnet.<br/>                                                  |
| [**QueryStatus**](istats-querystatus.md)                             | Recupera lo stato dell'oggetto NPP.<br/>                                                                                                               |
| [**Riprendi**](istats-resume.md)                                       | Riavvia un'acquisizione sospesa.<br/>                                                                                                                     |
| [**Avvio**](istats-start.md)                                         | Avvia l'acquisizione.<br/>                                                                                                                            |
| [**Interrompere**](istats-stop.md)                                           | Arresta l'acquisizione corrente.<br/>                                                                                                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

