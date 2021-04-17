---
title: Interfaccia utente di configurazione di Client-Side
description: Il fornitore che implementa il protocollo di autenticazione può anche fornire un'interfaccia utente di configurazione (UI) per il protocollo.
ms.assetid: 956a7ad6-1fd5-4938-aa2f-4de646dfd6c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d7296f6afd8fd84f287b6c2c7085e5ed92685f5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337143"
---
# <a name="client-side-configuration-user-interface"></a>Interfaccia utente di configurazione di Client-Side

Il fornitore che implementa il protocollo di autenticazione può anche fornire un'interfaccia utente di configurazione (UI) per il protocollo. L'interfaccia utente di configurazione può essere implementata nella stessa DLL del protocollo di autenticazione o in una DLL separata. Inoltre, la DLL che implementa l'interfaccia utente di configurazione può supportare più di un protocollo di autenticazione. Il percorso della DLL per l'interfaccia utente di configurazione viene archiviato nel \_ valore del registro di sistema Ras EAP \_ valueName \_ configui, sotto la chiave per il protocollo di autenticazione. Per ulteriori informazioni sulla creazione di questo valore del registro di sistema, vedere [EAP Installation](eap-installation.md).

La DLL per l'interfaccia utente di configurazione deve esportare i punti di ingresso per le funzioni seguenti:

[**RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui)

[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Quando l'utente crea una voce di configurazione per una particolare connessione, per un client RAS o wireless, l'utente è in grado di selezionare il protocollo di autenticazione che il servizio deve usare con tale voce. Se il protocollo di autenticazione è configurabile, il servizio chiama [**RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui) per richiamare l'interfaccia utente di configurazione. L'interfaccia utente di configurazione archivia le informazioni di configurazione restituite da **RasEapInvokeConfigUI** nella voce di configurazione.

Le informazioni di configurazione devono essere generiche per tutti gli utenti nel computer client. Le informazioni specifiche di un utente specifico o di utenti non devono essere archiviate nella voce. Il protocollo di autenticazione deve ottenere informazioni specifiche dell'utente usando le [funzioni di identità](obtaining-identity-information.md) o l' [interfaccia utente interattiva](interactive-user-interface.md). Il protocollo di autenticazione può archiviare queste informazioni nel registro di sistema passandole al servizio di autenticazione nel parametro *pEapOutput* di [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)).

Anche le informazioni di configurazione non devono essere specifiche per il computer corrente. deve essere portabile da computer a computer.

Quando il servizio di autenticazione chiama la funzione [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) per il protocollo di autenticazione, passa una struttura di [**\_ \_ input EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) che contiene un puntatore alle informazioni di configurazione. Al termine della chiamata a **RasEapBegin** , il servizio di autenticazione chiama [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) per liberare la memoria occupata dalle informazioni di configurazione. Il protocollo di autenticazione deve pertanto copiare le informazioni di configurazione in un buffer di memoria privato durante la chiamata a **RasEapBegin**.

Il fornitore può aggiungere un valore nella chiave del registro di sistema per il protocollo di autenticazione che specifica le informazioni di configurazione predefinite per il protocollo. Il fornitore può anche aggiungere un valore che specifica se l'utente deve immettere le informazioni di configurazione quando crea una voce della rubrica telefonica. Per ulteriori informazioni, vedere [valori del registro di sistema del protocollo di autenticazione](authentication-protocol-registry-values.md).

 

 