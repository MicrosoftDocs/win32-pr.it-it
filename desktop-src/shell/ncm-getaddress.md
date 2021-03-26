---
description: Indica se un indirizzo di rete è conforme a un tipo e un formato specificati.
title: Messaggio NCM_GETADDRESS (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 733CD62D-614C-4ac2-986D-CCFCFF4B1B4D
api_name:
- NCM_GETADDRESS
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d5effa69a23a61a602efaf1172de09a09889e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977879"
---
# <a name="ncm_getaddress-message"></a>NCM \_ GETaddress-messaggio

Indica se un indirizzo di rete è conforme a un tipo e un formato specificati.


```C++
NCM_GETADDRESS

    wParam = (WPARAM) (PNC_ADDRESS) pv;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*PV* \[ in uscita\]
</dt> <dd>Puntatore a una struttura di <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> per ricevere le informazioni sugli indirizzi di rete in forma analizzata, se il formato dell'indirizzo e il tipo nel controllo specificato da *HWND* sono convalidati. L'applicazione chiamante è responsabile dell'allocazione della memoria per questa struttura.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti di tipo **HRESULT**.



| Codice restituito                                                                                                | Descrizione                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | L'applicazione chiamante non è riuscita ad allocare una struttura dell' [**\_ Indirizzo NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) .<br/> |
| <dl> <dt>**ERRORE \_ buffer insufficiente \_**</dt> </dl> | Il buffer di uscita è troppo piccolo per mantenere l'indirizzo di rete analizzato.<br/>                           |
| <dl> <dt>**ERRORE \_ parametro non valido \_**</dt> </dl>   | La stringa dell'indirizzo di rete non è di alcun tipo specificato.<br/>                                  |
| <dl> <dt>**ERRORE \_ riuscito**</dt> </dl>              | L'operazione è stata completata.<br/>                                                             |
| <dl> <dt>**S \_ false**</dt> </dl>                    | Nessun indirizzo nel controllo indirizzo di rete da convalidare.<br/>                           |



 

## <a name="remarks"></a>Commenti

Usare il messaggio **NCM \_ GetAddress** per convalidare un indirizzo di rete in un controllo degli indirizzi di rete rispetto a una maschera di tipo indirizzo di rete preimpostata. Per creare un'istanza di, usare la classe **msctls \_ Netaddress** definita in Shellapi. h. Chiamare [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) in fase di esecuzione prima di inviare questo messaggio. Viene inizializzata la libreria di controlli comuni che contiene il controllo degli indirizzi di rete.

Questo messaggio ottiene la stringa dell'indirizzo di rete da un controllo indirizzo di rete, analizza la stringa e controlla se la stringa corrisponde a una maschera di tipo indirizzo di rete. Se la stringa corrisponde alla maschera, il messaggio restituisce S \_ OK e restituisce la stringa in formato analizzato all'applicazione chiamante (inclusi il numero di porta, la lunghezza del prefisso e altre informazioni sull'indirizzo), usando la struttura dell' [**\_ Indirizzo NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) a cui punta *PV*. Questo messaggio restituisce E \_ INVALIDARG se l'applicazione chiamante non riesce ad allocare la struttura a cui punta *PV*.

Le rappresentazioni di indirizzi IP (Internet Protocol) versioni 4 e 6 (V4/V6) per servizi e reti, oltre ad indirizzi Internet e servizi denominati che usano il formato Domain Name System (DNS) vengono analizzate. Se la stringa dell'indirizzo di rete rappresenta un nome host (DNS) o un servizio denominato, il valore restituito nel membro **LunghezzaPrefisso** dell' [**\_ Indirizzo NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) è zero.

Impostare il tipo di indirizzo di rete mask usando il messaggio [**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md) prima di inviare la macro **NCM \_ GetAddress** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NCM \_ GETALLOWTYPE**](ncm-getallowtype.md)
</dt> <dt>

[**NetAddr \_ GetAddress**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 




