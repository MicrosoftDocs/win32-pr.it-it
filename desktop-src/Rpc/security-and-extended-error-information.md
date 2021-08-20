---
title: Informazioni sulla sicurezza e sugli errori estesi
description: Le informazioni sugli errori estesi offrono dati molto utili durante la risoluzione di un problema RPC, ma molti di questi dati vengono considerati riservati dalle organizzazioni che si sono consapevoli della sicurezza.
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f246e86dee31ea5e755c45211e3bd949657cdf95c37bf6ab4de3706be09fdec3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925688"
---
# <a name="security-and-extended-error-information"></a>Informazioni sulla sicurezza e sugli errori estesi

Le informazioni sugli errori estesi offrono dati molto utili durante la risoluzione di un problema RPC, ma molti di questi dati vengono considerati riservati dalle organizzazioni che si sono consapevoli della sicurezza. In considerazione di questi problemi di sicurezza, le informazioni sugli errori estesi sono disattivate per impostazione predefinita.

Le informazioni sugli errori estesi vengono comunque generate quando le informazioni sugli errori estesi sono disabilitate, ma non vengono mai trasmesse attraverso i limiti del processo o del computer. Questo approccio consente l'uso delle informazioni sugli errori da parte di strumenti che hanno accesso allo spazio degli indirizzi del processo, ad esempio i debugger. Quando è attivata, le informazioni sugli errori estesi vengono generate e possono essere inviate attraverso i limiti del processo e del computer. Attualmente, le informazioni sugli errori estesi vengono usate per le sequenze di protocollo orientate alla connessione e RPC locale (LRPC). Viene parzialmente implementato per i datagrammi.

 

 




