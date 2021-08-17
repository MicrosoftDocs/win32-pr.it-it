---
description: L'API Internet Protocol Helper (HELPER IP) consente il recupero e la modifica delle impostazioni di configurazione di rete per il computer locale.
ms.assetid: 4896a9f8-0486-4380-bf49-d1c9ef114acc
title: Helper IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6262543d1644fbe62858f2c90064f42d2c1348b2f3c56033813f453d33470ce3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146774"
---
# <a name="ip-helper"></a>Helper IP

## <a name="purpose"></a>Scopo

L'API Internet Protocol Helper (HELPER IP) consente il recupero e la modifica delle impostazioni di configurazione di rete per il computer locale.

## <a name="where-applicable"></a>Se applicabile

L'API helper IP è applicabile in qualsiasi ambiente informatico in cui è utile modificare a livello di codice la configurazione di rete e TCP/IP. Le applicazioni tipiche includono protocolli di routing IP e Simple Network Management Protocol (SNMP).

## <a name="developer-audience"></a>Sviluppatori

L'API helper IP è progettata per l'uso da parte dei programmatori C/C++. I programmatori devono anche avere familiarità con Windows di rete e tcp/IP.

## <a name="run-time-requirements"></a>Requisiti di runtime

L'API helper IP può essere usata in tutte le piattaforme Windows ip. Non tutti i sistemi operativi supportano tutte le funzioni. Laddove esistono determinate implementazioni o funzionalità di Windows della piattaforma Sockets 2, vengono chiaramente notate nella documentazione. Se viene chiamata una funzione helper IP in una piattaforma che non supporta la funzione, viene restituito ERROR \_ NOT \_ SUPPORTED. Per informazioni più specifiche sui sistemi operativi che supportano una determinata funzione, vedere le sezioni Requisiti della documentazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                              | Descrizione                                                                                                                                                                                                       |
|--------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novità dell'helper IP](what-s-new-in-ip-helper.md)<br/>  | Informazioni sulle nuove funzionalità per l'helper IP.<br/>                                                                                                                                                             |
| [Informazioni sull'helper IP](about-ip-helper.md)<br/>                  | Informazioni generali sulle considerazioni sulla programmazione dell'helper IP e sulle funzionalità disponibili per gli sviluppatori.<br/>                                                                                               |
| [Uso dell'helper IP](using-ip-helper.md)<br/>                  | Procedure e tecniche di programmazione usate con l'helper IP. Questa sezione include tecniche di programmazione di base dell'helper IP, ad esempio [Attività iniziali con l'helper IP.](getting-started-with-ip-helper.md)<br/> |
| [Riferimento dell'helper IP](ip-helper-function-reference.md)<br/> | Documentazione di riferimento per funzioni, strutture ed enumerazioni dell'helper IP.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Socket 2](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[Routing and Remote Access Service](../rras/routing-start-page.md)
</dt> </dl>

 

