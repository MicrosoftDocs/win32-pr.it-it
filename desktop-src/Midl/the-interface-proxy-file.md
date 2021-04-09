---
title: File proxy di interfaccia
description: Il file proxy di interfaccia (U \_ p. c) è un file c che contiene routine equivalenti a quelle negli stub client e nei file stub del server di un'interfaccia di oggetto (com).
ms.assetid: f85f7384-a590-4146-9705-2e87f1a0a87a
keywords:
- MIDL e COM MIDL, interfacce, file proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be52b3561af03df0375212d729f64f41e3cdd7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955657"
---
# <a name="the-interface-proxy-file"></a>File proxy di interfaccia

Il file proxy di interfaccia (U \_ p. c) è un file c che contiene routine equivalenti a quelle negli stub client e nei file stub del server di un'interfaccia di oggetto (com). Questo file contiene le implementazioni delle routine surrogate per il client e il server in modalità inline del compilatore, i dati e i thunk equivalenti nelle modalità interpretate, nonché altri dati di Glue COM appropriati, ad esempio il proxy e lo stub vtable.

Il file proxy di interfaccia include le routine e i dati di supporto solo per i metodi delle interfacce definite nel file IDL corrente. Per chiarire questo comportamento, in questa sezione viene usato un esempio esteso. Quando si compila un file IDL con un'interfaccia come IFaceB che eredita da IFaceA, vengono generati i dati e le routine ausiliari correlati a IFaceB per il file proxy corrente, mentre l'interfaccia di base IFaceA i dati e le routine ausiliari correlati. si trovano nel proxy generato dal file IDL contenente la definizione IFaceA. Il compilatore genera tutti i dati necessari per identificare i surrogati dell'interfaccia di base e per delegarli quando necessario per supportare i metodi IFaceA usati tramite l'interfaccia IFaceB.

Per ogni metodo in un'interfaccia del file IDL corrente, il file proxy contiene i due metodi surrogati seguenti se compilati in modalità mista ([/OS](-os.md)) e dati dell'interprete equivalenti quando vengono compilati in modalità interprete ([/OI](-oi.md)).

-   Surrogato del lato client, ad esempio il \_ proxy del metodo IFaceB \_ in questo esempio.

    Questo surrogato sul lato client è il punto di ingresso virtuale a cui viene inviato il client, ad esempio IFaceB:: Method. Esegue il marshalling degli argomenti di input in un form transmittable, trasmette gli argomenti di marshalling insieme alle informazioni che identificano l'interfaccia e l'operazione, quindi esegue l'unmarshalling del valore restituito e degli eventuali argomenti di output quando l'operazione richiamata restituisce.

-   Surrogato lato server, ad esempio, \_ Stub metodo IFaceB \_ .

    Questo surrogato sul lato server è il punto di ingresso virtuale che il runtime sottostante invia al server per emulare il client. Esegue l'unmarshalling degli argomenti di input per replicare i dati del client, richiama l'implementazione del server della funzione di interfaccia, quindi esegue il marshalling e trasmette il valore restituito e gli eventuali argomenti di output al lato client.

Il nome predefinito per un file proxy generato da un file. idl è il file \_ p. c. utilizzare l'opzione del compilatore MIDL [**/proxy**](-proxy.md) per eseguire l'override del nome predefinito del file proxy di interfaccia. Le opzioni [**/ENV**](-env.md) e [**/out**](-out.md) influiscono sul file.

 

 




