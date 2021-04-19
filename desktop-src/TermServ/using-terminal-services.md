---
title: Utilizzo di Servizi Desktop remoto
description: Come programmare nell'ambiente Servizi Desktop remoto e come estendere la tecnologia di Servizi Desktop remoto (precedentemente nota come servizi Terminal) al Web utilizzando Connessione Web Desktop remoto.
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto utilizzando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac575a89d1ae8c7c065199aca136f2f0e5fc7459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298337"
---
# <a name="using-remote-desktop-services"></a>Utilizzo di Servizi Desktop remoto

Nelle sezioni seguenti viene descritto come programmare nell'ambiente Servizi Desktop remoto e come estendere la tecnologia di Servizi Desktop remoto (precedentemente nota come servizi Terminal) al Web utilizzando Connessione Web Desktop remoto. Per informazioni sull'utente per le connessioni Desktop remoto, vedere [connettersi a un altro computer usando connessione Desktop remoto](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).

> [!Note]  
> Questo argomento è per gli sviluppatori di software.

 

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Rilevamento dell'installazione del ruolo Servizi Desktop remoto](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

Esempio di codice C# che mostra un metodo che restituisce **true** se il ruolo del server Servizi Desktop remoto è installato e in esecuzione o **false** in caso contrario, a partire da Windows Server 2008.

</dd> <dt>

[Estensione di broker di sessione di Servizi terminal](extending-ts-session-broker.md)
</dt> <dd>

È possibile estendere broker di sessione di Servizi terminal tramite l'interfaccia com [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) .

</dd> <dt>

[Implementazione di un enumeratore di endpoint audio personalizzato](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

A partire da Windows Server 2008 R2, è possibile implementare un enumeratore endpoint audio remoto personalizzato come parte di un provider di protocollo Desktop remoto.

</dd> <dt>

[Moniker della sessione](session-monikers.md)
</dt> <dd>

Distributed COM (DCOM) consente l'attivazione di oggetti in base a ogni sessione usando un moniker di sessione fornito dal sistema.

</dd> <dt>

[Uso dell'estensione ADSI per la configurazione di Servizi Desktop remoto utente](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

L'amministrazione delle proprietà utente specifiche di Servizi Desktop remoto è possibile utilizzando i metodi implementati dall'estensione ADSI (Active Directory Service Interfaces), assemblata con la libreria a collegamento dinamico Tsuserex.dll.

</dd> <dt>

[Uso dell'API Servizi Desktop remoto](using-the-terminal-services-api.md)
</dt> <dd>

Viene descritto come utilizzare l'API Servizi Desktop remoto per consentire alle applicazioni di eseguire attività in un ambiente Servizi Desktop remoto.

</dd> <dt>

[Uso dell'API di virtualizzazione Desktop remoto](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

Gli sviluppatori possono utilizzare questa API per personalizzare la logica utilizzata da Connessione Desktop remoto broker di connessione Desktop remoto per determinare la destinazione migliore per una connessione client in ingresso.

</dd> <dt>

[Interfaccia WSDL per soluzioni VDI personalizzate](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

Gli sviluppatori possono creare servizi Web personalizzati che gestiscono soluzioni VDI (Virtual Desktop Infrastructure).

</dd> </dl>

Per ulteriori informazioni, vedere [Servizi Desktop remoto linee guida](terminal-services-programming-guidelines.md)per la programmazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi terminal è ora Servizi Desktop remoto](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[Rilevamento dell'ambiente Servizi Desktop remoto](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 




