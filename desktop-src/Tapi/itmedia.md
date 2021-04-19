---
description: L'interfaccia ITMedia è una rappresentazione di supporti in un protocollo SDP (Session Descriptor Protocol), vedere RFC 2327.
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: Interfaccia ITMedia (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd00d7eab685fe99b089556bcdb0ed2bf6329df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329447"
---
# <a name="itmedia-interface"></a>Interfaccia ITMedia

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'interfaccia **ITmedia** è una rappresentazione di supporti in un protocollo SDP (Session Descriptor Protocol), vedere RFC 2327. Questa interfaccia Esporta i metodi per ottenere e impostare le proprietà dei supporti di base, ad esempio Type. I metodi [**ITMediaCollection:: Get \_ Item**](itmediacollection-get-item.md) e [**ITMediaCollection:: create**](itmediacollection-create.md) creano l'interfaccia **ITmedia** .

## <a name="members"></a>Membri

L'interfaccia **ITmedia** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITmedia** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ITmedia** dispone di questi metodi.



| Metodo                                                          | Descrizione                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**ottenere \_ codiciformato**](itmedia-get-formatcodes.md)             | Ottiene l'elenco dei codici di formato del payload multimediale.<br/>                                          |
| [**ottenere \_ MEDIANAME**](itmedia-get-medianame.md)                 | Ottiene il nome del supporto.<br/>                                                                  |
| [**ottenere \_ MediaTitle**](itmedia-get-mediatitle.md)               | Ottiene il titolo del supporto.<br/>                                                                 |
| [**ottenere \_ NumPorts**](itmedia-get-numports.md)                   | Ottiene il numero di porte necessarie per la sessione.<br/>                                      |
| [**ottenere \_ presenta**](itmedia-get-startport.md)                 | Ottiene il valore della porta a 16 bit per la prima porta.<br/>                                        |
| [**ottenere \_ TransportProtocol**](itmedia-get-transportprotocol.md) | Ottiene il protocollo di trasporto.<br/>                                                          |
| [**Inserisci \_ codiciformato**](itmedia-put-formatcodes.md)             | Imposta l'elenco dei codici di formato del payload multimediale.<br/>                                          |
| [**Inserisci \_ MEDIANAME**](itmedia-put-medianame.md)                 | Imposta il nome del supporto.<br/>                                                                  |
| [**Inserisci \_ MediaTitle**](itmedia-put-mediatitle.md)               | Imposta il titolo del supporto.<br/>                                                                 |
| [**Inserisci \_ TransportProtocol**](itmedia-put-transportprotocol.md) | Imposta il protocollo di trasporto.<br/>                                                          |
| [**SetPortInfo**](itmedia-setportinfo.md)                      | Imposta il valore della porta a 16 bit per la prima porta e il numero di porte necessarie per la sessione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Libreria<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> <dt>

[**ITSDP**](itsdp.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

