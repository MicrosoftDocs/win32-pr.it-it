---
description: Autenticazione dell'origine di rete
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: Autenticazione dell'origine di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3e90ae7d7a8e4fb29b56aaa1296ba0c5aa44049f801b01a2c7797009ec736aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973040"
---
# <a name="network-source-authentication"></a>Autenticazione dell'origine di rete

Alcuni host multimediali possono richiedere le credenziali utente dalle applicazioni client prima di consentire l'accesso ai supporti. Le credenziali utente includono l'identificazione e la prova di identificazione, ad esempio il nome utente e la password, usati dal server multimediale per concedere l'accesso all'origine di rete ospitata. L'origine di rete può fornire l'autenticazione NTLM, Digest o Basic.

Le applicazioni basate Media Foundation possono archiviare le credenziali utente per un URL specifico in un oggetto *credenziale* che espone [**l'interfaccia IMFNetCredential.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) L'oggetto credenziale archivia le credenziali crittografate e fornisce metodi per restituire informazioni quali nome utente, password e dominio.

Gli oggetti credenziale vengono creati e gestiti in una cache. *L'oggetto cache* delle credenziali, esposto dall'interfaccia [**IMFNetCredentialCache,**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) fornisce metodi per recuperare gli oggetti credenziali dalla cache delle credenziali.

Un'applicazione che supporta l'autenticazione deve implementare [**l'interfaccia IMFNetCredentialManager.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) Media Foundation non fornisce un'implementazione predefinita di questa interfaccia. Il gestore delle credenziali è responsabile della raccolta delle credenziali necessarie per un URL dall'input dell'utente o dalla lettura dall'archiviazione persistente.

Questa sezione contiene i seguenti argomenti:

-   [Impostazione di un Gestione credenziali](setting-a-credential-manager.md)
-   [Uso della cache delle credenziali](using-the-credential-cache.md)
-   [Implementazione di IMFNetCredentialManager](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



