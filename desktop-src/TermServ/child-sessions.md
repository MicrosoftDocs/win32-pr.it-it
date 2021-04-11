---
title: Sessioni figlio
description: A partire da Windows Server 2012 e Windows 8, Desktop remoto supporta il concetto di sessione figlio, ovvero una sessione speciale di Desktop remoto loopback collegata alla sessione esistente di un utente.
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788b36bf9799da9b0cb7486963f3154451ca5392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220966"
---
# <a name="child-sessions"></a>Sessioni figlio

A partire da Windows Server 2012 e Windows 8, Desktop remoto supporta il concetto di *sessione figlio*, ovvero una sessione speciale di desktop remoto loopback collegata alla sessione esistente di un utente.

Le sessioni figlio non sono supportate nei sistemi operativi seguenti:

<dl> Windows RT  
Opzione di installazione Server Core di Windows Server 2012  
Microsoft Hyper-V Server 2012  
</dl>

Un sistema può avere una sola sessione figlio attiva e connessa in un determinato momento.

La sessione figlio può essere terminata disconnettendosi direttamente da tale sessione o verrà terminata al termine della sessione padre.

Prima di poter utilizzare le sessioni figlio in un sistema, è necessario abilitare la funzionalità della sessione figlio chiamando la funzione [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) . È inoltre possibile determinare se le sessioni figlio sono state abilitate tramite la funzione [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) .

Una sessione figlio può essere creata solo dall'interno di una sessione utente esistente usando il [controllo ActiveX Desktop remoto](remote-desktop-activex-control.md) e impostando la proprietà "ConnectToChildSession" con [**IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md) prima della connessione. Quando viene chiamato il metodo [**IMsTscAx. Connect**](imstscax-connect.md) , il controllo ActiveX Desktop remoto effettuerà automaticamente l'accesso alla sessione figlio senza richiedere le credenziali, tranne quando l'utente è connesso alla sessione padre tramite una smart card. A differenza di una normale sessione di Desktop remoto, un utente non necessita del diritto interattivo remoto per accedere alla sessione figlio perché si tratta di una sessione di loopback.

Una sessione figlio non può essere bloccata. Non avrà screen saver e nessuna schermata di accesso. Inoltre, a differenza di una sessione normale, se è impostato il criterio del testo di accesso WinLogon, il testo di accesso non verrà visualizzato in questa sessione figlio. Se questi criteri sono impostati, inoltre, non si verifica alcun effetto dei criteri di gruppo di timeout Connessione Desktop remoto nella sessione figlio.

Le API seguenti vengono usate insieme alle sessioni figlio:

-   [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [**WTSGetChildSessionId**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   Proprietà "ConnectToChildSession" in [ **IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md)

 

 




