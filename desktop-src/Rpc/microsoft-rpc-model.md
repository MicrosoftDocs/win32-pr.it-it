---
title: Modello RPC
description: La chiamata RPC (Remote Procedure Call) per i linguaggi di programmazione C e C++ è progettata per soddisfare le esigenze degli sviluppatori che lavorano alla prossima generazione di software per i sistemi operativi Windows.
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- RPC (Remote Procedure Call), descritto, modello RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e72048b12329133fcc8ce4ee82bce266ed29162
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729415"
---
# <a name="the-rpc-model"></a>Modello RPC

La chiamata RPC (Remote Procedure Call) per i linguaggi di programmazione C e C++ è progettata per soddisfare le esigenze degli sviluppatori che lavorano alla prossima generazione di software per i sistemi operativi Windows.

RPC è un meccanismo di comunicazione interprocesso potente, affidabile, efficiente e sicuro che consente lo scambio di dati e la chiamata di funzionalità che risiedono in un processo diverso. Il processo diverso può trovarsi nello stesso computer, nella rete locale o in Internet. In questa sezione vengono illustrati il modello di programmazione RPC e il modello per i sistemi distribuiti che possono essere implementati tramite RPC.

RPC supporta completamente Windows a 64 bit. Esistono tre tipi di processi: processi a 32 bit nativi, processi a 64 bit nativi e processi a 32 bit in esecuzione nell'emulatore di processi a 32 bit in un sistema a 64 bit (spesso definito processi WOW64). Per ulteriori informazioni su WOW64, vedere [esecuzione di applicazioni a 32 bit](/windows/desktop/WinProg64/running-32-bit-applications). Utilizzando RPC, gli sviluppatori possono comunicare in modo trasparente tra diversi tipi di processo. RPC gestisce automaticamente le differenze di processo dietro le quinte.

Inizialmente RPC è stato sviluppato come estensione per la RPC OSF. Ad eccezione di alcune funzionalità avanzate, RPC è interoperativo con le implementazioni di altri fornitori di OSF RPC.

In questa sezione viene inoltre fornita una panoramica dei componenti RPC e del relativo funzionamento. Le informazioni vengono presentate negli argomenti seguenti:

-   [Modello di programmazione](the-programming-model.md)
-   [Modello per sistemi distribuiti](the-model-for-distributed-systems.md)
-   [Funzionamento di RPC](how-rpc-works.md)
-   [Componenti RPC Microsoft](microsoft-rpc-components.md)

 

 