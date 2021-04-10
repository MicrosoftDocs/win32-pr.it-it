---
title: Recupero delle informazioni sull'identità
description: Il fornitore che implementa il protocollo di autenticazione può anche fornire un'interfaccia funzione che ottenga le informazioni di identificazione iniziali per l'utente che richiede l'autenticazione.
ms.assetid: 773c9fdb-c810-4cea-afed-df6484a9c9c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9519da9d66937fd25245fe78f12ef34c3c0ad8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046585"
---
# <a name="obtaining-identity-information"></a>Recupero delle informazioni sull'identità

Il fornitore che implementa il protocollo di autenticazione può anche fornire un'interfaccia funzione che ottenga le informazioni di identificazione iniziali per l'utente che richiede l'autenticazione.

Il fornitore deve implementare le funzioni seguenti.

-   [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)
-   [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Queste funzioni possono essere implementate nella stessa DLL del protocollo di autenticazione o in una DLL separata. Inoltre, la DLL che implementa le funzioni di identità può supportare più di un protocollo di autenticazione. Il percorso della DLL per queste funzioni viene archiviato nel valore del registro di sistema [RAS \_ EAP \_ valueName \_ Identity](authentication-protocol-registry-values.md) , sotto la chiave per il protocollo di autenticazione. Per ulteriori informazioni sulla creazione di questo valore del registro di sistema, vedere [EAP Installation](eap-installation.md).

La funzione [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) Visualizza in genere un'interfaccia utente (UI) per ottenere informazioni sull'identità per l'utente. Tuttavia, se il parametro *dwFlags* contiene il flag RAS \_ EAP \_ flag \_ non \_ interattivo, **RasEapGetIdentity** non dovrebbe visualizzare un'interfaccia utente.

Se [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) Visualizza un'interfaccia utente, l'interfaccia utente deve supportare i messaggi di [**\_ comando WM**](../menurc/wm-command.md) in cui il valore di [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) è uguale a IDCANCEL.

Il servizio di autenticazione chiama [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) se il valore di [RAS \_ EAP \_ valueName \_ Invoke \_ NAMEDLG](authentication-protocol-registry-values.md) che si trova nel registro di sistema per questo EAP è impostato su zero. Se RAS \_ EAP \_ valueName \_ Invoke \_ NAMEDLG non è presente oppure è presente e è impostato su uno, il servizio di autenticazione Visualizza la finestra di dialogo nome utente sistema standard.

Oltre a RAS \_ EAP \_ valueName \_ Invoke \_ NAMEDLG, il fornitore EAP può creare un valore correlato, [RAS \_ EAP \_ valueName \_ Invoke \_ PWDDLG](authentication-protocol-registry-values.md), nel registro di sistema. Se questo valore è presente ed è impostato su zero, il servizio non visualizzerà la finestra di dialogo password di sistema standard. Questo valore è utile quando si implementa un metodo biometrico, ad esempio un'analisi delle impronte digitali, per autenticare l'utente. Se entrambi i \_ \_ valori di Ras EAP valueName \_ Invoke \_ NAMEDLG e RAS \_ EAP \_ valueName \_ Invoke \_ PWDDLG sono pari a zero, è possibile usare un'interfaccia utente Identity per ottenere le informazioni sull'identità e sulla biometrica. Tuttavia, se solo RAS \_ EAP \_ valueName \_ Invoke \_ PWDDLG è zero, il servizio di autenticazione non chiamerà [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity). In questo caso, è possibile usare l' [interfaccia utente interattiva](interactive-user-interface.md) per ottenere le informazioni biometriche.

Per ulteriori informazioni su questi valori del registro di sistema, vedere [valori del registro di sistema del protocollo di autenticazione](authentication-protocol-registry-values.md).

Le informazioni ottenute da [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) vengono passate al protocollo di autenticazione durante la chiamata a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)). Le informazioni sono indicate dai membri **pszIdentity** e **pUserData** della struttura di [**\_ \_ input EAP PPP**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) . Per salvare queste informazioni nel registro di sistema del computer client, il protocollo di autenticazione deve restituire le informazioni nel parametro *pEapOutput* di [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)).

Dopo la chiamata a [**RasEapBegin**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)), il servizio di autenticazione chiama [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) per liberare la memoria occupata dai dati. Il protocollo di autenticazione deve pertanto copiare le informazioni in un buffer di memoria privato durante la chiamata a **RasEapBegin**.

 

 