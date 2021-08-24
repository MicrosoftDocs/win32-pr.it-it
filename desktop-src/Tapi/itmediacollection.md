---
description: L'interfaccia ITMediaCollection consente di accedere al set di informazioni multimediali nella descrizione di una conferenza SDP (RFC 2327).
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: Interfaccia ITMediaCollection (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2425ae89f376d5cb2d7cc23e70abd33f87750d3d1b5343a17c8ecb05d7de760d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034611"
---
# <a name="itmediacollection-interface"></a>Interfaccia ITMediaCollection

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

**L'interfaccia ITMediaCollection** consente di accedere al set di informazioni multimediali nella descrizione di una conferenza SDP (RFC 2327). Ogni descrizione dei supporti nel SDP è descritta da [**un'interfaccia ITMedia.**](itmedia.md) **ITMediaCollection consente** la manipolazione del set di **informazioni ITMedia** per SDP, tra cui:

-   Consente l'accesso ai supporti in base all'indice.
-   Consente la creazione e l'eliminazione di supporti.

Il [**metodo ITSdp::get \_ MediaCollection**](itsdp-get-mediacollection.md) crea **l'interfaccia ITMediaCollection.**

## <a name="members"></a>Membri

**L'interfaccia ITMediaCollection** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITMediaCollection** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITMediaCollection** include questi metodi.



| Metodo                                                            | Descrizione                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**Creare**](itmediacollection-create.md)                        | Crea un nuovo supporto con proprietà predefinite e lo restituisce.<br/> |
| [**Elimina**](itmediacollection-delete.md)                        | Elimina i supporti corrispondenti all'indice specificato.<br/>     |
| [**get \_ \_ NewEnum**](itmediacollection-get--newenum.md)          | Restituisce un enumeratore per la raccolta.<br/>                   |
| [**get \_ Count**](itmediacollection-get-count.md)                 | Ottiene il numero di supporti nella sessione.<br/>                    |
| [**get \_ EnumerationIf**](itmediacollection-get-enumerationif.md) | Ottiene il puntatore all'interfaccia di enumerazione.<br/>                      |
| [**get \_ Item**](itmediacollection-get-item.md)                   | Restituisce i supporti corrispondenti all'indice specificato.<br/>     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

