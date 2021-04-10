---
title: Impostazione delle DLL di estensione
description: All'avvio, NPS controlla il registro di sistema per un elenco di dll di terze parti da chiamare.
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14e8589f31144f12b120f9a77f281dd57a9f30ce
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047063"
---
# <a name="setting-up-the-extension-dlls"></a>Impostazione delle DLL di estensione

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a NPS. In tutto il testo, NPS viene utilizzato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

All'avvio, NPS controlla il registro di sistema per un elenco di dll di terze parti da chiamare.

Per impostare una DLL di autenticazione o autorizzazione in un server NPS, elencare i percorsi delle dll nei valori sotto la seguente chiave del registro di sistema:

**\\ \\ \\ Parametri AuthSrv dei servizi \\ CurrentControlSet \\ di sistema HKLM\\**

Se le chiavi **AuthSrv** e **Parameters** non esistono, crearle.

Il valore in cui elencare le DLL dell'estensione di autenticazione è:

**ExtensionDLLs**

Il valore in cui elencare le DLL dell'estensione di autorizzazione è:

**AuthorizationDLLs**

Entrambi i valori **ExtensionDLLs** e **AuthorizationDLLs** devono essere di tipo **reg \_ \_ multisz**. Questo tipo consente di elencare più dll.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiamo delle DLL di estensione](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[Attributi di identificazione utente](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 