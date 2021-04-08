---
description: Esistono due ingredienti per determinare il comportamento di rappresentazione dell'autorità che il client concede in modo esplicito al server tramite un livello di rappresentazione e la capacità dei server di mascherare la propria identità quando effettuano chiamate per conto dei client.
ms.assetid: b34264ff-eb6a-4b99-8c0e-ab6b969a7fb1
title: Mascheramento (Servizi componenti)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5cba98d229c7f2132a2a1c345e65900b634afe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748082"
---
# <a name="cloaking-component-services"></a>Mascheramento (Servizi componenti)

Esistono due ingredienti per determinare il comportamento della rappresentazione: l'autorità che il client concede in modo esplicito il server attraverso un livello di rappresentazione e la capacità del server di mascherare la propria identità quando effettuano chiamate per conto del client. Questa seconda funzionalità è nota come *mascheramento*. Il cloaking ha a che fare con l'identità di sicurezza in cui il server effettua le chiamate.

Quando il server rappresenta il client, ha accesso diretto alle credenziali di sicurezza del client. In un senso molto locale, il thread del server acquisisce l'identità del client. Tuttavia, quando il server effettua chiamate all'esterno del processo, l'identità del client non verrà necessariamente proiettata come identità con cui viene effettuata la chiamata.

Quando il mascheramento è abilitato, le chiamate effettuate dal server che rappresenta il client possono essere effettuate con l'identità del client. Quando il mascheramento è disabilitato, le chiamate dal server verranno effettuate nell'identità del server.

Sono inoltre disponibili due forme di mascheramento, mascheramento *statico* e *mascheramento dinamico*, che possono essere descritte come segue:

-   Rappresentazione con mascheramento statico. L'identità client originale (realizzata come token del thread del server) può essere presentata una volta a un server downstream in una chiamata usando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), impostando l'identità client originale una volta sul proxy e il token del thread verrà usato nelle chiamate al metodo successive.
-   Rappresentazione con mascheramento dinamico. L'identità client originale viene individuata come token del thread del server per ogni chiamata al metodo al server downstream. In effetti, l'identità presentata può essere determinata dinamicamente. L'overhead necessario per eseguire questa operazione può essere notevolmente più costoso.

Per le applicazioni COM+, la configurazione predefinita è per la funzionalità di mascheramento dinamico. Questa operazione può essere modificata a livello di programmazione e amministrativa. Sebbene il mascheramento dinamico possa avere un sovraccarico delle prestazioni, offre la flessibilità che in genere è necessaria per circostanze che richiedono l'uso della rappresentazione.

Per informazioni più dettagliate sul mascheramento e descrizioni precise dei comportamenti possibili, vedere [mascheramento](/windows/desktop/com/cloaking) nella documentazione com.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rappresentazione e delega client](client-impersonation-and-delegation.md)
</dt> <dt>

[Requisiti lato client per la rappresentazione](client-side-requirements-for-impersonation.md)
</dt> <dt>

[Requisiti lato server per la rappresentazione](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
