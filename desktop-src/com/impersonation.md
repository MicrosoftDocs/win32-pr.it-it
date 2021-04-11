---
title: Rappresentazione
description: La rappresentazione è la capacità di esecuzione di un thread in un contesto di sicurezza diverso dal contesto del processo a cui appartiene il thread.
ms.assetid: b33ca3b0-0423-4338-b3d6-4bb3db3d3e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a735fa12e175ecec5dc2a7ed741843d713532e19
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047437"
---
# <a name="impersonation"></a>Rappresentazione

La rappresentazione è la capacità di esecuzione di un thread in un contesto di sicurezza diverso dal contesto del processo a cui appartiene il thread. Quando viene eseguito nel contesto di sicurezza del client, il server "è" il client, a un certo livello. Il thread del server utilizza un token di accesso che rappresenta le credenziali del client per ottenere l'accesso agli oggetti a cui il client ha accesso.

Il motivo principale per la rappresentazione consiste nel causare l'esecuzione dei controlli di accesso con l'identità del client. L'uso dell'identità del client per i controlli di accesso può causare restrizioni o espansione dell'accesso, a seconda di ciò che il client è autorizzato a eseguire. Si supponga, ad esempio, che in un file server siano presenti file contenenti informazioni riservate e che ognuno di questi file sia protetto da un ACL. Per impedire a un client di ottenere accesso non autorizzato alle informazioni contenute in questi file, il server può rappresentare il client prima di accedere ai file.

## <a name="access-tokens-for-impersonation"></a>Token di accesso per la rappresentazione

I token di accesso sono oggetti che descrivono il contesto di sicurezza di un processo o di un thread. Forniscono informazioni che includono l'identità di un account utente e un subset dei privilegi disponibili per l'account utente. Ogni processo dispone di un *token di accesso primario* che descrive il contesto di sicurezza dell'account utente associato al processo. Per impostazione predefinita, il sistema usa il token primario quando un thread del processo interagisce con un oggetto a protezione diretta. Tuttavia, quando un thread rappresenta un client, il thread di rappresentazione include sia un token di accesso primario che un *token* di rappresentazione. Il token di rappresentazione rappresenta il contesto di sicurezza del client e questo token di accesso è quello usato per i controlli di accesso durante la rappresentazione. Quando la rappresentazione è finita, il thread viene ripristinato utilizzando solo il token di accesso primario.

È possibile usare la funzione [**OpenProcessToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) per ottenere un handle per il token primario di un processo. Utilizzare la funzione [**OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) per ottenere un handle per il token di rappresentazione di un thread.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Token di accesso](/windows/desktop/SecAuthZ/access-tokens)
</dt> <dt>

[Delega e rappresentazione](delegation-and-impersonation.md)
</dt> </dl>

 

 