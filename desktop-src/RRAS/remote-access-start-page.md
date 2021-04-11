---
title: Accesso remoto
description: Usare il servizio di accesso remoto (RAS) per creare applicazioni client.
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- RAS del servizio di accesso remoto
- RAS RAS
- RAS del servizio di accesso remoto, pagina iniziale
- Ras RAS, vedere Accesso remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95a4b1c06656b51395c8c4fc666e59d6115bd839
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104117407"
---
# <a name="remote-access"></a>Accesso remoto

## <a name="purpose"></a>Scopo

Usare il servizio di accesso remoto (RAS) per creare applicazioni client. Queste applicazioni visualizzano finestre di dialogo comuni RAS, gestiscono le connessioni e i dispositivi di accesso remoto e modificano le voci del libro telefonico. RAS fornisce inoltre la nuova generazione di funzionalità server per il servizio di accesso remoto (RAS) per Windows. La funzionalità del server RRAS segue e si basa sul servizio di accesso remoto (RAS).

## <a name="where-applicable"></a>Se applicabile

Il servizio di accesso remoto è applicabile in qualsiasi ambiente informatico che usa un collegamento WAN (Wide Area Network) o una rete privata virtuale (VPN). RAS rende possibile la connessione di un computer client remoto a un server di rete tramite un collegamento WAN o una VPN. Il computer remoto funge quindi da rete LAN del server come se il computer remoto fosse connesso direttamente alla LAN. L'API RAS consente ai programmatori di accedere alle funzionalità di RAS a livello di codice.

## <a name="developer-audience"></a>Sviluppatori

L'API RAS è progettata per l'uso da parte dei programmatori C/C++. I programmatori Microsoft Visual Basic possono anche trovare l'API utile. I programmatori devono acquisire familiarità con i concetti di rete.

## <a name="run-time-requirements"></a>Requisiti di runtime

Alcune funzioni nell'API RAS sono supportate solo nei server di rete e altre funzioni sono supportate solo sui client di rete. Per informazioni più specifiche sui sistemi operativi che supportano una particolare funzione, vedere le sezioni requisiti nella documentazione.

La [funzionalità RAS avanzata](function-comparison-windows-2000-versus-rras-redistributable.md) di RRAS è disponibile per Windows NT Server 4,0 installando [RRAS Redistributable](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp). Tutte le funzionalità di RRAS sono incorporate in Windows 2000 Server, Windows Server 2003 e Windows Server 2008. Le applicazioni RRAS non possono essere eseguite su workstation Windows NT 4,0 o sui sistemi operativi client, ad esempio Windows 95. Per informazioni più specifiche sui sistemi operativi che supportano una particolare funzione, vedere le sezioni requisiti nella documentazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                             | Descrizione                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Servizio di accesso remoto](about-remote-access-service.md)<br/>                               | Il servizio di accesso remoto (RAS) fornisce funzionalità di accesso remoto alle applicazioni client nei computer che eseguono Windows.<br/>                                                                                          |
| [Amministrazione del servizio di accesso remoto](about-remote-access-service-administration.md)<br/> | Amministrazione servizio di accesso remoto fornisce un set di funzioni per l'amministrazione delle autorizzazioni e delle porte utente nei server RAS. Utilizzando queste funzioni, è possibile sviluppare un'applicazione di amministrazione del server RAS.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Routing](routing-start-page.md)
</dt> <dt>

[Protocolli di routing](routing-protocols-start-page.md)
</dt> </dl>

 

 





