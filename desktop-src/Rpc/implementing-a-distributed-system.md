---
title: Implementazione di un sistema distribuito
description: Un modo per implementare il software in un sistema distribuito è usare il supporto di rete non elaborato.
ms.assetid: 46abbbec-caa1-4fee-a713-4a4a2b462051
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098263f916129115f41840e15ac689fab7e4544621989d1a4d3179e50ef17d27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020530"
---
# <a name="implementing-a-distributed-system"></a>Implementazione di un sistema distribuito

Un modo per implementare il software in un sistema distribuito è usare il supporto di rete non elaborato. Questo approccio include socket, named pipe o POST HTTP, GET e così via. Tutti questi modelli forzano lo sviluppatore a usare primitive di programmazione di basso livello, in un modo o nell'altro, che forzano lo sviluppatore a gestire la rappresentazione dei dati di rete (NDR), la creazione di pacchetti dei dati, la gestione del traffico di rete e delle condizioni di errore, la protezione e la crittografia dell'integrità dei dati e così via.

RPC offre un modello di programmazione in cui lo sviluppatore mantiene il controllo granulare dell'interazione di rete tra il client e il server tramite un'API ricca, risparmiando allo stesso tempo gli sviluppatori dai dettagli e dagli oneri che un sistema distribuito tende a introdurre.

Si consideri, ad esempio, l'onere associato ai vari approcci per proteggere l'integrità e la privacy degli scambi di messaggi in un sistema distribuito. Quando si considera la sicurezza di rete per gli scambi di pacchetti, alcune protezioni sono più deboli, altre più potenti. Non esiste una vera sicurezza di rete, ma solo vari meccanismi di sicurezza basati su pacchetti. sicurezza che identifica il chiamante (che tende a essere debole anche perché il contenuto dei pacchetti può spesso essere modificato in transito), sicurezza che protegge l'integrità del pacchetto senza proteggere la propria privacy (varie firme e hash) e la sicurezza che protegge la privacy dello scambio di messaggi (vari meccanismi di crittografia).

Un altro onere dell'implementazione di un sistema distribuito sicuro è quello degli algoritmi necessari per implementare primitive di sicurezza, ad esempio crittografia, firma, autenticazione e così via. Uno sviluppatore può implementare questi algoritmi, ma questa operazione è difficile, erta e persino rischiosa, poiché gli algoritmi risultanti spesso hanno piccoli difetti di sicurezza. In alternativa, uno sviluppatore può usare un provider di sicurezza disponibile per implementare la protezione per le interazioni di rete all'interno di un sistema distribuito.

Usando RPC, entrambi questi oneri vengono risolti molto facilmente. Uno sviluppatore deve semplicemente indicare a RPC quale pacchetto di sicurezza usare e quale protezione della sicurezza deve essere applicata allo scambio di messaggi (in termini di autenticazione, crittografia, autenticazione reciproca, rilevamento delle identità chiamante e così via). RPC si occupa di tutti i dettagli dietro le quinte in modo efficiente, ma fornisce allo sviluppatore il controllo completo su esattamente come verranno protetti i dati.

 

 




