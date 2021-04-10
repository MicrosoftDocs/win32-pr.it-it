---
title: Componenti RPC
description: Componenti RPC (Remote Procedure Call).
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- RPC, descrizione, componenti di RPC (Remote Procedure Call)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c715a4f454ef28db20ee527e5e8f33f66200b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955524"
---
# <a name="rpc-components"></a>Componenti RPC

RPC include i componenti principali seguenti:

-   Compilatore MIDL
-   Librerie e file di intestazione della fase di esecuzione
-   Nome provider di servizi (a volte definito Locator)
-   Mapper di endpoint (noto anche come Mapper della porta)

Nel modello RPC è possibile specificare formalmente un'interfaccia per le procedure remote utilizzando una lingua progettata a questo scopo. Questo linguaggio è denominato linguaggio di definizione dell'interfaccia o IDL. L'implementazione Microsoft di questo linguaggio è denominata Microsoft Interface Definition Language o MIDL.

Dopo aver creato un'interfaccia, è necessario passarla tramite il compilatore MIDL. Questo compilatore genera gli stub che convertono le chiamate di procedure locali in chiamate a procedure remote. Gli stub sono funzioni segnaposto che eseguono chiamate alle funzioni della libreria di runtime, che gestiscono la chiamata RPC. Il vantaggio di questo approccio è che la rete diventa quasi completamente trasparente per l'applicazione distribuita. Il programma client chiama le procedure locali; il lavoro di trasformarli in chiamate remote viene eseguito automaticamente. Tutto il codice che converte i dati, accede alla rete e recupera i risultati vengono generati automaticamente dal compilatore MIDL ed è invisibile all'applicazione.

 

 




