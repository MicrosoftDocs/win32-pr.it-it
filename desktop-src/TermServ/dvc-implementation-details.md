---
title: Dettagli dell'implementazione di DVC
description: Questa sezione contiene informazioni su come scrivere un modulo client Dynamic Channel (DVC).
ms.assetid: 338556d9-e9a7-4926-a09c-8e2ce1627467
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 876722736a95b45918d8a5b9e229f4f9eda5840b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298051"
---
# <a name="dvc-implementation-details"></a>Dettagli dell'implementazione di DVC

Questa sezione contiene informazioni su come scrivere un modulo client Dynamic Channel (DVC).

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Scrittura di un modulo client DVC](writing-a-client-dvc-component.md)
</dt> <dd>

Per scrivere un modulo client Dynamic Channel (DVC), è necessario innanzitutto implementare e registrare un plug-in client di Connessione Desktop remoto (RDC).

</dd> <dt>

[Registrazione del plug-in DVC](dvc-plug-in-registration.md)
</dt> <dd>

Viene descritta la sintassi per la voce del plug-in Dynamic Virtual Channel (DVC) per il client Connessione Desktop remoto (RDC).

</dd> <dt>

[Avvio di un listener DVC](starting-a-dvc-listener.md)
</dt> <dd>

Per stabilire una connessione corretta tra due moduli DVC (Dynamic Virtual Channel) in esecuzione nel client e nel server Connessione Desktop remoto (RDC), è necessario che un listener DVC sia in esecuzione e in stato di ascolto.

</dd> <dt>

[Accettazione di una connessione](accepting-a-connection.md)
</dt> <dd>

A un certo punto nel tempo, il client dinamico del canale virtuale (DVC) richiederà una connessione al listener di DVC.

</dd> <dt>

[Scrittura di dati tramite un canale DVC](writing-data-by-using-a-dvc-channel.md)
</dt> <dd>

La scrittura di dati del canale tramite un canale virtuale dinamico (DVC) è simmetrica sia per il server host sessione Desktop remoto (host sessione Desktop remoto) che per il client.

</dd> <dt>

[Test e debug](testing-and-debugging.md)
</dt> <dd>

È presente un listener "echo" implementato dal client Connessione Desktop remoto (RDC), che è sempre presente e in ascolto delle connessioni in ingresso.

</dd> <dt>

[Esempio di plug-in client DVC](dvc-client-plug-in-example.md)
</dt> <dd>

Esempio di codice C++ in cui viene illustrato come creare un plug-in del canale virtuale dinamico (DVC) client di Connessione Desktop remoto (RDC).

</dd> <dt>

[Esempio di modulo server DVC](dvc-server-component-example.md)
</dt> <dd>

Esempio di codice C++ che Mostra come creare il modulo canale virtuale dinamico lato server (DVC).

</dd> </dl>

 

 




