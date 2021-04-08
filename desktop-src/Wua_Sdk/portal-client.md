---
description: L'API dell'agente di Windows Update (WUA) è un set di interfacce COM che consentono agli amministratori di sistema e ai programmatori di accedere Windows Update e Windows Server Update Services (WSUS).
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: API dell'agente Windows Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c34cb76619c9739c84e650a32590fdc4f61022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749999"
---
# <a name="windows-update-agent-api"></a>API dell'agente Windows Update

## <a name="purpose"></a>Scopo

L'API dell'agente di Windows Update (WUA) è un set di interfacce COM che consentono agli amministratori di sistema e ai programmatori di accedere Windows Update e [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)). È possibile scrivere script e programmi per esaminare gli aggiornamenti attualmente disponibili per un computer, quindi è possibile installare o disinstallare gli aggiornamenti.

## <a name="where-applicable"></a>Se applicabile

Gli amministratori di sistema possono utilizzare WUA per determinare a livello di codice gli aggiornamenti da applicare a un computer, scaricare tali aggiornamenti e quindi installarli senza interventi da parte dell'utente.

I fornitori di software indipendenti (ISV) e gli sviluppatori di utenti finali possono integrare le funzionalità di WUA nel software di gestione dei computer o degli aggiornamenti per offrire un ambiente operativo semplice.

## <a name="developer-audience"></a>Sviluppatori

È possibile scrivere applicazioni WUA in diversi linguaggi di programmazione. WUA definisce le interfacce e gli oggetti accessibili da Visual Basic, Visual Basic Scripting Edition (VBScript), JScript e da C e C++. Una certa familiarità con la programmazione COM è utile per il programmatore WUA.

## <a name="run-time-requirements"></a>Requisiti di runtime

WUA è supportato a partire da Windows XP. WUA è supportato nel server che inizia con Windows Server 2003.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Uso dell'API Windows Update Agent](using-the-windows-update-agent-api.md)
-   [Informazioni di riferimento sull'API WUA](windows-update-agent--wua--api-reference.md)

 

 
