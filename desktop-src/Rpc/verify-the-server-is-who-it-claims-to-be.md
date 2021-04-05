---
title: Verificare che il server sia quello che dichiara di essere
description: È preferibile usare l'autenticazione reciproca e verificare quindi l'identità del server.
ms.assetid: 6636a865-0e3b-4e52-81bb-0df48285e928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e16ae6a87134a9fbc783d35216a1c4df56ce2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710576"
---
# <a name="verify-the-server-is-who-it-claims-to-be"></a>Verificare che il server sia quello che dichiara di essere

È preferibile usare l'autenticazione reciproca e verificare quindi l'identità del server. Un esempio di errore comune che non riesce a eseguire questa operazione è costituito dalle applicazioni che dispongono di un servizio locale in cui i client chiamano. In alcune configurazioni, un amministratore può decidere che il servizio di sistema non è molto utile e può scegliere di arrestarlo. Un utente malintenzionato inventivo in un computer Terminal Server può avviare un processo che rimane in ascolto sullo stesso endpoint e quando un client si connette a un endpoint, consentendo la rappresentazione sul server senza autenticare reciprocamente il server, l'autore dell'attacco può rappresentare il client e accedere ai dati del client oppure effettuare chiamate di rete per conto del client. La maggior parte dei servizi di sistema viene eseguita con un account noto, ad esempio LocalSysyem, LocalService o NetworkService, che può essere verificato utilizzando l'autenticazione reciproca.

 

 




