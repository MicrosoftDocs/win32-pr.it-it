---
description: L'API helper protocollo Internet (helper IP) consente il recupero e la modifica delle impostazioni di configurazione di rete per il computer locale.
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: Helper IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1d50153e1ad890063f33a473058f6a850a9f171
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879090"
---
# <a name="ip-helper"></a>Helper IP

## <a name="purpose"></a>Scopo

L'API helper protocollo Internet (helper IP) consente il recupero e la modifica delle impostazioni di configurazione di rete per il computer locale.

## <a name="where-applicable"></a>Se applicabile

L'API helper IP è applicabile in qualsiasi ambiente informatico in cui è utile modificare a livello di codice la rete e la configurazione TCP/IP. Le applicazioni tipiche includono i protocolli di routing IP e gli agenti Simple Network Management Protocol (SNMP).

## <a name="developer-audience"></a>Sviluppatori

L'API helper IP è progettata per l'uso da parte dei programmatori C/C++. I programmatori devono inoltre acquisire familiarità con i concetti relativi alla rete Windows e TCP/IP.

## <a name="run-time-requirements"></a>Requisiti di runtime

L'API helper IP può essere usata in tutte le piattaforme Windows. Non tutti i sistemi operativi supportano tutte le funzioni. Laddove sono presenti alcune implementazioni o funzionalità delle restrizioni della piattaforma Windows Sockets 2, sono chiaramente indicate nella documentazione. Se una funzione helper IP viene chiamata su una piattaforma che non supporta la funzione, \_ viene restituito l'errore non \_ supportato. Per informazioni più specifiche sui sistemi operativi che supportano una particolare funzione, vedere le sezioni requisiti nella documentazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                              | Descrizione                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novità dell'helper IP](what-s-new-in-ip-helper.md)<br/>  | Informazioni sulle nuove funzionalità per l'helper IP.<br/>                                                                                                                                                             |
| [Informazioni su helper IP](about-ip-helper.md)<br/>                  | Informazioni generali sulle funzionalità e le considerazioni sulla programmazione dell'helper IP disponibili per gli sviluppatori.<br/>                                                                                               |
| [Uso dell'helper IP](using-ip-helper.md)<br/>                  | Procedure e tecniche di programmazione utilizzate con l'helper IP. Questa sezione include tecniche di programmazione di base per l'helper IP, ad esempio [Introduzione con l'helper IP](getting-started-with-ip-helper.md).<br/> |
| [Riferimento dell'helper IP](ip-helper-function-reference.md)<br/> | Documentazione di riferimento per le funzioni di supporto IP, le strutture e le enumerazioni.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sockets 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[Routing and Remote Access Service](../rras/routing-start-page.md)
</dt> </dl>

 

