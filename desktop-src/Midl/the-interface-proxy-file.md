---
title: File del proxy di interfaccia
description: Il file proxy di interfaccia (U p.c) è un file C che contiene routine equivalenti a quelle nei file stub client e server di un'interfaccia \_ di oggetto (COM).
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- MIDL e COM MIDL, interfacce, file proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dedb9de50d00524b1e038f027448be5aaab369aa5d92243d2a3425bf603cd65a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013539"
---
# <a name="the-interface-proxy-file"></a>File del proxy di interfaccia

Il file proxy di interfaccia (U p.c) è un file C che contiene routine equivalenti a quelle nei file stub client e server di un'interfaccia \_ di oggetto (COM). Questo file contiene implementazioni delle routine surrogate per client e server in modalità inline del compilatore o dati e thunk equivalenti nelle modalità interpretate, nonché altri dati glue COM appropriati, ad esempio proxy e stub Vtable.

Il file proxy di interfaccia include le routine e i dati di supporto solo per i metodi delle interfacce definite nel file IDL corrente. Per chiarire questo comportamento, in questa sezione viene usato un esempio esteso. Quando si compila un file IDL con un'interfaccia come IFaceB che eredita da IFaceA, i dati ausiliari e le routine correlati a IFaceB vengono generati nel file proxy corrente, mentre i dati ausiliari correlati a IFaceA vengono trovati nel proxy generato dal file IDL contenente la definizione IFaceA. Il compilatore genera tutti i dati necessari per identificare i surrogati dell'interfaccia di base e delegarli quando necessario per supportare i metodi IFaceA usati tramite l'interfaccia IFaceB.

Per ogni metodo in un'interfaccia nel file IDL corrente, il file proxy contiene i due metodi surrogati seguenti quando vengono compilati in modalità mista ([/Os](-os.md)) e dati dell'interprete equivalenti quando vengono compilati in modalità interprete ([/Oi](-oi.md)).

-   Surrogato sul lato client, ad esempio IFaceB \_ Method Proxy in questo \_ esempio.

    Questo surrogato sul lato client è il punto di ingresso virtuale a cui il client, ad esempio IFaceB::Method, invia. Effettua il marshalling degli argomenti di input in un formato trasmettibile, trasmette gli argomenti sottoposti a marshalling insieme alle informazioni che identificano l'interfaccia e l'operazione e quindi annulla ilmarshaling del valore restituito e di tutti gli argomenti di output quando l'operazione richiamata viene restituita.

-   Surrogato sul lato server, ad esempio stub del \_ metodo IFaceB \_ .

    Questo surrogato sul lato server è il punto di ingresso virtuale a cui il runtime sottostante invia al server per emulare il client. Esegue l'unmarshaling degli argomenti di input per replicare i dati del client, richiama l'implementazione del server della funzione di interfaccia, quindi effettua il marshalling e trasmette il valore restituito e gli eventuali argomenti di output al lato client.

Il nome predefinito per un file proxy generato da un file.idl è il file p.c.Usare l'opzione del compilatore \_ MIDL [**/proxy**](-proxy.md) per eseguire l'override del nome predefinito del file proxy di interfaccia. Le [**opzioni /env**](-env.md) [**e /out**](-out.md) influiscono su questo file.

 

 




