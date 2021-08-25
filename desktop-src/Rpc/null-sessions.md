---
title: Sessioni Null
description: A volte una chiamata in arrivo nella sessione Null può apparire come una chiamata autenticata.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5476a49513019fe15afa4a30beae08104533a6621a84c4e0d1de4e9f315275ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019561"
---
# <a name="null-sessions"></a>Sessioni Null

A volte una chiamata in arrivo nella sessione Null può apparire come una chiamata autenticata. In particolare, la chiamata [**alla funzione RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) restituisce il livello di autenticazione e il provider di sicurezza usati per la chiamata. Questa operazione non significa che la chiamata non fosse in una sessione Null. I due problemi sono ortogonali. In Microsoft Windows 2000, una chiamata di procedura remota può tentare di rappresentare un chiamante e controllare le autorizzazioni dopo la rappresentazione. In Microsoft Windows XP è più veloce chiamare la [**funzione RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) e verificare la presenza del flag **NullSession.**

Esiste un'altra differenza pertinente tra Windows 2000 e Windows XP. Se viene specificato solo il flag RPC IF ALLOW SECURE ONLY, le chiamate alla sessione Null vengono effettuate \_ \_ Windows \_ \_ 2000. In Windows XP, con la stretta generale delle impostazioni di sicurezza predefinite, quando viene specificato questo flag, le chiamate sulla sessione Null vengono rifiutate con accesso negato. Tuttavia, anche con il flag RPC IF ALLOW SECURE ONLY, RPC non garantisce il \_ \_ livello di \_ \_ privilegio dell'utente chiamante. Tutti i controlli RPC verificano che l'utente abbia credenziali valide. È possibile che l'utente chiamante utilizzi l'account guest o altri account con privilegi bassi. Assicurarsi che il server non presupponga privilegi elevati dopo l'uso di RPC \_ IF \_ ALLOW SECURE \_ \_ ONLY.

 

 




