---
title: Informazioni Interfaccia utente
description: Il fornitore che implementa il protocollo di autenticazione può anche fornire un'interfaccia utente interattiva per il protocollo.
ms.assetid: 4f8ba0a4-3b52-4e7c-9e67-748f8d81d7a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811f35ac3492e45e80721f800925a003edbb8116ac8c199a1b633e08a28de675
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117781"
---
# <a name="interactive-user-interface"></a>Informazioni Interfaccia utente

Il fornitore che implementa il protocollo di autenticazione può anche fornire un'interfaccia utente interattiva per il protocollo. L'interfaccia utente interattiva consente al protocollo di autenticazione di ottenere informazioni aggiuntive dall'utente in base alle esigenze durante la sessione di autenticazione.

L'interfaccia utente interattiva può essere implementata nella stessa DLL del protocollo di autenticazione o in una DLL separata. Inoltre, la DLL che implementa l'interfaccia utente interattiva può supportare più di un protocollo di autenticazione. Il percorso della DLL per l'interfaccia utente interattiva viene archiviato nel valore del Registro di sistema [RAS \_ EAP \_ VALUENAME \_ INTERACTIVEUI,](authentication-protocol-registry-values.md) sotto la chiave per il protocollo di autenticazione. Per altre informazioni sulla creazione di questo valore del Registro di sistema, vedere [Installazione EAP](eap-installation.md).

La DLL per l'interfaccia utente interattiva deve esportare i punti di ingresso per le funzioni seguenti:<dl>

[**RasEapInvokeInteractiveUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui)  
[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)  
</dl>

L'interfaccia utente interattiva deve [**supportare i messaggi WM \_ COMMAND**](../menurc/wm-command.md) in cui [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) è uguale a IDCANCEL.

Per visualizzare l'interfaccia utente interattiva, il protocollo di autenticazione deve impostare il membro **fInvokeInteractiveUI** della struttura [**\_ PPP EAP \_ OUTPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_output) su **TRUE.** Facoltativamente, il protocollo di autenticazione può impostare i membri **pUIContextData** **e dwSizeOfUIContextData** su **TRUE.** Il servizio di autenticazione usa i valori di questi membri per passare i dati di contesto all'interfaccia utente interattiva. Il protocollo di autenticazione restituisce la **struttura \_ PPP EAP \_ OUTPUT** come parametro nella [**funzione RasEapMakeMessage.**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85))

Il servizio di autenticazione richiama l'interfaccia utente interattiva chiamando [**RasEapInvokeInteractiveUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeinteractiveui). Il servizio passa quindi al protocollo di autenticazione un puntatore ai dati restituiti dall'interfaccia utente interattiva nella chiamata successiva a [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)). Il puntatore viene passato come membro di una [**struttura \_ PPP EAP \_ INPUT.**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) Al **termine di RasEapMakeMessage,** il servizio chiama [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) per liberare la memoria occupata dalle informazioni. Pertanto, il protocollo di autenticazione deve copiare le informazioni in un buffer di memoria privato durante la chiamata a **RasEapMakeMessage**.

 

 