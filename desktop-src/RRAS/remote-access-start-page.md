---
title: Accesso remoto
description: Usare il servizio di accesso remoto (RAS) per creare applicazioni client.
ms.assetid: 4e6c04d4-f989-4248-901f-ec15f61582da
keywords:
- Ras del servizio di accesso remoto
- RAS RAS
- Servizio di accesso remoto RAS, pagina iniziale
- RAS RAS, vedere Accesso remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e300061c328751f288634faf2f36ab0391ba41d7079e4f42c842d31b3e29397
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788286"
---
# <a name="remote-access"></a>Accesso remoto

## <a name="purpose"></a>Scopo

Usare il servizio di accesso remoto (RAS) per creare applicazioni client. Queste applicazioni visualizzano finestre di dialogo comuni RAS, gestiscono connessioni e dispositivi di accesso remoto e modificano le voci della rubrica. RAS fornisce anche la nuova generazione di funzionalità server per il servizio di accesso remoto (RAS) per Windows. La funzionalità del server RRAS segue e si basa sul servizio di accesso remoto (RAS).

## <a name="where-applicable"></a>Se applicabile

Il servizio di accesso remoto è applicabile in qualsiasi ambiente di elaborazione che usa un collegamento WAN (Wide Area Network) o una rete privata virtuale (VPN). RAS consente di connettere un computer client remoto a un server di rete tramite un collegamento WAN o una VPN. Il computer remoto funziona quindi sulla LAN del server come se il computer remoto fosse connesso direttamente alla LAN. L'API RAS consente ai programmatori di accedere alle funzionalità di RAS a livello di codice.

## <a name="developer-audience"></a>Sviluppatori

L'API RAS è progettata per l'uso da parte dei programmatori C/C++. Anche Visual Basic programmatori microsoft possono trovare utile l'API. I programmatori devono avere familiarità con i concetti relativi alla rete.

## <a name="run-time-requirements"></a>Requisiti di runtime

Alcune delle funzioni nell'API RAS sono supportate solo nei server di rete e altre sono supportate solo nei client di rete. Per informazioni più specifiche sui sistemi operativi che supportano una particolare funzione, vedere le sezioni Requisiti nella documentazione.

La [funzionalità avanzata RAS di](function-comparison-windows-2000-versus-rras-redistributable.md) RRAS è disponibile per Windows NT Server 4.0 installando il [ridistribuibile RRAS.](https://www.microsoft.com/ntserver/nts/downloads/winfeatures/rras/rrasdown.asp) Tutte le funzionalità di RRAS sono incorporate in Windows 2000 Server, Windows Server 2003 e Windows Server 2008. Le applicazioni RRAS non possono essere eseguite Windows NT Workstation 4.0 o nei sistemi operativi client, ad esempio Windows 95. Per informazioni più specifiche sui sistemi operativi che supportano una particolare funzione, vedere le sezioni Requisiti nella documentazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                             | Descrizione                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Servizio di accesso remoto](about-remote-access-service.md)<br/>                               | Il servizio di accesso remoto (RAS) fornisce funzionalità di accesso remoto alle applicazioni client nei computer che eseguono Windows.<br/>                                                                                          |
| [Amministrazione del servizio Accesso remoto](about-remote-access-service-administration.md)<br/> | L'amministrazione del servizio Accesso remoto offre un set di funzioni per l'amministrazione delle autorizzazioni utente e delle porte nei server RAS. Usando queste funzioni, è possibile sviluppare un'applicazione di amministrazione del server RAS.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Routing](routing-start-page.md)
</dt> <dt>

[Protocolli di routing](routing-protocols-start-page.md)
</dt> </dl>

 

 





