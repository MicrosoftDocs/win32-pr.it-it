---
title: Chiusura di un protocollo di routing multicast
description: Nella tabella seguente viene riepilogata una serie di passaggi in un'interazione di arresto tra il gestore del gruppo multicast e il protocollo di routing quando il protocollo di routing viene arrestato.
ms.assetid: d868218d-7939-45d1-9e2f-3415c40f1a62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08d35285bdf613cb8ec5966fa438742004a97c0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729327"
---
# <a name="shutting-down-a-multicast-routing-protocol"></a>Chiusura di un protocollo di routing multicast

Nella tabella seguente viene riepilogata una serie di passaggi in un'interazione di arresto tra il gestore del gruppo multicast e il protocollo di routing quando il protocollo di routing viene arrestato. Nella prima colonna sono descritte le azioni eseguite dal protocollo di routing e le risposte del protocollo di routing al gestore del gruppo multicast. La seconda colonna descrive le risposte del gestore del gruppo multicast al protocollo di routing ed eventuali azioni eseguite dal gestore del gruppo multicast, ad esempio i callback. La terza colonna presenta informazioni aggiuntive.

Ogni riga della tabella rappresenta un passaggio.



| Azione protocollo di routing                                                                                                                                     | Azione gestione gruppi multicast                                                                                                                                                                                                                                                                                                                                                                                                                                            | Note                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| Rilasciare la proprietà di ogni interfaccia di cui il protocollo di routing è proprietario utilizzando la funzione [**MgmReleaseInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership) . | Se IGMP è in esecuzione anche sull'interfaccia appena rilasciata da un protocollo di routing, contattare IGMP usando il callback di [**\_ \_ \_ callback IGMP di PMGM Disable**](/windows/win32/api/mgm/nc-mgm-pmgm_disable_igmp_callback) . Dopo aver apportato tutte le modifiche ai dati multicast relativi alla proprietà dell'interfaccia, contattare di nuovo IGMP usando [**PMGM \_ enable \_ IGMP \_ callback**](/windows/desktop/api/Mgm/nc-mgm-pmgm_enable_igmp_callback) callback.<br/> Elimina tutte le voci di invio associate a questa interfaccia.<br/> |                                                                           |
| Annullare la registrazione con il gestore del gruppo multicast utilizzando la funzione [**MgmDeRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol) .                                    | Eliminare l'handle restituito al protocollo di routing da una chiamata precedente alla funzione [**MgmDeRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol) .                                                                                                                                                                                                                                                                                                                 | Il protocollo di routing non può più usare questo handle per chiamare le funzioni MGM. |



 

 

