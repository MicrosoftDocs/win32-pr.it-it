---
title: Interfaccia utente interattiva
description: Il fornitore che implementa il protocollo di autenticazione può anche fornire un'interfaccia utente interattiva (UI) per il protocollo.
ms.assetid: 4f8ba0a4-3b52-4e7c-9e67-748f8d81d7a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761799969f4e439a65534ab551f09b3788e95ba7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299616"
---
# <a name="interactive-user-interface"></a>Interfaccia utente interattiva

Il fornitore che implementa il protocollo di autenticazione può anche fornire un'interfaccia utente interattiva (UI) per il protocollo. L'interfaccia utente interattiva consente al protocollo di autenticazione di ottenere informazioni aggiuntive dall'utente, in base alle esigenze, nel corso della sessione di autenticazione.

L'interfaccia utente interattiva può essere implementata nella stessa DLL del protocollo di autenticazione o in una DLL separata. Inoltre, la DLL che implementa l'interfaccia utente interattiva può supportare più di un protocollo di autenticazione. Il percorso della DLL per l'interfaccia utente interattiva viene archiviato nel valore del registro di sistema [RAS \_ EAP \_ valueName \_ INTERACTIVEUI](authentication-protocol-registry-values.md) , sotto la chiave per il protocollo di autenticazione. Per ulteriori informazioni sulla creazione di questo valore del registro di sistema, vedere [EAP Installation](eap-installation.md).

La DLL per l'interfaccia utente interattiva deve esportare i punti di ingresso per le funzioni seguenti:<dl>

[**RasEapInvokeInteractiveUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui)  
[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)  
</dl>

L'interfaccia utente interattiva deve supportare i messaggi di [**\_ comando WM**](../menurc/wm-command.md) in cui [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) è uguale a IDCANCEL.

Per visualizzare l'interfaccia utente interattiva, il protocollo di autenticazione deve impostare il membro **fInvokeInteractiveUI** della struttura di [**\_ \_ output EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) su **true**. Il protocollo di autenticazione può impostare facoltativamente anche i membri **pUIContextData** e **dwSizeOfUIContextData** su **true** . Il servizio di autenticazione usa i valori di questi membri per passare i dati di contesto all'interfaccia utente interattiva. Il protocollo di autenticazione restituisce la struttura di **\_ \_ output EAP PPP** come parametro nella funzione [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)) .

Il servizio di autenticazione richiama l'interfaccia utente interattiva chiamando [**RasEapInvokeInteractiveUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui). Il servizio passa quindi il protocollo di autenticazione un puntatore ai dati restituiti dall'interfaccia utente interattiva nella chiamata successiva a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)). Il puntatore viene passato come membro di una struttura [**di \_ \_ input EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) . Quando **RasEapMakeMessage** restituisce, il servizio chiama [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) per liberare la memoria occupata dalle informazioni. Il protocollo di autenticazione deve pertanto copiare le informazioni in un buffer di memoria privato durante la chiamata a **RasEapMakeMessage**.

 

 