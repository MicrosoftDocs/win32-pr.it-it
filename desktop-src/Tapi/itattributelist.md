---
description: L'interfaccia ITAttributeList fornisce metodi per ottenere e impostare attributi non interpretati.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: Interfaccia ITAttributeList (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a8dd0ac143791a09eedbd3fe575dcecb894a1fb6dbb218c8ecfdcadf60ebd60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762427"
---
# <a name="itattributelist-interface"></a>Interfaccia ITAttributeList

\[I controlli e le interfacce di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

**L'interfaccia ITAttributeList** fornisce metodi per ottenere e impostare attributi non interpretati. Per quanto riguarda la posizione delle stringhe di attributo in un pacchetto SDP (Session Descriptor Protocol, vedere RFC 2327), i metodi presuppongono che tutte le stringhe di attributo esistano subito prima che gli attributi multimediali siano specificati e dopo tutti gli attributi comuni. **L'interfaccia ITAttributeList** viene creata chiamando **QueryInterface** in [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).

## <a name="members"></a>Membri

**L'interfaccia ITAttributeList** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITAttributeList** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITAttributeList** include questi metodi.



| Metodo                                                          | Descrizione                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [**Aggiungere**](itattributelist-add.md)                              | Aggiunge l'attributo in corrispondenza dell'indice specificato.<br/>   |
| [**Elimina**](itattributelist-delete.md)                        | Elimina l'attributo in corrispondenza dell'indice specificato<br/> |
| [**get \_ AttributeList**](itattributelist-get-attributelist.md) | Ottiene l'elenco di attributi.<br/>                 |
| [**get \_ count**](itattributelist-get-count.md)                 | Ottiene il numero di attributi.<br/>               |
| [**get \_ Item**](itattributelist-get-item.md)                   | Ottiene l'attributo specificato dall'indice.<br/>   |
| [**put \_ AttributeList**](itattributelist-put-attributelist.md) | Imposta l'elenco di attributi.<br/>                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

