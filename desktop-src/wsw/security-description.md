---
title: Descrizione della sicurezza
description: Una descrizione della sicurezza è rappresentata da una struttura WS SECURITY DESCRIPTION e viene fornita un'istanza di una descrizione di sicurezza quando si chiama la funzione WsCreateChannel per creare un canale protetto o la funzione \_ WsCreateListener per creare \_ un listener.
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- Servizi Web di descrizione della sicurezza per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a2395e2c1e894968f47fa41e98599ec333f6d2724cf6ffe6cbc5219396bca6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083161"
---
# <a name="security-description"></a>Descrizione della sicurezza

Una descrizione della sicurezza è rappresentata da una struttura [**WS \_ SECURITY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) e viene fornita un'istanza di una descrizione di sicurezza quando si chiama la funzione [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) per creare un canale protetto o la funzione [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) per creare un listener.


## <a name="structure-of-a-security-description"></a>Struttura di una descrizione di sicurezza

Il modello di base della sicurezza del canale è che un canale è protetto con uno o più token di sicurezza. In base a questo modello, la struttura [**WS \_ SECURITY \_ DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) contiene un elenco di associazioni di sicurezza, rappresentate dalle strutture [**\_ WS SECURITY \_ BINDING,**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) e ogni associazione di sicurezza descrive come un token di sicurezza viene ottenuto e usato nel canale. Il tipo di sicurezza usato in un canale è deciso dalla selezione dei sottotipi di associazione di sicurezza inclusi nella descrizione della sicurezza.

Le impostazioni di sicurezza facoltative specifiche di un'associazione di sicurezza vengono specificate come impostazioni [di associazione di sicurezza](security-binding-settings.md) nella struttura dell'associazione di sicurezza. Tuttavia, le impostazioni a livello di canale [](security-channel-settings.md) indipendenti dalle associazioni di sicurezza vengono specificate direttamente come impostazioni del canale di sicurezza nel campo **delle** proprietà della descrizione di sicurezza stessa.

![Diagramma che mostra la struttura di una descrizione della sicurezza.](images/securitydescription.png)

Gli elementi API seguenti vengono usati con le descrizioni di sicurezza.

| Struttura                                                    | Descrizione                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**DESCRIZIONE DELLA SICUREZZA DI WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | Struttura di primo livello usata per specificare i requisiti di sicurezza per un canale (sul lato client) o un listener (sul lato server). |



 

 

 




