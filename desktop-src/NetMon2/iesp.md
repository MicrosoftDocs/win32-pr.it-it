---
description: L'interfaccia IESP fornisce i metodi che connettono NPP alla rete, acquisiscono il traffico di rete a un file di acquisizione, recuperano le statistiche e disconnettono NPP dalla rete.
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: Interfaccia IESP (Netmon.h)
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
ms.openlocfilehash: e7420e21a9f2c6ac92712326fa4a51159c6303d3972756e7a47c0797f22a1d83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037431"
---
# <a name="iesp-interface"></a>Interfaccia IESP

**L'interfaccia IESP** fornisce i metodi che connettono NPP alla rete, acquisiscono il traffico di rete a un file di acquisizione, recuperano le statistiche e disconnettono il NPP dalla rete. Questa interfaccia viene usata principalmente quando è necessario raccogliere statistiche di [*conversazione di rete*](c.md) in un formato di file ESP proprietario.

## <a name="members"></a>Membri

**L'interfaccia IESP** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IESP** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IESP.**



| Metodo                                          | Descrizione                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Configurare**](iesp-configure.md)             | Invia informazioni di configurazione per un'acquisizione<br/>                                                                         |
| [**Connettere**](iesp-connect.md)                 | Connette il server dei criteri di rete alla rete.<br/>                                                                                        |
| [**Disconnetti**](iesp-disconnect.md)           | Disconnette NPP dalla rete.<br/>                                                                                   |
| [**GetControlState**](iesp-getcontrolstate.md) | Recupera lo stato [*dell'acquisizione*](c.md), che indica se l'acquisizione è in esecuzione o sospesa.<br/> |
| [**Sospendi**](iesp-pause.md)                     | Arresta temporaneamente l'acquisizione corrente.<br/>                                                                                  |
| [**QueryStations**](iesp-querystations.md)     | Recupera un elenco di tutti i computer che usano Network Monitor per acquisire dati in una subnet.<br/>                           |
| [**QueryStatus**](iesp-querystatus.md)         | Recupera lo stato di NPP.<br/>                                                                                        |
| [**Riprendi**](iesp-resume.md)                   | Riprende un'acquisizione sospesa.<br/>                                                                                               |
| [**Avvio**](iesp-start.md)                     | Avvia l'acquisizione e crea il file di acquisizione.<br/>                                                                        |
| [**Fermare**](iesp-stop.md)                       | Arresta l'acquisizione corrente.<br/>                                                                                              |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

