---
description: I controlli call center estendono il modello a oggetti TAPI 3 per supportare i requisiti dei sistemi di distribuzione automatica delle chiamate (ACD).
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: Uso dei controlli call center
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f166658cce86faa0003b762ec697286a434a06b36b18ae92a861d1f6757fa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991541"
---
# <a name="using-call-center-controls"></a>Uso dei controlli call center

I controlli call center estendono il modello a oggetti TAPI 3 per supportare i requisiti dei sistemi di distribuzione automatica delle chiamate (ACD). Un call center è una posizione con agenti o operatori presso banche telefoniche che effettuano chiamate telefoniche in uscita o che effettuano chiamate in ingresso sul campo. Ad esempio, una banca o una società di carte di credito userà un call center per elaborare le richieste di account.

Le applicazioni call center sono suddivise in tre tipi di base:

-   [Proxy ACD:](acd-proxy.md)gestisce le sessioni in ingresso o in uscita nel server, che possono essere qualsiasi cosa, da un commutatore telefonico proprietario a un gateway Internet.
-   [Client agente ACD:](acd-agent-client.md)servizi a un singolo agente che riceve o effettua chiamate.
-   ACD Supervisor Client: offre una visualizzazione generale delle operazioni di agente e ACD.

> [!Note]  
> Per Windows 2000, la funzionalità proxy è disponibile tramite TAPI 2.2 e le funzioni supervisore non sono implementate.

 

La sezione degli esempi di Windows SDK contiene esempi di codice ACD in Netds \\ \\ Tapi Tapi2 \\ Acd e Netds \\ \\ Tapi Tapi3 \\ Acd.

 

 



