---
description: L'API Windows Update Agent (WUA) è un set di interfacce COM che consentono agli amministratori di sistema e ai programmatori di accedere Windows Update e Windows Server Update Services (WSUS).
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: Windows API dell'agente di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82e7e2c79a707424128082f8f3123cb5fff506a9fc98203ab1fdf8063393310d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738003"
---
# <a name="windows-update-agent-api"></a>Windows API dell'agente di aggiornamento

## <a name="purpose"></a>Scopo

L'API Windows Update Agent (WUA) è un set di interfacce COM che consentono agli amministratori di sistema e ai programmatori di accedere a Windows Update [e Windows Server Update Services (WSUS).](/previous-versions/windows/desktop/ms744624(v=vs.85)) È possibile scrivere script e programmi per esaminare gli aggiornamenti attualmente disponibili per un computer e quindi installare o disinstallare gli aggiornamenti.

## <a name="where-applicable"></a>Se applicabile

Gli amministratori di sistema possono usare WUA per determinare a livello di codice quali aggiornamenti devono essere applicati a un computer, scaricare tali aggiornamenti e quindi installarli senza intervento dell'utente.

I fornitori di software indipendenti (ISV) e gli sviluppatori degli utenti finali possono integrare le funzionalità WUA nella gestione dei computer o nel software di gestione degli aggiornamenti per offrire un ambiente operativo senza problemi.

## <a name="developer-audience"></a>Sviluppatori

È possibile scrivere applicazioni WUA in diversi linguaggi di programmazione. WUA definisce interfacce e oggetti accessibili da Visual Basic, Visual Basic Scripting Edition (VBScript), JScript e da C e C++. Una familiarità con la programmazione COM è utile per il programmatore WUA.

## <a name="run-time-requirements"></a>Requisiti di runtime

WUA è supportato a partire da Windows XP. WUA è supportato nel server a partire da Windows Server 2003.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Uso dell'API Windows Update Agent](using-the-windows-update-agent-api.md)
-   [Informazioni di riferimento sulle API WUA](windows-update-agent--wua--api-reference.md)

 

 
