---
title: Componenti RPC
description: Componenti RPC (Remote Procedure Call).
ms.assetid: 7caaf01a-7f20-470f-afcf-478146cae5eb
keywords:
- RPC Remote Procedure Call , descritto, componenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b3416589eccf865b70d3da82fa7494631ab7592f172bb46c10eccb1d96fad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928120"
---
# <a name="rpc-components"></a>Componenti RPC

RPC include i componenti principali seguenti:

-   Compilatore MIDL
-   Librerie di runtime e file di intestazione
-   Provider di servizi dei nomi (noto anche come localizzatore)
-   Mapper di endpoint (talvolta definito mapper di porte)

Nel modello RPC è possibile specificare formalmente un'interfaccia per le procedure remote usando un linguaggio progettato a questo scopo. Questo linguaggio è detto linguaggio di definizione dell'interfaccia, o IDL. L'implementazione Microsoft di questo linguaggio è denominata Microsoft Interface Definition Language, o MIDL.

Dopo aver creato un'interfaccia, è necessario passarla tramite il compilatore MIDL. Questo compilatore genera gli stub che converte le chiamate di routine locali in chiamate di procedura remota. Gli stub sono funzioni segnaposto che eseguono le chiamate alle funzioni della libreria di runtime, che gestiscono la chiamata di procedura remota. Il vantaggio di questo approccio è che la rete diventa quasi completamente trasparente per l'applicazione distribuita. Il programma client chiama le procedure locali. il lavoro di trasformazione in chiamate remote viene eseguito automaticamente. Tutto il codice che converte i dati, accede alla rete e recupera i risultati viene generato automaticamente dal compilatore MIDL ed è invisibile all'applicazione.

 

 




