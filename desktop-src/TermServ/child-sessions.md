---
title: Sessioni figlio
description: A partire da Windows Server 2012 e Windows 8, Desktop remoto supporta il concetto di sessione figlio, ovvero una sessione di loopback speciale Desktop remoto associata alla sessione esistente di un utente.
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d79fa6e18cece69c672b60a65e679441ce986a6cd8a0ad46524440738c3844
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010421"
---
# <a name="child-sessions"></a>Sessioni figlio

A partire da Windows Server 2012 e Windows 8, Desktop remoto supporta il concetto di sessione figlio , ovvero una sessione di loopback speciale Desktop remoto associata alla sessione esistente di un utente.

Le sessioni figlio non sono supportate nei sistemi operativi seguenti:

<dl> Windows RT  
Windows Server 2012 Opzione di installazione Server Core  
Microsoft Hyper-V Server 2012  
</dl>

Un sistema può avere una sola sessione figlio attiva e connessa in un determinato momento.

La sessione figlio può essere terminata disconnettendo direttamente da essa oppure verrà terminata al termine della sessione padre.

Prima di poter usare le sessioni figlio in un sistema, è necessario abilitare la funzionalità della sessione figlio chiamando la [**funzione WTSEnableChildSessions.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) È anche possibile determinare se le sessioni figlio sono state abilitate usando la [**funzione WTSIsChildSessionsEnabled.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)

Una sessione figlio può essere creata solo dall'interno di una sessione utente esistente usando il controllo [Desktop remoto ActiveX](remote-desktop-activex-control.md) e impostando la proprietà "ConnectToChildSession" con [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md) prima della connessione. Quando viene chiamato il metodo [**IMsTscAx.Connessione,**](imstscax-connect.md) il controllo Desktop remoto ActiveX accede automaticamente alla sessione figlio senza richiedere le credenziali, tranne quando l'utente è connesso alla sessione padre usando un smart card. A differenza di una Desktop remoto normale, un utente non ha bisogno del diritto Interattivo remoto per accedere alla sessione figlio perché si tratta di una sessione di loopback.

Una sessione figlio non può essere bloccata. Non avrà alcuna screen saver e nessuna schermata di accesso. Inoltre, a differenza di una sessione normale, se è impostato il criterio di testo di accesso WinLogon, il testo di accesso non verrà visualizzato in questa sessione figlio. Inoltre, non vi sarà alcun effetto dei criteri Connessione Desktop remoto di gruppo timeout nella sessione figlio se questi criteri sono impostati.

Le API seguenti vengono usate insieme alle sessioni figlio:

-   [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   Proprietà "ConnectToChildSession" in [ **IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md)

 

 




