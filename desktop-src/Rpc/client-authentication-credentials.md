---
title: Credenziali di autenticazione client
description: Ogni client autenticato deve fornire le credenziali di autenticazione al server.
ms.assetid: d567e944-8d68-4d95-be6a-840e30f57ba9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3704663411fc33340a462d8e3b356041b6061468
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045291"
---
# <a name="client-authentication-credentials"></a>Credenziali di autenticazione client

Ogni client autenticato deve fornire le credenziali di autenticazione al server. In RPC il client archivia le proprie credenziali di autenticazione nell'associazione tra il client e il server. A tale scopo, il client chiama [**RpcBindingSetAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo) o [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa).

Esistono due tipi di credenziali, implicite ed esplicite:

-   Le credenziali esplicite sono disponibili quando il client fornisce il nome utente, la password e il dominio.
-   Le credenziali implicite sono disponibili quando il client utilizza le credenziali del thread o del token di processo chiamando le funzioni **RpcBindingSetAuthInfo** o **RpcBindingSetAuthInfoEx** .

I client devono evitare di fornire credenziali esplicite perché l'archiviazione, la manipolazione e il recupero di una password utente possono introdurre una vulnerabilità di sicurezza in un sistema distribuito se vengono usate credenziali esplicite.

Per usare le credenziali implicite, il client chiama **RpcBindingSetAuthInfo**(ad *esempio*). Il sistema di sicurezza e RPC ottengono le credenziali dal thread o dal token del processo per l'uso nella sessione di autenticazione.

Se il client usa credenziali esplicite, il quinto parametro di queste due funzioni è di [**tipo \_ \_ \_ handle di identità di autenticazione RPC**](rpc-auth-identity-handle.md). Si tratta di un tipo flessibile che rappresenta un puntatore a una struttura di dati. Il contenuto della struttura dei dati può variare a seconda del servizio di autenticazione. Attualmente, i SSP supportati da RPC richiedono che l'applicazione imposti l' **\_ handle di \_ identità \_ di autenticazione RPC** in modo che punti a una struttura di [**\_ \_ \_ identità di autenticazione WinNT sec**](/windows/desktop/api/Rpcdce/ns-rpcdce-sec_winnt_auth_identity_a) . La struttura di **\_ \_ \_ identità di autenticazione WinNT sec** contiene i campi relativi a nome utente, dominio e password.

 

 




