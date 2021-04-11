---
title: File IDL e ACF
description: La sintassi del Microsoft Interface Definition Language (MIDL) si basa sulla sintassi del linguaggio di programmazione C. Quando un concetto di linguaggio in questa descrizione di MIDL non è completamente definito, la definizione del linguaggio C di tale termine è implicita.
ms.assetid: f99f5934-750d-4c30-9970-803a891cacb7
keywords:
- RPC (Remote Procedure Call), descritti, file IDL e ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f7f739e50fd4e04ae35a11adcbbc936cd3cb36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963282"
---
# <a name="the-idl-and-acf-files"></a>File IDL e ACF

La sintassi del Microsoft Interface Definition Language (MIDL) si basa sulla sintassi del linguaggio di programmazione C. Quando un concetto di linguaggio in questa descrizione di MIDL non è completamente definito, la definizione del linguaggio C di tale termine è implicita.

La progettazione MIDL specifica due file distinti: il file IDL (Interface Definition Language) e il file di configurazione dell'applicazione (ACF). Questi file contengono attributi che indirizzano la generazione dei file stub del linguaggio C che gestiscono la chiamata RPC (Remote Procedure Call). Il file IDL contiene una descrizione dell'interfaccia tra il client e i programmi server. Le applicazioni RPC utilizzano il file ACF per descrivere le caratteristiche dell'interfaccia specifiche dell'hardware e del sistema operativo che costituiscono un particolare ambiente operativo. Lo scopo della divisione di queste informazioni in due file consiste nel lasciare l'interfaccia software separata dalle caratteristiche che interessano solo l'ambiente operativo.

Il file IDL specifica un contratto di rete tra il client e il server, ovvero il file IDL specifica le informazioni trasmesse tra il client e il server. Mantenendo queste informazioni separate dalle informazioni sull'ambiente operativo, il file IDL viene reso portabile in altri ambienti. Il file IDL è costituito da due parti: un' [intestazione di interfaccia](the-idl-interface-header.md) e un [corpo dell'interfaccia](the-idl-interface-body.md).

L'ACF specifica gli attributi che influiscono solo sulle prestazioni locali piuttosto che sul contratto di rete. Microsoft RPC consente di combinare gli attributi ACF e IDL in un unico file IDL. È anche possibile combinare più interfacce in un singolo file IDL (e nel relativo ACF).

In questa sezione vengono riepilogati gli attributi specificati nei file IDL e ACF. È destinato solo a fornire una panoramica. Per informazioni più dettagliate, vedere la Guida di [riferimento al linguaggio MIDL](/windows/desktop/Midl/midl-language-reference)e il [riferimento a MIDL Command-Line](/windows/desktop/Midl/midl-command-line-reference). Le informazioni contenute in questa sezione sono illustrate negli argomenti seguenti:

-   [File IDL (Interface Definition Language)](the-interface-definition-language-idl-file.md)
-   [Il file di configurazione dell'applicazione (ACF)](the-application-configuration-file-acf-.md)
-   [Output del compilatore MIDL](midl-compiler-output.md)

 

 