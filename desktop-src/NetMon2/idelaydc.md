---
description: L'interfaccia IDelaydC fornisce i metodi usati per connettersi alla rete, acquisire il traffico di rete in un file di acquisizione, recuperare le statistiche e disconnettersi dalla rete.
ms.assetid: ab275653-2377-4af6-a810-48515962c88c
title: Interfaccia IDelaydC (Netmon. h)
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
ms.openlocfilehash: cb87bc9f821e758b83a1bc3dee5d81a4b1b771d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308660"
---
# <a name="idelaydc-interface"></a>Interfaccia IDelaydC

L'interfaccia **IDelaydC** fornisce i metodi usati per connettersi alla rete, acquisire il traffico di rete in un file di acquisizione, recuperare le statistiche e disconnettersi dalla rete.

Questa interfaccia acquisisce i frame dal flusso di dati di rete e quindi copia i frame in un file di acquisizione. Questa interfaccia viene utilizzata dalle applicazioni Network Monitor e NPP. Per ricevere i dati di rete, la scheda di interfaccia di rete di destinazione deve supportare la modalità promiscua.

## <a name="members"></a>Membri

L'interfaccia **IDelaydC** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDelaydC** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDelaydC** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                                                                                                             |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurare**](idelaydc-configure.md)                                 | Invia le informazioni di configurazione usate per un'acquisizione.<br/>                                                                                        |
| [**Connettersi**](idelaydc-connect.md)                                     | Connette l'oggetto NPP alla rete.<br/>                                                                                                             |
| [**Disconnetti**](idelaydc-disconnect.md)                               | Disconnette l'oggetto NPP dalla rete.<br/>                                                                                                        |
| [**GetControlState**](idelaydc-getcontrolstate.md)                     | Recupera lo stato dell' [*acquisizione*](c.md), che indica se l'acquisizione viene eseguita o sospesa.<br/>                      |
| [**GetConversationStatistics**](idelaydc-getconversationstatistics.md) | Recupera le informazioni sulla [*sessione*](s.md) e [*sulla stazione*](s.md) per l'acquisizione corrente.<br/> |
| [**GetTotalStatistics**](idelaydc-gettotalstatistics.md)               | Estrae tempo, buffer, driver e altre statistiche di rete dall'acquisizione attualmente in esecuzione.<br/>                                              |
| [**Sospendere**](idelaydc-pause.md)                                         | Interrompe temporaneamente l'acquisizione corrente.<br/>                                                                                                       |
| [**QueryStations**](idelaydc-querystations.md)                         | Recupera un elenco di tutti i computer che utilizzano Network Monitor per acquisire i dati in una subnet.<br/>                                                      |
| [**QueryStatus**](idelaydc-querystatus.md)                             | Recupera lo stato dell'oggetto NPP.<br/>                                                                                                             |
| [**Riprendi**](idelaydc-resume.md)                                       | Riprende un'acquisizione sospesa.<br/>                                                                                                                    |
| [**Avvio**](idelaydc-start.md)                                         | Avvia un'acquisizione e crea il [*file di acquisizione*](c.md).<br/>                                                           |
| [**Interrompere**](idelaydc-stop.md)                                           | Arresta l'acquisizione corrente e chiude il [*file di acquisizione*](c.md).<br/>                                                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                                                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                                                                     |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

