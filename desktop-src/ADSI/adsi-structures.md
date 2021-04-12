---
title: Strutture ADSI
description: Le interfacce ADSI (Active Directory Service Interfaces) definiscono e utilizzano le strutture elencate nella tabella seguente.
ms.assetid: 3ee0e469-9932-4135-8798-27d318011786
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, riferimento, strutture
- strutture ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f35ba74f0334e8b66329d8f526266c315056af9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116693"
---
# <a name="adsi-structures"></a>Strutture ADSI

Le interfacce ADSI (Active Directory Service Interfaces) definiscono e utilizzano le strutture elencate nella tabella seguente.



| Struttura                                                                      | Descrizione                                                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**DEF. ADS \_ attr \_**](/windows/desktop/api/Iads/ns-iads-ads_attr_def)<br/>                              | Descrive un set di definizioni di attributi di un oggetto **attributeSchema** .<br/>                          |
| [**\_info attr \_ ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)<br/>                            | Include il valore di un attributo denominato e specifica le operazioni per la modifica dell'attributo.<br/>              |
| [**\_BACKLINK annunci**](/windows/win32/api/iads/ns-iads-ads_backlink)<br/>                               | Rappresenta una rappresentazione ADSI dell'attributo **back link** .<br/>                                   |
| [**\_elenco CASEIGNORE \_ ADS**](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)<br/>                | Rappresenta una rappresentazione ADSI dell'attributo dell' **elenco Case Ignore** .<br/>                            |
| [**\_classe Ads \_ def**](/windows/desktop/api/Iads/ns-iads-ads_class_def)<br/>                            | Descrive i dati dello schema per un oggetto.<br/>                                                                |
| [**\_DN Ads \_ con \_ binario**](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)<br/>                 | Struttura ADSI-defined che esegue il mapping di un nome distinto a un **GUID** dell'oggetto.<br/>                     |
| [**\_DN Ads \_ con \_ stringa**](/windows/win32/api/iads/ns-iads-ads_dn_with_string)<br/>                 | Struttura ADSI-defined che esegue il mapping di un nome distinto di un oggetto a un valore di stringa non variabile.<br/> |
| [**\_posta elettronica ADS**](/windows/win32/api/iads/ns-iads-ads_email)<br/>                                     | Rappresenta una rappresentazione ADSI dell'attributo **email** .<br/>                                       |
| [**\_NUMEROFAX ADS**](/windows/win32/api/iads/ns-iads-ads_faxnumber)<br/>                             | Rappresenta una rappresentazione ADSI dell'attributo del **numero di telefono del fax** .<br/>                  |
| [**\_attesa annunci**](/windows/win32/api/iads/ns-iads-ads_hold)<br/>                                       | Rappresenta una rappresentazione ADSI dell'attributo di **attesa** .<br/>                                        |
| [**\_Netaddress ADS**](/windows/win32/api/iads/ns-iads-ads_netaddress)<br/>                           | Rappresenta una rappresentazione ADSI dell'attributo **net Address** .<br/>                                 |
| [**descrittore di sicurezza di ADS \_ NT \_ \_**](/windows/win32/api/iads/ns-iads-ads_nt_security_descriptor)<br/> | Descrive un descrittore di sicurezza.<br/>                                                                    |
| [**\_informazioni sugli oggetti ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_object_info)<br/>                        | Descrive i dati degli oggetti del servizio directory.<br/>                                                            |
| [**\_elenco degli ottetti Ads \_**](/windows/desktop/api/Iads/ns-iads-ads_octet_list)<br/>                          | Rappresenta una rappresentazione ADSI dell'attributo dell' **elenco di ottetti** .<br/>                                  |
| [**\_stringa di ottetto Ads \_**](/windows/win32/api/iads/ns-iads-ads_octet_string)<br/>                      | Rappresenta una rappresentazione ADSI dell'attributo **stringa ottetto** .<br/>                                |
| [**\_percorso annunci**](/windows/win32/api/iads/ns-iads-ads_path)<br/>                                       | Rappresenta una rappresentazione ADSI dell'attributo **path** .<br/>                                        |
| [**\_POSTALADDRESS ADS**](/windows/win32/api/iads/ns-iads-ads_postaladdress)<br/>                     | Rappresenta una rappresentazione ADSI dell'attributo dell' **Indirizzo postale** .<br/>                              |
| [**ANNUNCI \_ \_ specifici**](/windows/win32/api/iads/ns-iads-ads_prov_specific)<br/>                    | Descrive un tipo di dati specifico del provider.<br/>                                                            |
| [**\_REPLICAPOINTER ADS**](/windows/win32/api/iads/ns-iads-ads_replicapointer)<br/>                   | Rappresenta una rappresentazione ADSI dell'attributo del puntatore di replica.<br/>                                 |
| [**\_colonna di ricerca Ads \_**](/windows/desktop/api/Iads/ns-iads-ads_search_column)<br/>                    | Rappresenta una colonna risultante da una query di directory.<br/>                                               |
| [**\_informazioni SEARCHPREF \_ ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)<br/>                | Descrive le preferenze di query.<br/>                                                                        |
| [**\_SORTKEY ADS**](/windows/desktop/api/Iads/ns-iads-ads_sortkey)<br/>                                 | Descrive la chiave di ordinamento utilizzata per l'ordinamento di una query.<br/>                                                    |
| [**\_timestamp ADS**](/windows/win32/api/iads/ns-iads-ads_timestamp)<br/>                             | Rappresenta una rappresentazione ADSI dell'attributo **timestamp** .<br/>                                   |
| [**ADS \_ digitato**](/windows/win32/api/iads/ns-iads-ads_typedname)<br/>                             | Rappresenta una rappresentazione ADSI dell'attributo del **nome tipizzato** .<br/>                                  |
| [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)<br/>                                        | Descrive il valore di un tipo di dati ADSI.<br/>                                                           |
| [**\_VLV ADS**](/windows/desktop/api/Iads/ns-iads-ads_vlv)<br/>                                         | Specifica che la visualizzazione elenco virtuale deve essere utilizzata quando vengono restituiti i risultati della ricerca dal server.<br/>  |



 

 

 





