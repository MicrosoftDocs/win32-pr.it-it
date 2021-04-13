---
title: Scrittura di applicazioni WinSNMP con più thread
description: L'implementazione di Microsoft WinSNMP garantisce che le operazioni WinSNMP di un processo non modifichino le impostazioni di WinSNMP di un altro processo.
ms.assetid: faa98704-f55f-4450-9f6e-d2bbbc7a50b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb6b7991968c5c5efafa898758c3c60cad1abb2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399331"
---
# <a name="writing-winsnmp-applications-with-multiple-threads"></a>Scrittura di applicazioni WinSNMP con più thread

L'implementazione di Microsoft WinSNMP garantisce che le operazioni WinSNMP di un processo non modifichino le impostazioni di WinSNMP di un altro processo.

Un'applicazione WinSNMP con più thread deve garantire che le operazioni WinSNMP che impostano i parametri a livello di applicazione siano thread-safe. Le funzioni che impostano i parametri a livello di applicazione sono [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) e [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode). Queste funzioni modificano le impostazioni per la modalità di conversione dell'entità e del contesto e la modalità di ritrasmissione.

Per altre informazioni, vedere [più thread](/windows/desktop/ProcThread/multiple-threads) e [diritti di accesso e sicurezza dei thread](/windows/desktop/ProcThread/thread-security-and-access-rights).

 

 