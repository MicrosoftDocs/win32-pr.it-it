---
title: Configurazione delle DLL di estensione
description: All'avvio, Server dei criteri di rete controlla il Registro di sistema per un elenco di DLL di terze parti da chiamare.
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737d53bd25a28321c333e890a019af881ae54fa1c5ae92299b1776689f9abb74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962511"
---
# <a name="setting-up-the-extension-dlls"></a>Configurazione delle DLL di estensione

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete (NPS) a partire Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a Server dei criteri di rete. In tutto il testo, Server dei criteri di rete viene usato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente indicate come IAS.

 

All'avvio, Server dei criteri di rete controlla il Registro di sistema per un elenco di DLL di terze parti da chiamare.

Per configurare una DLL di autenticazione o autorizzazione in un server dei criteri di rete, elencare i percorsi delle DLL nei valori sotto la chiave del Registro di sistema seguente:

**Parametri \\ \\ \\ \\ AuthSrv del sistema HKLM CurrentControlSet Services \\\\**

Se le **chiavi AuthSrv** **e Parameters** non esistono, crearle.

Il valore in cui elencare le DLL dell'estensione di autenticazione è:

**Istruzioni ExtensionDLLs**

Il valore in cui elencare le DLL dell'estensione di autorizzazione è:

**AuthorizationDLLs**

Entrambi i **valori ExtensionDLLs** **e AuthorizationDLLs** devono essere di tipo **REG MULTI \_ \_ SZ.** Questo tipo consente di elencare più DLL.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Richiamo delle DLL di estensione](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[Attributi di identificazione utente](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 