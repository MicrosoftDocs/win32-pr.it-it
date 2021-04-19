---
description: L'interfaccia ITMediaCollection consente di accedere al set di informazioni sui supporti in una descrizione della conferenza SDP (RFC 2327).
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: Interfaccia ITMediaCollection (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21305e1d1729437b53c380b7712feee3827b3ba8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324238"
---
# <a name="itmediacollection-interface"></a>Interfaccia ITMediaCollection

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITMediaCollection** consente di accedere al set di informazioni sui supporti in una descrizione della conferenza SDP (RFC 2327). Ogni descrizione del supporto in SDP è descritta da un'interfaccia [**ITmedia**](itmedia.md) . **ITMediaCollection** consente la manipolazione del set di informazioni **ITMEDIA** per il SDP, tra cui:

-   Consente l'accesso ai file multimediali in base all'indice.
-   Consente la creazione e l'eliminazione di supporti.

Il metodo [**ITSdp:: Get \_ mediacollection**](itsdp-get-mediacollection.md) crea l'interfaccia **ITMediaCollection** .

## <a name="members"></a>Membri

L'interfaccia **ITMediaCollection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITMediaCollection** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITMediaCollection** dispone di questi metodi.



| Metodo                                                            | Descrizione                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**Creare**](itmediacollection-create.md)                        | Crea un nuovo supporto con le proprietà predefinite e lo restituisce.<br/> |
| [**Delete**](itmediacollection-delete.md)                        | Elimina i supporti corrispondenti all'indice specificato.<br/>     |
| [**ottenere \_ \_ NewEnum**](itmediacollection-get--newenum.md)          | Restituisce un enumeratore per la raccolta.<br/>                   |
| [**Ottieni \_ conteggio**](itmediacollection-get-count.md)                 | Ottiene il numero di supporti nella sessione.<br/>                    |
| [**ottenere \_ EnumerationIf**](itmediacollection-get-enumerationif.md) | Ottiene il puntatore all'interfaccia di enumerazione.<br/>                      |
| [**Ottieni \_ elemento**](itmediacollection-get-item.md)                   | Restituisce il supporto corrispondente all'indice specificato.<br/>     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

