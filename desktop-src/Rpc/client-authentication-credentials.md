---
title: Credenziali di autenticazione client
description: Ogni client autenticato deve fornire le credenziali di autenticazione al server.
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2410b073886ffd70409cd749ea90305faa8d4635754e8f9596547c47bb976800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932187"
---
# <a name="client-authentication-credentials"></a>Credenziali di autenticazione client

Ogni client autenticato deve fornire le credenziali di autenticazione al server. In RPC, il client archivia le credenziali di autenticazione nell'associazione tra il client e il server. A tale scopo, il client chiama [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).

Esistono due tipi di credenziali, implicite ed esplicite:

-   Le credenziali esplicite esistono quando il client fornisce nome utente, password e dominio.
-   Le credenziali implicite esistono quando il client usa le credenziali del token del thread o del processo che chiama le **funzioni RpcBindingSetAuthInfo** o **RpcBindingSetAuthInfoEx.**

I client devono evitare di fornire credenziali esplicite perché l'archiviazione, la modifica e il recupero di una password utente possono introdurre una vulnerabilità di sicurezza in un sistema distribuito se vengono usate credenziali esplicite.

Per usare credenziali implicite, il client chiama **RpcBindingSetAuthInfo**(*es*. Il sistema di sicurezza e RPC ottengono le credenziali dal token del thread o del processo da usare nella sessione di autenticazione.

Se il client usa credenziali esplicite, il quinto parametro di queste due funzioni è di tipo [**RPC \_ AUTH \_ IDENTITY \_ HANDLE**](rpc-auth-identity-handle.md). Si tratta di un tipo flessibile che è un puntatore a una struttura di dati. Il contenuto della struttura dei dati può differire con ogni servizio di autenticazione. Attualmente, gli SSP supportati da RPC richiedono che l'applicazione imposta **RPC \_ AUTH \_ IDENTITY \_ HANDLE** in modo che punti a una [**struttura SEC \_ WINNT \_ AUTH AUTH \_ IDENTITY.**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) La **struttura SEC \_ WINNT \_ AUTH \_ IDENTITY** contiene i campi per un nome utente, un dominio e una password.

 

 




