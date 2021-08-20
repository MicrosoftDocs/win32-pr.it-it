---
title: Rappresentazione
description: La rappresentazione è la capacità di un thread di essere eseguita in un contesto di sicurezza diverso dal contesto del processo proprietario del thread.
ms.assetid: b33ca3b0-0423-4338-b3d6-4bb3db3d3e1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67654c3a894a985f5f3da7c25e2c2a2f095787fa659233d450165ccbdd5217c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919243"
---
# <a name="impersonation"></a>Rappresentazione

La rappresentazione è la capacità di un thread di essere eseguita in un contesto di sicurezza diverso dal contesto del processo proprietario del thread. Durante l'esecuzione nel contesto di sicurezza del client, il server "è" il client, in una certa misura. Il thread del server usa un token di accesso che rappresenta le credenziali del client per ottenere l'accesso agli oggetti a cui il client ha accesso.

Il motivo principale della rappresentazione è l'esecuzione di controlli di accesso sull'identità del client. L'uso dell'identità del client per i controlli di accesso può determinare la limitazione o l'espansione dell'accesso, a seconda di ciò che il client ha l'autorizzazione per eseguire. Si supponga, ad esempio, file server file contenenti informazioni riservate e che ognuno di questi file sia protetto da un ACL. Per impedire a un client di ottenere l'accesso non autorizzato alle informazioni contenute in questi file, il server può rappresentare il client prima di accedere ai file.

## <a name="access-tokens-for-impersonation"></a>Token di accesso per la rappresentazione

I token di accesso sono oggetti che descrivono il contesto di sicurezza di un processo o di un thread. Forniscono informazioni che includono l'identità di un account utente e un subset dei privilegi disponibili per l'account utente. Ogni processo ha un *token di accesso* primario che descrive il contesto di sicurezza dell'account utente associato al processo. Per impostazione predefinita, il sistema usa il token primario quando un thread del processo interagisce con un oggetto a protezione diretta. Tuttavia, quando un thread rappresenta un client, il thread di rappresentazione dispone sia di un token di accesso primario che di *un token di rappresentazione.* Il token di rappresentazione rappresenta il contesto di sicurezza del client e questo token di accesso è quello utilizzato per i controlli di accesso durante la rappresentazione. Al termine della rappresentazione, il thread torna a usare solo il token di accesso primario.

È possibile usare la [**funzione OpenProcessToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) per ottenere un handle per il token primario di un processo. Usare la [**funzione OpenThreadToken**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) per ottenere un handle al token di rappresentazione di un thread.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Token di accesso](/windows/desktop/SecAuthZ/access-tokens)
</dt> <dt>

[Delega e rappresentazione](delegation-and-impersonation.md)
</dt> </dl>

 

 