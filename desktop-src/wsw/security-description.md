---
title: Descrizione della sicurezza
description: Un Descrizione di sicurezza è rappresentato da una \_ \_ struttura di descrizione della sicurezza WS e viene fornita un'istanza di una descrizione di sicurezza quando si chiama la funzione WsCreateChannel per creare un canale sicuro o la funzione WsCreateListener per creare un listener.
ms.assetid: 252418fc-dad4-43f4-a5e2-38055da3779c
keywords:
- Servizi Web per la descrizione della sicurezza per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c06e8553441b7eb813106213dbfa089810aad74c
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "104132134"
---
# <a name="security-description"></a>Descrizione della sicurezza

Un Descrizione di sicurezza è rappresentato da una struttura di [**\_ \_ Descrizione della sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) e viene fornita un'istanza di una descrizione di sicurezza quando si chiama la funzione [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) per creare un canale sicuro o la funzione [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener) per creare un listener.


## <a name="structure-of-a-security-description"></a>Struttura di una descrizione della sicurezza

Il modello di base della sicurezza del canale è che un canale è protetto da uno o più token di sicurezza. Riflettendo questo modello, la struttura di [**\_ \_ Descrizione della sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) contiene un elenco di associazioni di sicurezza, rappresentate dalle strutture di [**\_ \_ associazione di sicurezza WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding) , e ogni associazione di sicurezza descrive il modo in cui un token di sicurezza viene ottenuto e utilizzato sul canale. Il tipo di sicurezza utilizzato su un canale è determinato dalla selezione dei sottotipi di associazione di sicurezza inclusi nella descrizione della sicurezza.

Le impostazioni di sicurezza facoltative specifiche di un'associazione di sicurezza sono specificate come [impostazioni di associazione](security-binding-settings.md) di sicurezza nella struttura di associazione di sicurezza. Tuttavia, le impostazioni a livello di canale indipendenti dalle associazioni di sicurezza vengono specificate direttamente come [impostazioni del canale di sicurezza](security-channel-settings.md) nel campo **Proprietà** della descrizione di sicurezza.

![Diagramma che illustra la struttura di una descrizione di sicurezza.](images/securitydescription.png)

Gli elementi API seguenti vengono usati con le descrizioni di sicurezza.

| Struttura                                                    | Descrizione                                                                                                                              |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Descrizione della sicurezza WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) | Struttura di primo livello utilizzata per specificare i requisiti di sicurezza per un canale (sul lato client) o un listener (sul lato server). |



 

 

 




