---
title: Uso della sicurezza a livello di trasporto nel server
description: Uso della sicurezza a livello di trasporto nel server con RPC (Remote Procedure Call).
ms.assetid: 8ad86d46-cdc8-44f0-bb56-4d5069f33e64
keywords:
- Chiamata di procedura remota RPC, attività, uso della sicurezza a livello di trasporto nel server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abd1f072f249336f4804aed56fb1122556596c43286383b763839d988a2406b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010589"
---
# <a name="using-transport-level-security-on-the-server"></a>Uso della sicurezza a livello di trasporto nel server

Questa sezione presenta le discussioni sulla sicurezza a livello di trasporto, suddivise negli argomenti seguenti:

-   [Uso Transport-Level sicurezza nel client](using-transport-level-security-on-the-client.md)

Quando si usa [ncacn \_ np](/windows/desktop/Midl/ncacn-np) o [ncalrpc](/windows/desktop/Midl/ncalrpc) come sequenza di protocollo, il server specifica un descrittore di sicurezza per l'endpoint nel momento in cui seleziona la sequenza di protocollo. Per altre informazioni sulle sequenze di protocollo, vedere [Specifica delle sequenze di protocollo](specifying-protocol-sequences.md). L'applicazione fornisce il descrittore di sicurezza come parametro aggiuntivo (estensione ai parametri OSF-DCE standard) in tutte le funzioni che iniziano con i prefissi [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) e [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs). Il descrittore di sicurezza controlla se un client può connettersi all'endpoint.

Ogni processo e thread è associato a un token di sicurezza. Questo token include un descrittore di sicurezza predefinito usato per tutti gli oggetti creati dal processo, ad esempio l'endpoint. Se l'applicazione non specifica un descrittore di sicurezza quando si chiama una funzione con i [**prefissi RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) e [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), la libreria di runtime RPC applica il descrittore di sicurezza predefinito dal token di sicurezza del processo all'endpoint.

Per garantire che l'applicazione server sia accessibile a tutti i client, l'amministratore deve avviare l'applicazione server in un processo con un descrittore di sicurezza predefinito che tutti i client possono usare. In genere, solo i processi di sistema hanno un descrittore di sicurezza predefinito.

Per altre informazioni su queste funzioni e sulle funzioni [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) e [**RpcRevertToSelf.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself)

 

 