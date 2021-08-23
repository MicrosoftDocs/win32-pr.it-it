---
title: Client-Side configurazione Interfaccia utente
description: Il fornitore che implementa il protocollo di autenticazione può anche fornire un'interfaccia utente di configurazione per il protocollo.
ms.assetid: 956a7ad6-1fd5-4938-aa2f-4de646dfd6c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13c8b067ba65312edea412ba532620e029912088e9cc61885626f8a13f5a2834
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119117806"
---
# <a name="client-side-configuration-user-interface"></a>Client-Side configurazione Interfaccia utente

Il fornitore che implementa il protocollo di autenticazione può anche fornire un'interfaccia utente di configurazione per il protocollo. L'interfaccia utente di configurazione può essere implementata nella stessa DLL del protocollo di autenticazione o in una DLL separata. Inoltre, la DLL che implementa l'interfaccia utente di configurazione può supportare più di un protocollo di autenticazione. Il percorso della DLL per l'interfaccia utente di configurazione viene archiviato nel valore del Registro di sistema RAS \_ EAP VALUENAME CONFIGUI, sotto la \_ chiave per il protocollo di \_ autenticazione. Per altre informazioni sulla creazione di questo valore del Registro di sistema, vedere [Installazione EAP](eap-installation.md).

La DLL per l'interfaccia utente di configurazione deve esportare i punti di ingresso per le funzioni seguenti:

[**RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui)

[**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Quando l'utente crea una voce di configurazione per una determinata connessione, sia per un client RAS che per un client wireless, l'utente può selezionare il protocollo di autenticazione che il servizio deve usare con tale voce. Se il protocollo di autenticazione è configurabile, il servizio chiama [**RasEapInvokeConfigUI**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapinvokeconfigui) per richiamare l'interfaccia utente di configurazione. L'interfaccia utente di configurazione archivia le informazioni di configurazione restituite da **RasEapInvokeConfigUI** nella voce di configurazione.

Le informazioni di configurazione devono essere generiche per tutti gli utenti nel computer client. Le informazioni specifiche di uno o più utenti specifici non devono essere archiviate nella voce. Il protocollo di autenticazione deve ottenere informazioni specifiche dell'utente usando le funzioni [di identità](obtaining-identity-information.md) o [l'interfaccia utente interattiva](interactive-user-interface.md). Il protocollo di autenticazione può archiviare queste informazioni nel Registro di sistema passandolo al servizio di autenticazione nel *parametro pEapOutput* [**di RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)).

Anche le informazioni di configurazione non devono essere specifiche per il computer corrente. deve essere portabile da computer a computer.

Quando il servizio di autenticazione chiama la [**funzione RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) per il protocollo di autenticazione, passa una struttura [**\_ PPP EAP \_ INPUT**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) che contiene un puntatore alle informazioni di configurazione. Al termine della chiamata **a RasEapBegin,** il servizio di autenticazione chiama [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) per liberare la memoria occupata dalle informazioni di configurazione. Pertanto, il protocollo di autenticazione deve copiare le informazioni di configurazione in un buffer di memoria privato durante la chiamata a **RasEapBegin**.

Il fornitore può aggiungere un valore nella chiave del Registro di sistema per il protocollo di autenticazione che specifica le informazioni di configurazione predefinite per il protocollo. Il fornitore può anche aggiungere un valore che specifica se l'utente deve immettere le informazioni di configurazione quando crea una voce della rubrica telefonica. Per altre informazioni, vedere [Valori del Registro di sistema del protocollo di autenticazione](authentication-protocol-registry-values.md).

 

 