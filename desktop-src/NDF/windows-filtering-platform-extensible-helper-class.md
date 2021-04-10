---
title: Classe helper Windows Filtering Platform estendibile
description: Windows Filtering Platform (WFP) include una classe helper NDF (Network Diagnostics Framework), denominata FPHC (Filtering Platform Helper Class).
ms.assetid: 006ea30c-8682-4a3d-803a-73dba5162696
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858835c1a649602293ed042c13205ca982de9258
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963163"
---
# <a name="windows-filtering-platform-extensible-helper-class"></a>Classe helper Windows Filtering Platform estendibile

[Windows Filtering Platform (WFP](/windows/desktop/FWP/windows-filtering-platform-start-page) ) include una classe helper NDF (Network Diagnostics Framework), denominata fphc (Filtering Platform Helper Class). FPHC consente di identificare le cause principali dei problemi di connettività causati da WFP. Gli sviluppatori di firewall di terze parti possono implementare le proprie classi helper NDF. L'estendibilità di FPHC consente di richiamare le classi helper di terze parti durante la diagnostica.

In questo argomento si presuppone una certa familiarità con l' [API PAM](/windows/desktop/FWP/windows-filtering-platform-start-page).

## <a name="why-extend-the-fphc"></a>Perché estendere il FPHC?

Tutti gli sviluppatori che scrivono applicazioni che chiamano l'API WFP devono scrivere una classe helper NDF che estende FPHC.

FPHC è in grado di identificare WFP come causa di un problema di connettività. Se disponibile, FPHC può anche identificare il provider che ha creato il filtro che blocca il traffico di rete. FPHC passa queste informazioni a NDF, che a sua volta può notificare all'utente che il PAM sta causando il problema di connettività e fornire il nome del provider che blocca il traffico.

Tuttavia, FPHC non può suggerire un'azione correttiva all'utente, né può fornire il motivo per cui il filtro blocca il traffico verso l'utente. Queste attività possono essere eseguite solo da un'estensione FPHC.

Si consideri un'applicazione firewall di terze parti che chiama l'API Pam. Se il firewall di terze parti implementa un'estensione FPHC, è possibile implementare azioni personalizzate per gestire i problemi di connettività identificati da NDF. Quando NDF diagnostica che un'applicazione è stata bloccata dal firewall di terze parti, l'estensione FPHC può gestire l'evento di blocco. Un modo in cui l'estensione FPHC può gestire un evento consiste nel presentare all'utente un prompt per sbloccare un programma usando il firewall e quindi sbloccare il programma alla conferma dell'utente. In alternativa, l'estensione FPHC può gestire un evento notificando all'utente il motivo per cui l'applicazione è stata bloccata, ad esempio un'applicazione è stata bloccata perché era considerata malware dal firewall.

## <a name="about-wfp-diagnostics"></a>Informazioni sulla diagnostica WFP

Quando NDF viene richiamato per diagnosticare un problema di rete, vengono contattate le classi helper per determinare la causa del problema. Se una classe helper di livello superiore determina che un errore di rete potrebbe essere causato da WFP, viene generata un'ipotesi per FPHC in base alle informazioni disponibili. NDF passa questa ipotesi, sotto forma di diversi attributi evento, a FPHC. Questi attributi sono descritti in dettaglio nella sezione degli [attributi degli eventi di fphc](#windows-filtering-platform-extensible-helper-class) riportata di seguito.

Un problema di rete può essere descritto come un problema di connettività che influisce su un tentativo di connessione specifico. Ad esempio, è possibile che l'utente abbia accidentalmente bloccato un'applicazione facendo clic inavvertitamente su **non consentire**. Il firewall bloccherà quindi l'applicazione dal binding a qualsiasi porta. L'utente, non sapendo perché l'applicazione è bloccata, può provare a diagnosticare il problema tramite un punto di ingresso offerto dall'applicazione. FPHC osserverà i log e, se trova una corrispondenza, recupererà l'ID del filtro e l'ID del provider di quel particolare filtro. A questo punto, FPHC sa chi è il proprietario di quel filtro e passa il processo diagnostico alla classe helper appropriata per un'ulteriore diagnosi.

