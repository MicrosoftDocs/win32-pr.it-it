---
description: Windows Sockets 2 (Winsock) consente ai programmatori di creare applicazioni Internet, Intranet e altre applicazioni idonee per la rete per la trasmissione di dati dell'applicazione in transito, indipendentemente dal protocollo di rete utilizzato.
ms.assetid: 1ec8758a-40fd-4c98-b839-c2409ef712d6
title: Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df253572d2fca117dbc8b45b451f8c3bacc2f360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130410"
---
# <a name="windows-sockets-2"></a>Windows Sockets 2

## <a name="purpose"></a>Scopo

Windows Sockets 2 (Winsock) consente ai programmatori di creare applicazioni Internet, Intranet e altre applicazioni idonee per la rete per la trasmissione di dati dell'applicazione in transito, indipendentemente dal protocollo di rete utilizzato. Con Winsock, i programmatori possono accedere alle funzionalità di rete avanzate di Microsoft® Windows®, ad esempio il multicast e la qualità del servizio (QoS).

Winsock segue il modello WOSA (Windows Open System Architecture); definisce un'interfaccia del provider di servizi (SPI) standard tra il Application Programming Interface (API), con le funzioni esportate e gli stack di protocolli. Usa il paradigma Sockets che è stato inizialmente popolare da Berkeley Software Distribution (BSD) UNIX. In seguito è stato adattato per Windows in Windows Sockets 1,1, con cui le applicazioni Windows Sockets 2 sono compatibili con le versioni precedenti. Programmazione Winsock precedentemente centrata su TCP/IP. Alcune procedure di programmazione che hanno funzionato con TCP/IP non funzionano con ogni protocollo. Di conseguenza, l'API di Windows Sockets 2 aggiunge funzioni laddove necessario per gestire diversi protocolli.

## <a name="developer-audience"></a>Sviluppatori

Windows Sockets 2 è progettato per l'uso da programmatori C/C++. È necessaria una certa familiarità con la rete di Windows.

## <a name="run-time-requirements"></a>Requisiti di runtime

Windows Sockets 2 può essere usato in tutte le piattaforme Windows. Laddove sono presenti alcune implementazioni o funzionalità delle restrizioni della piattaforma Windows Sockets 2, sono chiaramente indicate nella documentazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                             | Descrizione                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novità di Windows Sockets](what-s-new-for-windows-sockets-2.md)<br/>                 | Informazioni sulle nuove funzionalità per Windows Sockets.<br/>                                                                                                                                                                                                                                 |
| [Supporto del protocollo di rete Winsock in Windows](network-protocol-support-in-windows.md)<br/> | Informazioni sul supporto del protocollo di rete per Windows Sockets in versioni diverse di Windows.<br/>                                                                                                                                                                                    |
| [Informazioni su Winsock](about-winsock.md)<br/>                                                     | Informazioni generali sulla programmazione di Windows Socket considerazioni, architettura e funzionalità disponibili per gli sviluppatori.<br/>                                                                                                                                                       |
| [Uso di Winsock](using-winsock.md)<br/>                                                     | Procedure e tecniche di programmazione utilizzate con Windows Sockets. Questa sezione include tecniche di programmazione Winsock di base, ad esempio [Introduzione con Winsock](getting-started-with-winsock.md), nonché tecniche avanzate utili per gli sviluppatori Winsock esperti.<br/> |
| [Riferimento Winsock](winsock-reference.md)<br/>                                             | Documentazione dell'API di Windows Sockets.<br/>                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Helper IP](../iphlp/ip-helper-start-page.md)
</dt> <dt>

[QoS (Quality of Service)](/previous-versions/windows/desktop/qos/qos-start-page)
</dt> </dl>

 

 
