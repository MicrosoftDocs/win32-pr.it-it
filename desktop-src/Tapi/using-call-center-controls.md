---
description: I controlli Call Center estendono il modello a oggetti TAPI 3 per supportare i requisiti dei sistemi di distribuzione automatica delle chiamate (ACD).
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: Uso di controlli Call Center
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc01cac4b068c5ec17ff5794e2e7ffff46dbf95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308871"
---
# <a name="using-call-center-controls"></a>Uso di controlli Call Center

I controlli Call Center estendono il modello a oggetti TAPI 3 per supportare i requisiti dei sistemi di distribuzione automatica delle chiamate (ACD). Un Call Center è una località con agenti o operatori presso le banche dei telefoni, che effettuano chiamate telefoniche in uscita o che invadono in campo. Ad esempio, una società banca o una carta di credito utilizzerà un Call Center per elaborare le richieste di account.

Le applicazioni del Call Center sono divise in tre tipi di base:

-   [Proxy ACD](acd-proxy.md): gestisce le sessioni in ingresso o in uscita nel server, che può essere qualsiasi elemento da un telefono proprietario a un gateway Internet.
-   [Client agente ACD](acd-agent-client.md): Servizi di un singolo agente che riceve o chiama.
-   Client Supervisor ACD: fornisce una panoramica generale delle operazioni di Agent e ACD.

> [!Note]  
> Per Windows 2000, la funzionalità proxy è disponibile tramite TAPI 2,2 e le funzioni di Supervisore non sono implementate.

 

La sezione Samples del Windows SDK contiene esempi di codice ACD in Netds \\ TAPI \\ Tapi2 \\ ACD e Netds \\ TAPI \\ Tapi3 \\ ACD.

 

 