L'evento più recente nei registri eventi di WFP per trovare la corrispondenza con gli attributi è selezionato come pertinente per il problema di rete. Se non viene trovato alcun evento corrispondente e l'ora in cui si è verificato l'evento viene analizzato nel registro WFP, FPHC indica a NDF che è integro. Se non vengono trovati eventi corrispondenti e i log del WFP non includono l'ora in cui si è verificato l'evento, FPHC restituisce uno stato indeterminato a NDF.

Se viene trovato un evento corrispondente, FPHC usa l'ID del provider del filtro che ha provocato l'evento per identificare il provider della regola di sicurezza che ha bloccato la connettività. FPHC verifica quindi se esiste un'estensione della classe helper per quel provider. Se ne viene trovato uno, FPHC genera un'ipotesi per quel provider, quindi NDF richiama l'estensione. L'estensione deve restituire all'utente informazioni utili di diagnostica e ripristino.

## <a name="helper-class-registration"></a>Registrazione della classe helper

È necessario registrare un'estensione FPHC, come descritto in [registrare le estensioni della classe helper NDF](registering-ndf-helper-class-extensions.md). Gli sviluppatori che implementano una classe helper devono registrare le proprie estensioni per assicurarsi che l'estensione venga chiamata da NDF quando appropriato. L' *attributo corrispondente* descritto di seguito deve essere archiviato nel registro di **sistema in HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper Class dll* \\ **HelperClasses** \\ *Helper Class Name* \\ **MatchAttributes**.

La tabella seguente illustra l'attributo corrispondente usato per identificare l'ipotesi da usare nella diagnostica nel registro eventi di WFP. 

| Nome       | Tipo    | Descrizione                                                                                                                                                                                                                                                                                                 |
|------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProviderID | REG \_ SZ | GUID dell'estensione FPHC. Questo valore deve corrispondere al GUID del provider WFP. <br/> Questa stringa distingue tra maiuscole e minuscole. Deve essere archiviato nel registro di sistema in lettere maiuscole con parentesi graffe e trattini di inclusione. Ad esempio, {C200E360-38C5-11CE-AE62-08002B2B79EF} è un ProviderID valido.<br/> |



 

Quando il ProviderID di un filtro di blocco corrisponde a quello di una classe helper registrata, FPHC informa NDF per richiamare tale classe helper, estendendo in tal modo la funzionalità di diagnostica di FPHC.

## <a name="fphc-event-attributes"></a>Attributi dell'evento FPHC

Nella tabella seguente sono elencati gli attributi degli eventi associati a ogni evento corrispondente. Ogni attributo dell'evento viene archiviato in una struttura di [**\_ attributi Helper**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) . Questi attributi vengono passati da NDF a FPHC quando viene trovato un evento corrispondente. Questi possono a loro volta essere passati alle estensioni FPHC.



| Attributo     | [**Attributo \_ Valore tipo**](/windows/win32/api/ndattrib/ne-ndattrib-attribute_type) | Descrizione                                                                                                                               |
|---------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| GUID del provider | AL \_ GUID                                        | GUID del provider associato al filtro.                                                                                      |
| Timestamp     | \_stringa a ottetto \_                               | Buffer di tipo FILETIME che specifica l'ora in cui si è verificato l'evento. Questo timestamp può essere usato per identificare in modo univoco un evento. |
| ipProtocol    | A \_ UInt32                                      | Protocollo del livello di trasporto, in formato UINT8.                                                                                            |
| LocalAddr     | ALLE \_ sockaddr                                    | Indirizzo IP locale e porta, archiviati in una struttura [**\_ sockaddr di Diag**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr) .                                             |
| IndirizzoRemoto    | ALLE \_ sockaddr                                    | Indirizzo IP remoto e porta, archiviati in una struttura [**\_ sockaddr diag**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr) .                                            |
| userId        | \_stringa a ottetto \_                               | Buffer di tipo SID che rappresenta l'ID utente. Se userId è di lunghezza 0, il SID non è disponibile.                                        |
| appId         | in corrispondenza della \_ stringa                                      | Buffer che archivia l'identificatore dell'applicazione recuperato. Se appId ha un valore di L "", l'identificatore dell'applicazione non è disponibile.        |



 

