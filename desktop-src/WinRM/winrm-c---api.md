---
title: WinRM C++ API
description: È Windows le interfacce di gestione remota per ottenere dati o gestire le risorse in un computer remoto. Questa API è destinata principalmente all'uso interno. Quando possibile, è consigliabile usare l'API della shell client WinRM.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c6039dde1884f2b4b7aa9801fbbd26bb0e10b9a5353dffb5096ba66461d1d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742947"
---
# <a name="winrm-c-api"></a>WinRM C++ API

Il Windows interfacce di gestione remota può essere utilizzato per ottenere dati o gestire [*le risorse*](windows-remote-management-glossary.md) in un computer remoto. Questa API è destinata principalmente all'uso interno. Quando possibile, è [consigliabile usare l'API della shell client WinRM.](client-shell-api.md) Le interfacce corrispondono strettamente [all'API di scripting WinRM](winrm-scripting-api.md).

Le interfacce WinRM che ereditano direttamente da **IDispatch** hanno ognuna un oggetto di scripting corrispondente. Per altre informazioni, vedere [l'API di scripting WinRM.](winrm-scripting-api.md)

Per le applicazioni multithreading, WinRM non supporta thread separati che accedono allo [**stesso oggetto IWSMAN.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)

Le interfacce seguenti sono fornite da WinRM.

<dl> <dt>

<span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Fornisce metodi e proprietà utilizzati per creare una nuova sessione e gestire una sessione stabilita. [**WSMan è**](wsman.md) l'oggetto di scripting corrispondente.

</dd> <dt>

<span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Fornisce metodi e proprietà usati per creare un nuovo [**oggetto IWSManResourceLocator.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) Questo metodo è disponibile per l'oggetto di scripting [**WSMan.**](wsman.md)

</dd> <dt>

<span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)
</dt> <dd>

Definisce il nome utente e la password utilizzati per le connessioni remote. [**ConnectionOptions è**](connectionoptions.md) l'oggetto di scripting corrispondente.

</dd> <dt>

<span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> <dd>

Definisce le operazioni e le proprietà di rete disponibili per la sessione. [**Session**](session.md) è l'oggetto di scripting corrispondente.

</dd> <dt>

<span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)
</dt> <dd>

Rappresenta una raccolta di risultati restituiti dall'enumerazione di una risorsa. [**Enumeratore**](enumerator.md) è l'oggetto di scripting corrispondente.

</dd> <dt>

<span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)
</dt> <dd>

Specifica il percorso di una risorsa. È possibile usare un [**oggetto IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) invece di un [*URI di risorsa*](windows-remote-management-glossary.md) nelle operazioni [**dell'oggetto**](session.md) Sessione. [**ResourceLocator è**](resourcelocator.md) l'oggetto di scripting corrispondente.

</dd> </dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Informazioni di riferimento sulla gestione remota](windows-remote-management-reference.md)
</dt> </dl>

 

 




