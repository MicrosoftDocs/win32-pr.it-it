---
description: La funzionalità dell'interfaccia ITConnection è illustrata di seguito.
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: Interfaccia ITConnection (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a64758f6a5cf7bcd9106504412f4cf7f39e6fb7ca0b76e35b38e19dc3f815ccf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140344"
---
# <a name="itconnection-interface"></a>Interfaccia ITConnection

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

**L'interfaccia ITConnection** offre le funzionalità seguenti:

-   Fornisce l'accesso alle informazioni relative all'indirizzo e alla durata (TTL) per la sessione.
-   Fornisce l'accesso alle informazioni sulla larghezza di banda.
-   Consente la manipolazione della chiave di crittografia.

**L'interfaccia ITConnection** viene creata chiamando **QueryInterface** [**in ITConferenceBlob.**](itconferenceblob.md)

## <a name="members"></a>Membri

**L'interfaccia ITConnection** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITConnection** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITConnection** include questi metodi.



| Metodo                                                               | Descrizione                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ AddressType**](itconnection-get-addresstype.md)             | Ottiene il tipo di indirizzo.<br/>                                                                                                              |
| [**get \_ bandwidth**](itconnection-get-bandwidth.md)                 | Ottiene il valore della larghezza di banda.<br/>                                                                                                               |
| [**get \_ BandwidthModifier**](itconnection-get-bandwidthmodifier.md) | Ottiene il modificatore della larghezza di banda.<br/>                                                                                                        |
| [**get \_ NetworkType**](itconnection-get-networktype.md)             | Ottiene il tipo di rete.<br/>                                                                                                              |
| [**get \_ NumAddresses**](itconnection-get-numaddresses.md)           | Ottiene il numero di indirizzi da utilizzare per la sessione.<br/>                                                                            |
| [**get \_ StartAddress**](itconnection-get-startaddress.md)           | Ottiene il primo indirizzo da utilizzare per la sessione.<br/>                                                                                  |
| [**get \_ Ttl**](itconnection-get-ttl.md)                             | Ottiene [*l'ambito*](t-tapgloss.md) TTL (Time To Live) per le trasmissioni sugli indirizzi.<br/> |
| [**GetEncryptionKey**](itconnection-getencryptionkey.md)            | Ottiene la chiave di crittografia.<br/>                                                                                                            |
| [**put \_ AddressType**](itconnection-put-addresstype.md)             | Imposta il tipo di indirizzo.<br/>                                                                                                              |
| [**put \_ NetworkType**](itconnection-put-networktype.md)             | Imposta il tipo di rete.<br/>                                                                                                              |
| [**SetAddressInfo**](itconnection-setaddressinfo.md)                | Imposta le informazioni sull'indirizzo.<br/>                                                                                                           |
| [**SetBandwidthInfo**](itconnection-setbandwidthinfo.md)            | Imposta il valore della larghezza di banda.<br/>                                                                                                           |
| [**SetEncryptionKey**](itconnection-setencryptionkey.md)            | Imposta la chiave di crittografia necessaria per decrittografare la sessione o un'indicazione di un meccanismo per ottenere una chiave utilizzabile con mezzi esterni.<br/>     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

