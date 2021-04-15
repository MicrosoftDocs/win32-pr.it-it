---
title: Terminologia pipe essenziale
description: Analogamente ad altri tipi di parametri per le chiamate a procedure remote, le pipe possono essere \ in \ o \ out \ Parameters.
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df183d18d7962ad0c63ecaa0d350006a4144f23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517019"
---
# <a name="essential-pipe-terminology"></a>Terminologia pipe essenziale

Analogamente ad altri tipi di parametri per le chiamate di procedure remote, le pipe possono essere \[ parametri [**in**](/windows/desktop/Midl/in) \] o \[ [**out**](/windows/desktop/Midl/out-idl) \] . Poiché il server controlla il trasferimento dei dati tramite una pipe, le pipe con l' \[  \] attributo in si dicono di eseguire il *pull* dei dati nel server. Analogamente, le pipe di output effettuano il *push* dei dati dal server al client. Le procedure che eseguono il trasferimento dei dati sono denominate rispettivamente la *procedura pull* e la *procedura push*.

Il compilatore MIDL genera le procedure push e pull per il server. Inoltre, gestisce l'allocazione dei buffer di dati in memoria. Tuttavia, il client deve fornire le proprie procedure push e pull. Deve inoltre fornire una procedura per l'allocazione dei buffer di memoria utilizzati dalla pipe. Questi vengono chiamati automaticamente al momento appropriato dallo stub del client. La procedura di allocazione è spesso denominata routine Alloc o funzione Alloc.

 

 