---
description: L'interfaccia IESP fornisce i metodi che connettono l'oggetto NPP alla rete, acquisisce il traffico di rete in un file di acquisizione, recupera le statistiche e disconnette l'oggetto NPP dalla rete.
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: Interfaccia IESP (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a7400bb9a16e6ece5f5f26fe95a0398a7d45e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128918"
---
# <a name="iesp-interface"></a>Interfaccia IESP

L'interfaccia **IESP** fornisce i metodi che connettono l'oggetto NPP alla rete, acquisisce il traffico di rete in un file di acquisizione, recupera le statistiche e disconnette l'oggetto NPP dalla rete. Questa interfaccia viene utilizzata principalmente quando è necessario raccogliere le [*statistiche delle conversazioni*](c.md) di rete in un formato di file ESP proprietario.

## <a name="members"></a>Membri

L'interfaccia **IESP** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IESP** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IESP** dispone di questi metodi.



| Metodo                                          | Descrizione                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Configurare**](iesp-configure.md)             | Invia le informazioni di configurazione per un'acquisizione<br/>                                                                         |
| [**Connettersi**](iesp-connect.md)                 | Connette l'oggetto NPP alla rete.<br/>                                                                                        |
| [**Disconnetti**](iesp-disconnect.md)           | Disconnette l'oggetto NPP dalla rete.<br/>                                                                                   |
| [**GetControlState**](iesp-getcontrolstate.md) | Recupera lo stato dell' [*acquisizione*](c.md), che indica se l'acquisizione viene eseguita o sospesa.<br/> |
| [**Sospendere**](iesp-pause.md)                     | Interrompe temporaneamente l'acquisizione corrente.<br/>                                                                                  |
| [**QueryStations**](iesp-querystations.md)     | Recupera un elenco di tutti i computer che utilizzano Network Monitor per acquisire i dati in una subnet.<br/>                           |
| [**QueryStatus**](iesp-querystatus.md)         | Recupera lo stato dell'oggetto NPP.<br/>                                                                                        |
| [**Riprendi**](iesp-resume.md)                   | Riprende un'acquisizione sospesa.<br/>                                                                                               |
| [**Avvio**](iesp-start.md)                     | Avvia l'acquisizione e crea il file di acquisizione.<br/>                                                                        |
| [**Interrompere**](iesp-stop.md)                       | Arresta l'acquisizione corrente.<br/>                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

