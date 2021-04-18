---
title: API di scripting WinRM
description: Gestione remota Windows gli oggetti di scripting sono implementati come livello superiore al protocollo di WS-Management.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7910213487f525b74c3d1a8819a450f95336aba1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298613"
---
# <a name="winrm-scripting-api"></a>API di scripting WinRM

Gestione remota Windows gli oggetti di scripting sono implementati come livello superiore al [protocollo WS-Management](ws-management-protocol.md). Gli oggetti di scripting consentono di ottenere dati o gestire [*risorse*](windows-remote-management-glossary.md) in computer locali e remoti.

## <a name="ws-management-objects"></a>Oggetti WS-Management

Ogni oggetto di scripting dispone di un'interfaccia C++ corrispondente. Per ulteriori informazioni, vedere l' [API C++ WinRM](winrm-c---api.md) e [scripting in gestione remota Windows](scripting-in-windows-remote-management.md).

Gli oggetti seguenti vengono forniti dall'API di scripting di WinRM.

<dl> <dt>

<span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)
</dt> <dd>

Definisce il nome utente e la password utilizzati per le connessioni remote. Il nome utente e la password vengono passati quando si chiama il metodo [**CreateConnectionOptions**](wsman-createconnectionoptions.md) . Per ulteriori informazioni, vedere [recupero di dati da un computer remoto](obtaining-data-from-a-remote-computer.md). L'interfaccia C++ corrispondente è [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).

</dd> <dt>

<span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumeratore**](enumerator.md)
</dt> <dd>

Rappresenta una raccolta di risultati restituiti dall'enumerazione di una risorsa. Per altre informazioni, vedere [enumerazione o elenco di tutte le istanze di una risorsa](enumerating-or-listing-all-instances-of-a-resource.md). L'interfaccia C++ corrispondente è [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).

</dd> <dt>

<span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)
</dt> <dd>

Fornisce il percorso di una risorsa. È possibile usare un oggetto [**resourceLocator**](resourcelocator.md) anziché un [*URI di risorsa*](windows-remote-management-glossary.md) nelle operazioni dell'oggetto [**sessione**](session.md) , ad esempio [**Session. Get**](session-get.md), [**Session. Put**](session-put.md)o [**Session. enumerate**](session-enumerate.md). L'interfaccia C++ corrispondente è [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Sessione**](session.md)
</dt> <dd>

Definisce le operazioni di rete e le proprietà disponibili per la sessione, ad esempio [**Session. Get**](session-get.md), [**Session. enumerate**](session-enumerate.md), [**Session. Invoke**](session-invoke.md). Per ulteriori informazioni, vedere [recupero di dati dal computer locale](obtaining-data-from-the-local-computer.md). L'interfaccia C++ corrispondente è [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).

</dd> <dt>

<span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)
</dt> <dd>

Fornisce metodi e proprietà utilizzati per creare una nuova sessione o gestire una sessione stabilita. Per ulteriori informazioni, vedere [utilizzo di gestione remota Windows](using-windows-remote-management.md). Le interfacce C++ corrispondenti sono [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) e [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Gestione remota Windows](about-windows-remote-management.md)
</dt> <dt>

[Utilizzo di Gestione remota Windows](using-windows-remote-management.md)
</dt> <dt>

[Creazione di script in Gestione remota Windows](scripting-in-windows-remote-management.md)
</dt> <dt>

[Riferimento Gestione remota Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 




