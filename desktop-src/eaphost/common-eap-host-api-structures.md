---
title: Strutture API EAPHost comuni
description: Informazioni sulle strutture API EAPHost comuni. Vedere un elenco di strutture usate da tutte le tecnologie EAPHost.
ms.assetid: f6f3b909-1e89-47f8-853c-c0f3f2414817
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b44a94aae1f18336dae8c11a1dc0217dc7c8d08
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730386"
---
# <a name="common-eaphost-api-structures"></a>Strutture API EAPHost comuni

La tabella seguente elenca le strutture comuni a tutte le tecnologie API EAPHost.



| Struttura                                                                | Descrizione                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_attributo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)                                  | Contiene un attributo EAP.                                                                                                                                                                                              |
| [**\_attributi EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes)                                | Contiene una matrice di attributi EAP.                                                                                                                                                                                    |
| [**\_matrice di \_ campi di input configurazione \_ EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Contiene un set di strutture di [**dati del campo di \_ input di configurazione \_ \_ \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) che contengono collettivamente i dati dei campi di input dell'utente ottenuti da una finestra di dialogo di configurazione Single Sign-on (SSO) EAP. |
| [**\_dati del \_ campo di input configurazione \_ EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Contiene i dati associati a un singolo campo di input in una finestra di dialogo di configurazione di EAP Single Sign-on (SSO).                                                                                                              |
| [**\_errore EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)                                          | Contiene dati relativi a un errore che si è verificato durante un'operazione EAPHost.                                                                                                                                                 |
| [**\_informazioni sul metodo EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info)                             | Contiene dati specifici per un metodo EAP.                                                                                                                                                                               |
| [**informazioni sul metodo EAP, ad \_ \_ \_ esempio**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex)                      | Windows Vista con Service Pack 1 (SP1) o versione successiva: contiene dati specifici per un metodo EAP.                                                                                                                             |
| [**\_ \_ Array informazioni metodo \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array)                | Contiene informazioni sui metodi EAP installati nel computer client.                                                                                                                                                   |
| [**matrice informazioni sul metodo EAP, ad \_ \_ \_ \_ esempio**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array_ex)         | Windows Vista con SP1 o versione successiva: contiene informazioni su tutti i metodi EAP installati nel computer client.                                                                                                    |
| [**\_tipo di metodo EAP \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type)                             | Contiene i dati di tipo, identificazione e autore per un metodo EAP.                                                                                                                                                       |
| [**\_tipo EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type)                                            | Contiene i dati di identificazione del tipo e del fornitore per un metodo EAP.                                                                                                                                                         |
| [**EapPacket**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket)                                           | Contiene un pacchetto di dati opachi inviati durante una sessione di autenticazione EAP.                                                                                                                                             |



 

 

 




