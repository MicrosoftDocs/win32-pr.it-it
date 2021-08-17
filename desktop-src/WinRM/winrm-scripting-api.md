---
title: WinRM Scripting API
description: Windows Gli oggetti di scripting di Gestione remota vengono implementati come un livello sopra WS-Management protocollo.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c7ce6311fe80884ab0c71e66360a2072381221b5b85a8626fda0e0104168b4f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742759"
---
# <a name="winrm-scripting-api"></a>WinRM Scripting API

Windows Gli oggetti di scripting di Gestione remota vengono implementati come livello sopra [protocollo WS-Management](ws-management-protocol.md). Gli oggetti di scripting consentono di ottenere dati o gestire [*risorse*](windows-remote-management-glossary.md) in computer locali e remoti.

## <a name="ws-management-objects"></a>oggetti WS-Management

Ogni oggetto di scripting ha un'interfaccia C++ corrispondente. Per altre informazioni, vedere [API C++ WinRM](winrm-c---api.md) e [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).

Gli oggetti seguenti vengono forniti dall'API di scripting WinRM.

<dl> <dt>

<span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**Connectionoptions**](connectionoptions.md)
</dt> <dd>

Definisce il nome utente e la password utilizzati per le connessioni remote. Il nome utente e la password vengono passati quando si chiama [**il metodo CreateConnectionOptions.**](wsman-createconnectionoptions.md) Per altre informazioni, vedere [Recupero di dati da un computer remoto.](obtaining-data-from-a-remote-computer.md) L'interfaccia C++ corrispondente è [**IWSManConnectionOptions.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)

</dd> <dt>

<span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumeratore**](enumerator.md)
</dt> <dd>

Rappresenta una raccolta di risultati restituiti dall'enumerazione di una risorsa. Per altre informazioni, vedere [Enumerazione o elenco di tutte le istanze di una risorsa.](enumerating-or-listing-all-instances-of-a-resource.md) L'interfaccia C++ corrispondente è [**IWSManEnumerator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)

</dd> <dt>

<span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)
</dt> <dd>

Specifica il percorso di una risorsa. È possibile usare un [**oggetto ResourceLocator**](resourcelocator.md) anziché un [*URI*](windows-remote-management-glossary.md) di risorsa nelle operazioni sull'oggetto [**Session,**](session.md) ad esempio [**Session.Get,**](session-get.md) [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md) L'interfaccia C++ corrispondente è [**IWSManResourceLocator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Sessione**](session.md)
</dt> <dd>

Definisce le operazioni di rete e le proprietà disponibili per la sessione, ad esempio [**Session.Get**](session-get.md), [**Session.Enumerate**](session-enumerate.md), [**Session.Invoke**](session-invoke.md). Per altre informazioni, vedere [Recupero di dati dal computer locale.](obtaining-data-from-the-local-computer.md) L'interfaccia C++ corrispondente è [**IWSManSession.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)

</dd> <dt>

<span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)
</dt> <dd>

Fornisce metodi e proprietà utilizzati per creare una nuova sessione o gestire una sessione stabilita. Per altre informazioni, vedere [Using Windows Remote Management](using-windows-remote-management.md). Le interfacce C++ corrispondenti sono [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) e [**IWSManEx.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni Windows gestione remota](about-windows-remote-management.md)
</dt> <dt>

[Uso Windows gestione remota](using-windows-remote-management.md)
</dt> <dt>

[Esecuzione di script Windows gestione remota](scripting-in-windows-remote-management.md)
</dt> <dt>

[Windows Informazioni di riferimento sulla gestione remota](windows-remote-management-reference.md)
</dt> </dl>

 

 




