---
title: Recupero di informazioni di identità
description: Il fornitore che implementa il protocollo di autenticazione può anche fornire un'interfaccia di funzione che ottiene informazioni di identificazione iniziali per l'utente che richiede l'autenticazione.
ms.assetid: 773c9fdb-c810-4cea-afed-df6484a9c9c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46245b22a5538fc347ba735620270b7bbc1071574852305adc6b3881202ae317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605821"
---
# <a name="obtaining-identity-information"></a>Recupero di informazioni di identità

Il fornitore che implementa il protocollo di autenticazione può anche fornire un'interfaccia di funzione che ottiene informazioni di identificazione iniziali per l'utente che richiede l'autenticazione.

Il fornitore deve implementare le funzioni seguenti.

-   [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity)
-   [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory)

Queste funzioni possono essere implementate nella stessa DLL del protocollo di autenticazione o in una DLL separata. Inoltre, la DLL che implementa le funzioni di identità può supportare più di un protocollo di autenticazione. Il percorso della DLL per queste funzioni viene archiviato nel valore del Registro di sistema [RAS \_ EAP \_ VALUENAME \_ IDENTITY,](authentication-protocol-registry-values.md) sotto la chiave per il protocollo di autenticazione. Per altre informazioni sulla creazione di questo valore del Registro di sistema, vedere [Installazione EAP.](eap-installation.md)

La [**funzione RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) visualizza in genere un'interfaccia utente per ottenere informazioni di identità per l'utente. Tuttavia, se il *parametro dwFlags* contiene il flag RAS \_ EAP \_ FLAG NON \_ \_ INTERACTIVE, **RasEapGetIdentity** non deve visualizzare un'interfaccia utente.

Se [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) visualizza un'interfaccia utente, l'interfaccia utente deve supportare i messaggi [**WM \_ COMMAND**](../menurc/wm-command.md) in cui il valore di [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))(*wParam*) è uguale a IDCANCEL.

Il servizio di autenticazione chiama [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) se il valore [RAS \_ EAP \_ VALUENAME \_ INVOKE \_ NAMEDLG](authentication-protocol-registry-values.md) presente nel Registro di sistema per questo EAP è impostato su zero. Se RAS \_ EAP VALUENAME INVOKE NAMEDLG non è presente o è presente ed è impostato su uno, il servizio di autenticazione visualizza la finestra di dialogo standard nome utente \_ \_ di \_ sistema.

Oltre a RAS EAP VALUENAME INVOKE NAMEDLG, il fornitore EAP può creare un valore \_ \_ \_ \_ correlato, [RAS \_ EAP \_ VALUENAME \_ INVOKE \_ PWDDLG,](authentication-protocol-registry-values.md)nel Registro di sistema. Se questo valore è presente e è impostato su zero, il servizio non visualizza la finestra di dialogo della password di sistema standard. Questo valore è utile quando si implementa un metodo biometrico, ad esempio una scansione con impronta digitale, per autenticare l'utente. Se entrambi i valori DI RAS \_ EAP \_ VALUENAME INVOKE NAMEDLG e \_ RAS \_ \_ EAP \_ VALUENAME \_ INVOKE \_ PWDDLG sono pari a zero, è possibile usare un'interfaccia utente di identità per ottenere sia l'identità che le informazioni biometriche. Tuttavia, se solo RAS EAP VALUENAME INVOKE PWDDLG è zero, il servizio di autenticazione non chiamerà \_ \_ \_ \_ [**RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity). In questo caso, è possibile usare [l'interfaccia utente interattiva per](interactive-user-interface.md) ottenere le informazioni biometriche.

Per altre informazioni su questi valori del Registro di sistema, vedere [Authentication Protocol Registry Values](authentication-protocol-registry-values.md).

Le informazioni ottenute [**da RasEapGetIdentity**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapgetidentity) vengono passate al protocollo di autenticazione durante la chiamata [**a RasEapBegin.**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85)) Le informazioni sono a cui puntano **i membri pszIdentity** e **pUserData** della [**struttura \_ PPP EAP \_ INPUT.**](/windows/desktop/api/Raseapif/ns-raseapif-ppp_eap_input) Per salvare queste informazioni nel Registro di sistema nel computer client, il protocollo di autenticazione deve restituire le informazioni nel *parametro pEapOutput* di [**RasEapMakeMessage**](/previous-versions/windows/desktop/legacy/aa363532(v=vs.85)).

Dopo la chiamata [**a RasEapBegin,**](/previous-versions/windows/desktop/legacy/aa363520(v=vs.85))il servizio di autenticazione chiama [**RasEapFreeMemory**](/previous-versions/windows/desktop/api/Raseapif/nf-raseapif-raseapfreememory) per liberare la memoria occupata da questi dati. Pertanto, il protocollo di autenticazione deve copiare le informazioni in un buffer di memoria privato durante la chiamata **a RasEapBegin**.

 

 