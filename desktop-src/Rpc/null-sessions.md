---
title: Sessioni null
description: A volte una chiamata in arrivo nella sessione null può apparire come una chiamata autenticata.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68fe0542d86dd2e6b903a08834293d6cc2f09828
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471659"
---
# <a name="null-sessions"></a>Sessioni null

A volte una chiamata in arrivo nella sessione null può apparire come una chiamata autenticata. In particolare, la chiamata della funzione [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) restituisce il livello di autenticazione e il provider di sicurezza utilizzati per la chiamata. Questa operazione non significa che la chiamata non si trovava in una sessione null. I due problemi sono ortogonali. In Microsoft Windows 2000 una chiamata di procedura remota può tentare di rappresentare un chiamante e controllare le autorizzazioni dopo la rappresentazione. In Microsoft Windows XP è più veloce chiamare la funzione [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) e verificare la presenza del flag **NullSession** .

Esiste un'altra differenza rilevante tra Windows 2000 e Windows XP. Se \_ viene specificato solo il flag RPC if \_ allow \_ \_ solo Secure, le chiamate sulla sessione null passano attraverso in Windows 2000. In Windows XP, con la stretta generale delle impostazioni di sicurezza predefinite, quando si specifica questo flag, le chiamate della sessione null vengono rifiutate con accesso negato. Tuttavia, anche con il \_ flag RPC \_ if \_ allow \_ solo Secure, RPC non garantisce il livello di privilegio dell'utente chiamante. Tutti i controlli RPC sono che l'utente dispone di credenziali valide. È possibile che l'utente chiamante stia utilizzando l'account Guest o altri account con privilegi limitati. Verificare che il server non assuma privilegi elevati una volta \_ RPC \_ se \_ \_ si usa Consenti solo sicurezza.

 

 




