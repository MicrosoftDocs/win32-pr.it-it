---
description: Autenticazione origine rete
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: Autenticazione origine rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09c38968fccf501f49ac7666a066b88528b237bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049661"
---
# <a name="network-source-authentication"></a>Autenticazione origine rete

Alcuni host multimediali potrebbero richiedere credenziali utente dalle applicazioni client prima di consentire l'accesso al supporto. Le credenziali utente includono l'identificazione e la prova dell'identificazione, ad esempio nome utente e password, che vengono usate dal server multimediale per concedere l'accesso all'origine di rete ospitata. L'origine di rete può fornire l'autenticazione NTLM, digest o di base.

Le applicazioni basate su Media Foundation possono archiviare le credenziali utente per un URL specifico in un oggetto *credenziale* che espone l'interfaccia [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) . L'oggetto Credential archivia le credenziali crittografate e fornisce i metodi per restituire informazioni come nome utente, password e dominio.

Gli oggetti credenziale vengono creati e gestiti in una cache. L'oggetto della *cache delle credenziali* , esposto dall'interfaccia [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) , fornisce metodi per il recupero degli oggetti Credential dalla cache delle credenziali.

Un'applicazione che supporta l'autenticazione deve implementare l'interfaccia [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) . Media Foundation non fornisce un'implementazione predefinita di questa interfaccia. Gestione credenziali è responsabile della raccolta delle credenziali necessarie per un URL dall'input dell'utente o della lettura da un archivio permanente.

Questa sezione contiene i seguenti argomenti:

-   [Impostazione di una gestione credenziali](setting-a-credential-manager.md)
-   [Uso della cache delle credenziali](using-the-credential-cache.md)
-   [Implementazione di IMFNetCredentialManager](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



