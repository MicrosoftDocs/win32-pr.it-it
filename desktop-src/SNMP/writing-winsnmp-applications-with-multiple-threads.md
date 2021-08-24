---
title: Scrittura di applicazioni WinSNMP con più thread
description: L'implementazione Di Microsoft WinSNMP garantisce che le operazioni WinSNMP di un processo non modificano le impostazioni WinSNMP di un altro processo.
ms.assetid: faa98704-f55f-4450-9f6e-d2bbbc7a50b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33ee400009204a1117eb54b8166ade2c10f3d1dd3317a8316d70fc8c2d606d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142734"
---
# <a name="writing-winsnmp-applications-with-multiple-threads"></a>Scrittura di applicazioni WinSNMP con più thread

L'implementazione Di Microsoft WinSNMP garantisce che le operazioni WinSNMP di un processo non modificano le impostazioni WinSNMP di un altro processo.

Un'applicazione WinSNMP con più thread deve garantire che le operazioni WinSNMP che impostano i parametri a livello di applicazione siano thread-safe. Le funzioni che impostano i parametri a livello di applicazione [**sono SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) e [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode). Queste funzioni modificano le impostazioni per la modalità di conversione di entità e contesto e la modalità di ritrasmissione.

Per altre informazioni, vedere [Thread multipli](/windows/desktop/ProcThread/multiple-threads) e Sicurezza [dei thread e Diritti di accesso.](/windows/desktop/ProcThread/thread-security-and-access-rights)

 

 