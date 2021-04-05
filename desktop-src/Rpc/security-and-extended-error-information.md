---
title: Informazioni sulla sicurezza e sugli errori estesi
description: Le informazioni estese sugli errori offrono dati molto utili per la risoluzione di un problema RPC, ma tali dati sono molti considerati riservati dalle organizzazioni con consapevolezza della sicurezza.
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b2029b40937dcef0622f6163e5e8f95b7006ade
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713552"
---
# <a name="security-and-extended-error-information"></a>Informazioni sulla sicurezza e sugli errori estesi

Le informazioni estese sugli errori offrono dati molto utili per la risoluzione di un problema RPC, ma tali dati sono molti considerati riservati dalle organizzazioni con consapevolezza della sicurezza. In considerazione di questi problemi di sicurezza, le informazioni estese sugli errori sono disattivate per impostazione predefinita.

Le informazioni estese sugli errori vengono comunque generate quando le informazioni estese sugli errori sono disabilitate, ma le informazioni non vengono mai trasmesse tra i limiti del processo o del computer Questo approccio consente di usare le informazioni sugli errori per gli strumenti che hanno accesso allo spazio degli indirizzi del processo, ad esempio i debugger. Se attivata, le informazioni estese sugli errori vengono generate e possono essere inviate attraverso i limiti del processo e del computer. Attualmente, le informazioni sugli errori estesi vengono utilizzate per le sequenze di protocollo orientate alla connessione e RPC locale (LRPC). È parzialmente implementato per datagrammi.

 

 




