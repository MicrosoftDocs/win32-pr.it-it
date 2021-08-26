---
description: L'interfaccia ITMedia è una rappresentazione dei supporti in un protocollo SDP (Session Descriptor Protocol, vedere RFC 2327).
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: Interfaccia ITMedia (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfd1cf7dcf8ef294481a4687dbac950f97b4adede6a6871222292127e6255057
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034641"
---
# <a name="itmedia-interface"></a>Interfaccia ITMedia

\[Le interfacce e i controlli di conferenza di telefonia IP rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

**L'interfaccia ITMedia** è una rappresentazione dei supporti in un protocollo SDP (Session Descriptor Protocol, vedere RFC 2327). Questa interfaccia esporta i metodi per ottenere e impostare le proprietà multimediali di base, ad esempio type. I [**metodi ITMediaCollection::get \_ Item**](itmediacollection-get-item.md) [**e ITMediaCollection::Create**](itmediacollection-create.md) creano **l'interfaccia ITMedia.**

## <a name="members"></a>Membri

**L'interfaccia ITMedia** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITMedia** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ITMedia** include questi metodi.



| Metodo                                                          | Descrizione                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**get \_ FormatCodes**](itmedia-get-formatcodes.md)             | Ottiene l'elenco dei codici di formato del payload multimediale.<br/>                                          |
| [**get \_ MediaName**](itmedia-get-medianame.md)                 | Ottiene il nome del supporto.<br/>                                                                  |
| [**get \_ MediaTitle**](itmedia-get-mediatitle.md)               | Ottiene il titolo dell'elemento multimediale.<br/>                                                                 |
| [**get \_ NumPorts**](itmedia-get-numports.md)                   | Ottiene il numero di porte necessarie per la sessione.<br/>                                      |
| [**get \_ StartPort**](itmedia-get-startport.md)                 | Ottiene il valore della porta a 16 bit per la prima porta.<br/>                                        |
| [**get \_ TransportProtocol**](itmedia-get-transportprotocol.md) | Ottiene il protocollo di trasporto.<br/>                                                          |
| [**put \_ FormatCodes**](itmedia-put-formatcodes.md)             | Imposta l'elenco di codici di formato del payload multimediale.<br/>                                          |
| [**put \_ MediaName**](itmedia-put-medianame.md)                 | Imposta il nome del supporto.<br/>                                                                  |
| [**put \_ MediaTitle**](itmedia-put-mediatitle.md)               | Imposta il titolo del contenuto multimediale.<br/>                                                                 |
| [**put \_ TransportProtocol**](itmedia-put-transportprotocol.md) | Imposta il protocollo di trasporto.<br/>                                                          |
| [**SetPortInfo**](itmedia-setportinfo.md)                      | Imposta il valore della porta a 16 bit per la prima porta e il numero di porte necessarie per la sessione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Idispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> <dt>

[**ITSDP**](itsdp.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

