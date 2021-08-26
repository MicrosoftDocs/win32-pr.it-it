---
title: Modello RPC
description: Rpc (Remote Procedure Call) per i linguaggi di programmazione C e C++ è progettato per soddisfare le esigenze degli sviluppatori che lavorano alla prossima generazione di software per i sistemi operativi Windows C++.
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- RPC Remote Procedure Call, descritto, il modello RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4c21a9fbbff24f4aafe9bad67186b65f4e3411b507d07953e29f806c6ff73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019711"
---
# <a name="the-rpc-model"></a>Modello RPC

Rpc (Remote Procedure Call) per i linguaggi di programmazione C e C++ è progettato per soddisfare le esigenze degli sviluppatori che lavorano alla prossima generazione di software per i sistemi operativi Windows C++.

RPC è un meccanismo di comunicazione interprocesso (IPC) potente, affidabile, efficiente e sicuro che consente lo scambio di dati e la chiamata di funzionalità che risiedono in un processo diverso. Questo processo diverso può essere nello stesso computer, nella rete locale o in Internet. In questa sezione vengono illustrati il modello di programmazione RPC e il modello per i sistemi distribuiti che possono essere implementati tramite RPC.

RPC supporta completamente l'autenticazione Windows a 64 bit. Esistono tre tipi di processi: processi nativi a 32 bit, processi nativi a 64 bit e processi a 32 bit in esecuzione nell'emulatore di processi a 32 bit in un sistema a 64 bit (spesso definiti processi WOW64). Per altre informazioni su WOW64, vedere [Esecuzione di applicazioni a 32 bit.](/windows/desktop/WinProg64/running-32-bit-applications) Tramite RPC, gli sviluppatori possono comunicare in modo trasparente tra diversi tipi di processo. RPC gestisce automaticamente le differenze di processo in background.

RPC è stato inizialmente sviluppato come estensione di RPC OSF. Ad eccezione di alcune delle funzionalità avanzate, RPC è interoperatività con le implementazioni di RPC OSF di altri fornitori.

In questa sezione viene inoltre fornita una panoramica dei componenti RPC e del relativo funzionamento. Le informazioni vengono presentate negli argomenti seguenti:

-   [Modello di programmazione](the-programming-model.md)
-   [Modello per sistemi distribuiti](the-model-for-distributed-systems.md)
-   [Funzionamento di RPC](how-rpc-works.md)
-   [Componenti RPC Microsoft](microsoft-rpc-components.md)

 

 