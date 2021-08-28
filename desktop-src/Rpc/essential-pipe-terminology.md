---
title: Terminologia essenziale delle pipe
description: Analogamente ad altri tipi di parametri per le chiamate di procedura remota, le pipe possono essere \ in\ o \ out\ parametri.
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 389885f440faa477ab22f2100685e2955cbf9fb7ddc4ffcb6440dc4b6f68e003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930070"
---
# <a name="essential-pipe-terminology"></a>Terminologia essenziale delle pipe

Analogamente ad altri tipi di parametri per le chiamate di procedura remota, le pipe possono essere \[ [**parametri in**](/windows/desktop/Midl/in) \] o \[ [**out.**](/windows/desktop/Midl/out-idl) \] Poiché il server controlla il trasferimento dei dati tramite una pipe, le pipe con l'attributo in vengono detto per \[  \] eseguire il *pull* dei dati nel server. Analogamente, le pipe di output *esegono il push* dei dati dal server al client. Le procedure che esegono il trasferimento dei dati sono denominate *rispettivamente procedura pull* *e procedura push.*

Il compilatore MIDL genera le procedure push e pull per il server. Gestisce inoltre l'allocazione dei buffer di dati in memoria. Tuttavia, il client deve fornire le proprie procedure push e pull. Deve anche fornire una procedura per allocare i buffer di memoria usati dalla pipe. Questi vengono chiamati automaticamente al momento appropriato dallo stub del client. La procedura di allocazione è spesso denominata routine alloc o funzione alloc.

 

 