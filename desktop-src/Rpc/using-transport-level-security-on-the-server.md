---
title: Uso della sicurezza a livello di trasporto nel server
description: Utilizzo della sicurezza a livello di trasporto nel server con RPC (Remote Procedure Call).
ms.assetid: 8ad86d46-cdc8-44f0-bb56-4d5069f33e64
keywords:
- RPC (Remote Procedure Call), attività, uso della sicurezza a livello di trasporto nel server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39af5b8fb43a57683804eb7b91067ca9faad4390
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473411"
---
# <a name="using-transport-level-security-on-the-server"></a>Uso della sicurezza a livello di trasporto nel server

In questa sezione vengono illustrate le discussioni sulla sicurezza a livello di trasporto, divise negli argomenti seguenti:

-   [Utilizzo di Transport-Level sicurezza sul client](using-transport-level-security-on-the-client.md)

Quando si usa [ncacn \_ NP](/windows/desktop/Midl/ncacn-np) o [ncalrpc](/windows/desktop/Midl/ncalrpc) come sequenza di protocollo, il server specifica un descrittore di sicurezza per l'endpoint al momento della selezione della sequenza del protocollo. Per ulteriori informazioni sulle sequenze di protocollo, vedere [specifica delle sequenze di protocollo](specifying-protocol-sequences.md). L'applicazione fornisce il descrittore di sicurezza come parametro aggiuntivo (un'estensione ai parametri OSF-DCE standard) in tutte le funzioni che iniziano con i prefissi [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) e [**RpcServerUseAllProtSeqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs). Il descrittore di sicurezza controlla se un client può connettersi all'endpoint.

Ogni processo e thread è associato a un token di sicurezza. Questo token include un descrittore di sicurezza predefinito usato per tutti gli oggetti creati dal processo, ad esempio l'endpoint. Se l'applicazione non specifica un descrittore di sicurezza quando si chiama una funzione con i prefissi [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq) e [**RpcServerUseAllProtSeqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs), la libreria di runtime RPC applica il descrittore di sicurezza predefinito dal token di sicurezza del processo all'endpoint.

Per garantire che l'applicazione server sia accessibile a tutti i client, l'amministratore deve avviare l'applicazione server in un processo che dispone di un descrittore di sicurezza predefinito che tutti i client possono usare. In genere, solo i processi di sistema dispongono di un descrittore di sicurezza predefinito.

Per ulteriori informazioni su queste funzioni e sulle funzioni [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) e [**RpcRevertToSelf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcreverttoself).

 

 