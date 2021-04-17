---
description: Le dll TAPI, insieme al server TAPI (Tapisvr.exe), sono astrazioni cruciali che separano le applicazioni dell'utente finale o del server dai provider di servizi. Una DLL TAPI insieme al server TAPI fornisce un'interfaccia coerente tra i due livelli.
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: DLL TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8482045ec16a999957121aff669e93b34b605069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560450"
---
# <a name="tapi-dll"></a>DLL TAPI

Le dll TAPI, insieme al server TAPI (Tapisvr.exe), sono astrazioni cruciali che separano le applicazioni dell'utente finale o del server dai provider di servizi. Una DLL TAPI insieme al server TAPI fornisce un'interfaccia coerente tra i due livelli.

Un'applicazione TAPI carica la DLL appropriata nello spazio di elaborazione. Durante l'inizializzazione, TAPI stabilisce un collegamento RPC con Tapisvr.exe. Il server TAPI viene eseguito nel contesto di SVCHOST.

Sono disponibili tre DLL associate a TAPI: Tapi.dll, Tapi32.dll e Tapi3.dll. Queste dll si trovano in% SystemRoot% \\ system32. Nella figura seguente vengono illustrati i ruoli dei rispettivi ruoli in telefonia Microsoft:

![ruoli delle tre dll TAPI](images/dllserv.png)

Le applicazioni a 16 bit esistenti si collegano a Tapi.dll. Tapi.dll è semplicemente un livello thunk che esegue il mapping degli indirizzi a 16 bit a indirizzi a 32 bit e passa le richieste al Tapi32.dll.

Le applicazioni TAPI 2. x a 32 bit esistenti si collegano a Tapi32.dll. Tapi32.dll è un livello di marshalling sottile che trasferisce le richieste di funzione al server TAPI (TAPISRV) e, quando necessario, carica e richiama le dll del provider di servizi multimediali nel processo dell'applicazione.

Le applicazioni TAPI 3. x si collegano a Tapi3.dll.

 

 



