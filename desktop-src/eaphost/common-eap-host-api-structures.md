---
title: Strutture comuni dell'API EAPHost
description: Informazioni sulle strutture comuni dell'API EAPHost. Vedere un elenco delle strutture usate da tutte le tecnologie EAPHost.
ms.assetid: f6f3b909-1e89-47f8-853c-c0f3f2414817
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4740658f798eadee2a658df1a7f9f8fd44b386c4ac39b52bcf49e75887d2d719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984331"
---
# <a name="common-eaphost-api-structures"></a>Strutture comuni dell'API EAPHost

Nella tabella seguente sono elencate le strutture comuni a tutte le tecnologie API EAPHost.



| Struttura                                                                | Descrizione                                                                                                                                                                                                             |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ATTRIBUTO \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attribute)                                  | Contiene un attributo EAP.                                                                                                                                                                                              |
| [**ATTRIBUTI \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_attributes)                                | Contiene una matrice di attributi EAP.                                                                                                                                                                                    |
| [**MATRICE DI \_ CAMPI \_ DI INPUT \_ EAP CONFIG \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) | Contiene un set di strutture [**EAP \_ CONFIG INPUT FIELD \_ \_ \_ DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data) che contengono collettivamente i dati dei campi di input utente ottenuti da una finestra di dialogo di configurazione EAP Single Sign-On (SSO). |
| [**DATI DEI CAMPI \_ \_ DI INPUT \_ EAP CONFIG \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_data)   | Contiene i dati associati a un singolo campo di input in una finestra di dialogo di configurazione dell'accesso Single Sign-On (SSO) EAP.                                                                                                              |
| [**ERRORE \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_error)                                          | Contiene i dati relativi a un errore che si è verificato durante un'operazione EAPHost.                                                                                                                                                 |
| [**INFORMAZIONI SUL METODO EAP \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info)                             | Contiene dati specifici per un metodo EAP.                                                                                                                                                                               |
| [**INFORMAZIONI SUL METODO EAP \_ \_ \_ EX**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_ex)                      | Windows Vista con Service Pack 1 (SP1) o versione successiva: contiene dati specifici per un metodo EAP.                                                                                                                             |
| [**MATRICE DI INFORMAZIONI SUL METODO EAP \_ \_ \_**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array)                | Contiene informazioni sui metodi EAP installati nel computer client.                                                                                                                                                   |
| [**EAP \_ METHOD \_ INFO \_ ARRAY \_ EX**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info_array_ex)         | Windows Vista con SP1 o versione successiva: contiene informazioni su tutti i metodi EAP installati nel computer client.                                                                                                    |
| [**TIPO DI \_ METODO \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type)                             | Contiene i dati di tipo, identificazione e autore per un metodo EAP.                                                                                                                                                       |
| [**TIPO \_ EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_type)                                            | Contiene i dati di identificazione del tipo e del fornitore per un metodo EAP.                                                                                                                                                         |
| [**EapPacket**](/windows/win32/api/eapmethodtypes/ns-eapmethodtypes-eappacket)                                           | Contiene un pacchetto di dati opachi inviati durante una sessione di autenticazione EAP.                                                                                                                                             |



 

 

 




