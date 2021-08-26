---
title: File IDL e ACF
description: La sintassi del Microsoft Interface Definition Language (MIDL) si basa sulla sintassi del linguaggio di programmazione C. Quando un concetto di linguaggio in questa descrizione di MIDL non è completamente definito, la definizione del linguaggio C di tale termine è implicita.
ms.assetid: f99f5934-750d-4c30-9970-803a891cacb7
keywords:
- RPC Remote Procedure Call , descritto, file IDL e ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788756c6762575d2366950f1b6412a76c03d14518acb1707dfdaf109ba2b5fc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017101"
---
# <a name="the-idl-and-acf-files"></a>File IDL e ACF

La sintassi del Microsoft Interface Definition Language (MIDL) si basa sulla sintassi del linguaggio di programmazione C. Quando un concetto di linguaggio in questa descrizione di MIDL non è completamente definito, la definizione del linguaggio C di tale termine è implicita.

La progettazione MIDL specifica due file distinti: il file IDL (Interface Definition Language) e il file di configurazione dell'applicazione (ACF). Questi file contengono attributi che indirizzano la generazione dei file stub del linguaggio C che gestiscono rpc (Remote Procedure Call). Il file IDL contiene una descrizione dell'interfaccia tra i programmi client e server. Le applicazioni RPC usano il file ACF per descrivere le caratteristiche dell'interfaccia specifiche dell'hardware e del sistema operativo che costituiscono un particolare ambiente operativo. Lo scopo di suddividere queste informazioni in due file è quello di mantenere l'interfaccia software separata dalle caratteristiche che interessano solo l'ambiente operativo.

Il file IDL specifica un contratto di rete tra il client e il server, ovvero il file IDL specifica ciò che viene trasmesso tra il client e il server. Mantenere queste informazioni diverse dalle informazioni sull'ambiente operativo rende il file IDL portabile in altri ambienti. Il file IDL è costituito da due parti: [un'intestazione di interfaccia e](the-idl-interface-header.md) un corpo [dell'interfaccia](the-idl-interface-body.md).

Il file ACF specifica gli attributi che influiscono solo sulle prestazioni locali anziché sul contratto di rete. Microsoft RPC consente di combinare gli attributi ACF e IDL in un singolo file IDL. È anche possibile combinare più interfacce in un singolo file IDL (e il relativo ACF).

In questa sezione vengono riepilogati gli attributi specificati nei file IDL e ACF. L'obiettivo è fornire solo una panoramica. Per informazioni più dettagliate, vedere MIDL Language Reference (Riferimenti al linguaggio [MIDL)](/windows/desktop/Midl/midl-language-reference)e [MIDL Command-Line Reference (Riferimento al linguaggio MIDL).](/windows/desktop/Midl/midl-command-line-reference) La discussione in questa sezione viene presentata negli argomenti seguenti:

-   [File IDL (Interface Definition Language)](the-interface-definition-language-idl-file.md)
-   [File di configurazione dell'applicazione (ACF)](the-application-configuration-file-acf-.md)
-   [Output del compilatore MIDL](midl-compiler-output.md)

 

 