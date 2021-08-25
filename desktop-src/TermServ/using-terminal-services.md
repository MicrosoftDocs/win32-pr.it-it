---
title: Uso di Servizi Desktop remoto
description: Come programmare nell'ambiente Servizi Desktop remoto e come estendere la tecnologia Servizi Desktop remoto (in precedenza nota come Servizi terminal) al Web usando Connessione Web Desktop remoto.
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto , usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d0af90aef8eed3c8b9dc397f86cb6940a79e8e399af201ff854cbfaba3ff3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868771"
---
# <a name="using-remote-desktop-services"></a>Uso di Servizi Desktop remoto

Le sezioni seguenti descrivono come programmare nell'ambiente Servizi Desktop remoto e come estendere la tecnologia Servizi Desktop remoto (in precedenza nota come Servizi terminal) al Web usando Connessione Web Desktop remoto. Se si cercano informazioni utente per le connessioni Desktop remoto, vedere Connessione [a un altro computer usando Connessione Desktop remoto](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).

> [!Note]  
> Questo argomento è per sviluppatori di software.

 

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Rilevamento dell'installazione del Servizi Desktop remoto di configurazione](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

Esempio di codice C# che mostra un metodo che restituisce **True** se il ruolo del server Servizi Desktop remoto è installato e in esecuzione o **false** in caso contrario, a partire da Windows Server 2008.

</dd> <dt>

[Estensione di Gestore di sessione di Servizi terminal](extending-ts-session-broker.md)
</dt> <dd>

È possibile estendere TS Session Broker usando [**l'interfaccia COM IWTSSBPlugin.**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)

</dd> <dt>

[Implementazione di un enumeratore di endpoint audio personalizzato](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

A partire da Windows Server 2008 R2, è possibile implementare un enumeratore di endpoint audio remoto personalizzato come parte di un provider Desktop remoto protocol.

</dd> <dt>

[Moniker di sessione](session-monikers.md)
</dt> <dd>

Distributed COM (DCOM) consente l'attivazione degli oggetti per sessione tramite un moniker di sessione fornito dal sistema.

</dd> <dt>

[Uso dell'estensione ADSI per Servizi Desktop remoto utente](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

L'amministrazione di proprietà utente specifiche di Servizi Desktop remoto è possibile usando i metodi implementati dall'estensione ADSI (Active Directory Service Interfaces), in pacchetto con la libreria a collegamento dinamico Tsuserex.dll.

</dd> <dt>

[Uso dell'API Servizi Desktop remoto](using-the-terminal-services-api.md)
</dt> <dd>

Viene descritto come usare l'API Servizi Desktop remoto per consentire alle applicazioni di eseguire attività in un Servizi Desktop remoto locale.

</dd> <dt>

[Uso dell'API Desktop remoto Virtualization](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

Gli sviluppatori possono usare questa API per personalizzare la logica utilizzata da Connessione Desktop remoto Broker (Gestore connessione Desktop remoto) per determinare la destinazione migliore per una connessione client in ingresso.

</dd> <dt>

[Interfaccia WSDL per soluzioni VDI personalizzate](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

Gli sviluppatori possono creare servizi Web personalizzati che gestiscono soluzioni VDI (Virtual Desktop Infrastructure).

</dd> </dl>

Per altre informazioni, vedere linee [guida per Servizi Desktop remoto di programmazione.](terminal-services-programming-guidelines.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi terminal è ora disponibile Servizi Desktop remoto](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[Rilevamento dell'Servizi Desktop remoto locale](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 




