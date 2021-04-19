---
description: La funzionalità dell'interfaccia ITConnection è illustrata di seguito.
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: Interfaccia ITConnection (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00da80631c0ef4e8186aa36425f18e4d2a62bfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333143"
---
# <a name="itconnection-interface"></a>Interfaccia ITConnection

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITConnection** fornisce le funzionalità seguenti:

-   Consente di accedere alle informazioni relative all'indirizzo e alla durata (TTL) per la sessione.
-   Consente di accedere alle informazioni sulla larghezza di banda.
-   Abilita la manipolazione della chiave di crittografia.

L'interfaccia **ITConnection** viene creata chiamando **QueryInterface** in [**ITConferenceBlob**](itconferenceblob.md).

## <a name="members"></a>Membri

L'interfaccia **ITConnection** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITConnection** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITConnection** dispone di questi metodi.



| Metodo                                                               | Descrizione                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**ottenere \_ AddressType**](itconnection-get-addresstype.md)             | Ottiene il tipo di indirizzo.<br/>                                                                                                              |
| [**ottenere la \_ larghezza di banda**](itconnection-get-bandwidth.md)                 | Ottiene il valore della larghezza di banda.<br/>                                                                                                               |
| [**ottenere \_ BandwidthModifier**](itconnection-get-bandwidthmodifier.md) | Ottiene il modificatore della larghezza di banda.<br/>                                                                                                        |
| [**ottenere \_ NetworkType**](itconnection-get-networktype.md)             | Ottiene il tipo di rete.<br/>                                                                                                              |
| [**ottenere \_ NumAddresses**](itconnection-get-numaddresses.md)           | Ottiene il numero di indirizzi da utilizzare per la sessione.<br/>                                                                            |
| [**ottenere \_ STARTADDRESS**](itconnection-get-startaddress.md)           | Ottiene il primo indirizzo da utilizzare per la sessione.<br/>                                                                                  |
| [**ottenere la durata ( \_ TTL)**](itconnection-get-ttl.md)                             | Ottiene l'ambito TTL ( [*time to Live*](t-tapgloss.md) ) per le trasmissioni sugli indirizzi.<br/> |
| [**GetEncryptionKey**](itconnection-getencryptionkey.md)            | Ottiene la chiave di crittografia.<br/>                                                                                                            |
| [**Inserisci \_ AddressType**](itconnection-put-addresstype.md)             | Imposta il tipo di indirizzo.<br/>                                                                                                              |
| [**Inserisci \_ NetworkType**](itconnection-put-networktype.md)             | Imposta il tipo di rete.<br/>                                                                                                              |
| [**SetAddressInfo**](itconnection-setaddressinfo.md)                | Imposta le informazioni sull'indirizzo.<br/>                                                                                                           |
| [**SetBandwidthInfo**](itconnection-setbandwidthinfo.md)            | Imposta il valore della larghezza di banda.<br/>                                                                                                           |
| [**SetEncryptionKey**](itconnection-setencryptionkey.md)            | Imposta la chiave di crittografia necessaria per decrittografare la sessione o un'indicazione in un meccanismo per ottenere una chiave utilizzabile per mezzo esterno.<br/>     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

