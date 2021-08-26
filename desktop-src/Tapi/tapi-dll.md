---
description: Le DLL TAPI, insieme a TAPI Server (Tapisvr.exe), sono astrazioni cruciali che separano le applicazioni dell'utente finale o del server dai provider di servizi. Una DLL TAPI in combinazione con il server TAPI fornisce un'interfaccia coerente tra questi due livelli.
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: TAPI DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff26274baf25047212a3f9f8e15c2211d90cbaa10db23674ae54dbb97bbfdf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012206"
---
# <a name="tapi-dll"></a>TAPI DLL

Le DLL TAPI, insieme a TAPI Server (Tapisvr.exe), sono astrazioni cruciali che separano le applicazioni dell'utente finale o del server dai provider di servizi. Una DLL TAPI in combinazione con il server TAPI fornisce un'interfaccia coerente tra questi due livelli.

Un'applicazione TAPI carica la DLL appropriata nello spazio di elaborazione. Durante l'inizializzazione, TAPI stabilisce un collegamento RPC con Tapisvr.exe. Il server TAPI viene eseguito nel contesto di SVCHOST.

A TAPI sono associate tre DLL: Tapi.dll, Tapi32.dll e Tapi3.dll. Queste DLL si trovano in %SystemRoot% \\ system32. La figura seguente illustra i ruoli dei rispettivi ruoli in Telefonia Microsoft:

![ruoli delle tre DLL Tapi](images/dllserv.png)

Le applicazioni a 16 bit esistenti si collegano Tapi.dll. Tapi.dll è semplicemente un livello thunk che esegue il mapping degli indirizzi a 16 bit agli indirizzi a 32 bit e passa le richieste a Tapi32.dll.

Le applicazioni TAPI 2.x a 32 bit esistenti si collegano Tapi32.dll. Tapi32.dll è un livello di thin marshalling che trasferisce le richieste di funzione al server TAPISRV (TAPISRV) e, quando necessario, carica e richiama le DLL del provider di servizi multimediali nel processo dell'applicazione.

Le applicazioni TAPI 3.x si collegano Tapi3.dll.

 

 