## <a name="handling-fphc-events"></a>Gestione degli eventi FPHC

Prima di suggerire le informazioni di diagnostica e ripristino all'utente, un'estensione FPHC dovrebbe raccogliere più dati rispetto a quelli forniti dalle notifiche FPHC. Questi dati possono essere acquisiti dalle [funzioni di gestione degli eventi di WFP](/windows/desktop/FWP/fwp-mgmt-functions). Queste funzioni vengono illustrate nell'esempio [visualizzazione di eventi NET](/windows/desktop/FWP/displaying-net-events) .

Nell'SDK è incluso un esempio di gestione di eventi più dettagliato. Il codice sorgente per l'esempio è disponibile nel percorso di installazione di SDK in C: \\ programmi \\ Microsoft SDK \\ Windows \\ <version number> \\ Samples \\ NetDs \\ WFP \\ DiagEvents. Windows Vista SDK è disponibile nell' [area download](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).

## <a name="built-in-fphc-diagnostics"></a>Diagnostica FPHC incorporata

In assenza di un'estensione FPHC, FPHC è in grado di diagnosticare gli scenari elencati di seguito. La maggior parte degli errori di connettività diagnosticati da FPHC si verifica perché i firewall bloccano il traffico. Gli scenari IPsec sono meno comuni.

La tabella seguente illustra alcuni scenari che causano errori di connettività che possono essere diagnosticati da FPHC, oltre alla descrizione e alle informazioni di ripristino passate a NDF.



| Scenario                   | Descrizione di basso livello di integrità                                                                                                               | Informazioni di ripristino                   |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Eliminazione del firewall              | Le impostazioni del firewall nel computer bloccano la connessione.                                                                  | Verificare le impostazioni del firewall.       |
| Errore in modalità principale          | Non è possibile connettersi a causa di una mancata corrispondenza dei criteri di sicurezza IPsec.                                                                     | Contattare il proprietario del criterio IPsec.      |
| Errore in modalità rapida         | Non è possibile connettersi a causa di una mancata corrispondenza dei criteri di sicurezza IPsec.                                                                     | Contattare il proprietario del criterio IPsec.      |
| Errore della modalità utente          | Non è possibile connettersi a causa di una mancata corrispondenza dei criteri di sicurezza IPsec.                                                                     | Contattare il proprietario del criterio IPsec.      |
| Errore delle credenziali         | Non è possibile connettersi perché l'autorità di certificazione radice (CA) del computer non corrisponde alla CA radice nel computer remoto. | Aggiornare il certificato radice attendibile. |
| Certificato scaduto        | Il certificato utilizzato per l'autenticazione IPsec è scaduto.                                                                           | Richiedere un certificato.               |
| Altri errori relativi ai certificati | Impossibile trovare un certificato valido per l'autenticazione IPsec.                                                                          | Richiedere un certificato.               |
| Errore Kerberos           | Il computer non fa parte di questo dominio.                                                                                             | Aggiungere il computer a un dominio.      |
| Chiave precondivisa              | Reimpostare le chiavi già condivise.                                                                                                            | Reimpostare le chiavi già condivise.            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Piattaforma filtro Windows](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Progettazione di estensioni di classe helper NDF](designing-ndf-helper-class-extensions.md)
</dt> <dt>

[Registrazione delle estensioni di classe helper NDF](registering-ndf-helper-class-extensions.md)
</dt> <dt>

[Esempi di classi helper NDF](ndf-helper-class-examples.md)
</dt> </dl>

 

