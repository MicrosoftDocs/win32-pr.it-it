---
description: L'interfaccia IDelaydC fornisce i metodi usati per connettersi alla rete, acquisire il traffico di rete a un file di acquisizione, recuperare statistiche e disconnettersi dalla rete.
ms.assetid: ab275653-2377-4af6-a810-48515962c88c
title: Interfaccia IDelaydC (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1b6b965990435dd7b9a1758cc9bf8ac8001c747ae800225a90123da862032ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890561"
---
# <a name="idelaydc-interface"></a>Interfaccia IDelaydC

**L'interfaccia IDelaydC** fornisce i metodi usati per connettersi alla rete, acquisire il traffico di rete a un file di acquisizione, recuperare statistiche e disconnettersi dalla rete.

Questa interfaccia acquisisce i frame dal flusso di dati di rete e quindi copia i frame in un file di acquisizione. Questa interfaccia viene usata dalle applicazioni Network Monitor e NPP. Per ricevere i dati di rete, la scheda di interfaccia di rete di destinazione deve supportare la modalità promiscua.

## <a name="members"></a>Membri

**L'interfaccia IDelaydC** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IDelaydC** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IDelaydC** include questi metodi.



| Metodo                                                                  | Descrizione                                                                                                                                             |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurare**](idelaydc-configure.md)                                 | Invia le informazioni di configurazione usate per un'acquisizione.<br/>                                                                                        |
| [**Connettere**](idelaydc-connect.md)                                     | Connette il server dei criteri di rete alla rete.<br/>                                                                                                             |
| [**Disconnetti**](idelaydc-disconnect.md)                               | Disconnette NPP dalla rete.<br/>                                                                                                        |
| [**GetControlState**](idelaydc-getcontrolstate.md)                     | Recupera lo stato [*dell'acquisizione*](c.md), che indica se l'acquisizione è in esecuzione o sospesa.<br/>                      |
| [**GetConversationStatistics**](idelaydc-getconversationstatistics.md) | Recupera le [*informazioni sulla*](s.md) sessione e [*sulla stazione*](s.md) per l'acquisizione corrente.<br/> |
| [**GetTotalStatistics**](idelaydc-gettotalstatistics.md)               | Estrae tempo, buffer, driver e altre statistiche di rete dall'acquisizione attualmente in esecuzione.<br/>                                              |
| [**Sospendi**](idelaydc-pause.md)                                         | Arresta temporaneamente l'acquisizione corrente.<br/>                                                                                                       |
| [**QueryStations**](idelaydc-querystations.md)                         | Recupera un elenco di tutti i computer che usano Network Monitor per acquisire dati in una subnet.<br/>                                                      |
| [**QueryStatus**](idelaydc-querystatus.md)                             | Recupera lo stato di NPP.<br/>                                                                                                             |
| [**Riprendi**](idelaydc-resume.md)                                       | Riprende un'acquisizione sospesa.<br/>                                                                                                                    |
| [**Avvio**](idelaydc-start.md)                                         | Avvia un'acquisizione e crea il [*file di acquisizione*](c.md).<br/>                                                           |
| [**Fermare**](idelaydc-stop.md)                                           | Arresta l'acquisizione corrente e chiude il [*file di acquisizione*](c.md).<br/>                                                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

