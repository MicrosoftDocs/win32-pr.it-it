---
description: L'interfaccia ITAttributeList fornisce i metodi per ottenere e impostare gli attributi non interpretati.
ms.assetid: 12806c2e-615c-4d78-a4bb-5cc35ea21175
title: Interfaccia ITAttributeList (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2afbc7ab447188943c0f02e6c5a664bbcc4c6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332729"
---
# <a name="itattributelist-interface"></a>Interfaccia ITAttributeList

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITAttributeList** fornisce i metodi per ottenere e impostare gli attributi non interpretati. Per quanto riguarda la posizione delle stringhe degli attributi in un pacchetto del protocollo di descrizione della sessione (SDP, see RFC 2327), i metodi presuppongono che tutte le stringhe di attributo esistano immediatamente prima che siano specificati gli attributi multimediali e dopo tutti gli attributi comuni. L'interfaccia **ITAttributeList** viene creata chiamando **QueryInterface** in [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).

## <a name="members"></a>Membri

L'interfaccia **ITAttributeList** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITAttributeList** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITAttributeList** dispone di questi metodi.



| Metodo                                                          | Descrizione                                             |
|:----------------------------------------------------------------|:--------------------------------------------------------|
| [**Aggiungere**](itattributelist-add.md)                              | Aggiunge l'attributo in corrispondenza dell'indice specificato.<br/>   |
| [**Delete**](itattributelist-delete.md)                        | Elimina l'attributo in corrispondenza dell'indice specificato.<br/> |
| [**Ottieni \_ attributo**](itattributelist-get-attributelist.md) | Ottiene l'elenco di attributi.<br/>                 |
| [**Ottieni \_ conteggio**](itattributelist-get-count.md)                 | Ottiene il numero di attributi.<br/>               |
| [**Ottieni \_ elemento**](itattributelist-get-item.md)                   | Ottiene l'attributo specificato dall'indice.<br/>   |
| [**Inserisci \_ attributo**](itattributelist-put-attributelist.md) | Imposta l'elenco di attributi.<br/>                 |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

