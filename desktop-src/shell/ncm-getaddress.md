---
description: Indica se un indirizzo di rete è conforme a un tipo e a un formato specificati.
title: NCM_GETADDRESS messaggio (Shellapi.h)
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
ms.openlocfilehash: 27f5beec56a0125d26cc359f40b5033eda1f035f2dec7666725264ec6fd59ba7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677969"
---
# <a name="ncm_getaddress-message"></a>Messaggio \_ GETADDRESS di NCM

Indica se un indirizzo di rete è conforme a un tipo e a un formato specificati.


```C++
NCM_GETADDRESS

    wParam = (WPARAM) (PNC_ADDRESS) pv;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*pv* \[ in, out\]
</dt> <dd>Puntatore a una <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">struttura NC_ADDRESS</a> per ricevere informazioni sull'indirizzo di rete in formato analizzato, se il formato dell'indirizzo e il tipo nel controllo specificato da *hwnd* vengono convalidati. L'applicazione chiamante è responsabile dell'allocazione della memoria per questa struttura.</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori seguenti di tipo **HRESULT**.



| Codice restituito                                                                                                | Descrizione                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | L'applicazione chiamante non è riuscita ad allocare [**una struttura NC \_ ADDRESS.**](/windows/win32/api/shellapi/ns-shellapi-nc_address)<br/> |
| <dl> <dt>**ERRORE \_ BUFFER \_ INSUFFICIENTE**</dt> </dl> | Il buffer out è troppo piccolo per contenere l'indirizzo di rete analizzato.<br/>                           |
| <dl> <dt>**ERRORE \_ PARAMETRO NON \_ VALIDO**</dt> </dl>   | La stringa dell'indirizzo di rete non è di alcun tipo specificato.<br/>                                  |
| <dl> <dt>**ERRORE \_ RIUSCITO**</dt> </dl>              | L'operazione è stata completata.<br/>                                                             |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | Non è presente alcun indirizzo nel controllo degli indirizzi di rete da convalidare.<br/>                           |



 

## <a name="remarks"></a>Commenti

Usare il **messaggio NCM \_ GETADDRESS** per convalidare un indirizzo di rete in un controllo degli indirizzi di rete rispetto a una maschera del tipo di indirizzo di rete preimpostato. Per creare un'istanza, usare la **classe msctls \_ netaddress** definita in Shellapi.h. Chiamare [**InitNetworkAddressControl in**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) fase di esecuzione prima di inviare questo messaggio. In questo modo viene inizializzata la libreria di controlli comuni che contiene il controllo degli indirizzi di rete.

Questo messaggio ottiene la stringa dell'indirizzo di rete da un controllo degli indirizzi di rete, analizza la stringa e verifica se la stringa corrisponde a una maschera del tipo di indirizzo di rete. Se la stringa corrisponde alla maschera, il messaggio restituisce S OK e restituisce la stringa in formato analizzato all'applicazione chiamante (inclusi il numero di porta, la lunghezza del prefisso e altre informazioni sull'indirizzo), usando la struttura NC ADDRESS a cui punta \_ *pv* [**\_**](/windows/win32/api/shellapi/ns-shellapi-nc_address) . Questo messaggio restituisce E INVALIDARG se l'applicazione chiamante non riesce ad \_ allocare la struttura a cui punta *pv*.

Vengono analizzate le rappresentazioni degli indirizzi IP (Internet Protocol) versioni 4 e 6 (v4/v6) per servizi e reti, nonché di indirizzi e servizi Internet denominati che usano il formato Domain Name System (DNS). Se la stringa dell'indirizzo di rete rappresenta un nome host denominato (DNS) o un servizio, il valore restituito nel membro **PrefixLength** di [**NC \_ ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) è zero.

Impostare la maschera del tipo di indirizzo di rete usando il [**messaggio \_ NCM SETALLOWTYPE**](ncm-setallowtype.md) prima di inviare la macro **NCM \_ GETADDRESS.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Shellapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NCM \_ GETALLOWTYPE**](ncm-getallowtype.md)
</dt> <dt>

[**NetAddr \_ GetAddress**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 




