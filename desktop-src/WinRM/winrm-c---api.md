---
title: API WinRM C++
description: Le interfacce Gestione remota Windows possono essere utilizzate per ottenere i dati o gestire le risorse in un computer remoto. Questa API è destinata principalmente all'uso interno. Quando possibile, è consigliabile usare l'API della shell client WinRM.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7cff2334d9839936d15f7258a70ce03f9751e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955628"
---
# <a name="winrm-c-api"></a>API WinRM C++

Le interfacce Gestione remota Windows possono essere utilizzate per ottenere i dati o gestire [*le risorse*](windows-remote-management-glossary.md) in un computer remoto. Questa API è destinata principalmente all'uso interno. Quando possibile, è consigliabile usare l' [API della shell client WinRM](client-shell-api.md) . Le interfacce corrispondono strettamente all' [API di scripting WinRM](winrm-scripting-api.md).

Le interfacce WinRM che ereditano direttamente da **IDispatch** hanno un oggetto di scripting corrispondente. Per ulteriori informazioni, vedere l' [API di scripting WinRM](winrm-scripting-api.md).

Per le applicazioni multithread, WinRM non supporta thread distinti che accedono allo stesso oggetto [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) .

Le interfacce seguenti sono fornite da WinRM.

<dl> <dt>

<span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Fornisce metodi e proprietà utilizzati per creare una nuova sessione e gestire una sessione stabilita. [**WSMan**](wsman.md) è l'oggetto di scripting corrispondente.

</dd> <dt>

<span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Fornisce metodi e proprietà utilizzati per creare un nuovo [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator). Questo metodo è disponibile per l'oggetto di scripting [**WSMan**](wsman.md) .

</dd> <dt>

<span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)
</dt> <dd>

Definisce il nome utente e la password utilizzati per le connessioni remote. [**ConnectionOptions**](connectionoptions.md) è l'oggetto di scripting corrispondente.

</dd> <dt>

<span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> <dd>

Definisce le operazioni di rete e le proprietà disponibili per la sessione. [**Session**](session.md) è l'oggetto di scripting corrispondente.

</dd> <dt>

<span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)
</dt> <dd>

Rappresenta una raccolta di risultati restituiti dall'enumerazione di una risorsa. [**Enumerator**](enumerator.md) è l'oggetto di scripting corrispondente.

</dd> <dt>

<span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)
</dt> <dd>

Fornisce il percorso di una risorsa. È possibile usare un oggetto [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) anziché un [*URI di risorsa*](windows-remote-management-glossary.md) nelle operazioni dell'oggetto [**Session**](session.md) . [**ResourceLocator**](resourcelocator.md) è l'oggetto di scripting corrispondente.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento Gestione remota Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 




