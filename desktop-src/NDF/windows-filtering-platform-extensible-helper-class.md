---
title: Windows Classe helper Estendibile della piattaforma di filtro
description: La Windows filtering platform (WFP) include una classe helper Framework di diagnostica di rete (NDF), denominata classe helper della piattaforma di filtro (FPHC).
ms.assetid: 006ea30c-8682-4a3d-803a-73dba5162696
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff972beffebb44b33eb68a0439193307639522738ac1f8766845404c03d3cd9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065211"
---
# <a name="windows-filtering-platform-extensible-helper-class"></a>Windows Classe helper Estendibile della piattaforma di filtro

La [Windows filtering platform (WFP)](/windows/desktop/FWP/windows-filtering-platform-start-page) include una classe helper Framework di diagnostica di rete (NDF), denominata classe helper della piattaforma di filtro (FPHC). FPHC consente di identificare le cause principali dei problemi di connettività causati da WFP. Gli sviluppatori di firewall di terze parti possono implementare le proprie classi helper NDF. L'estendibilità FPHC consente di richiamare queste classi helper di terze parti durante la diagnostica.

Questo argomento presuppone una certa familiarità con [l'API WFP](/windows/desktop/FWP/windows-filtering-platform-start-page).

## <a name="why-extend-the-fphc"></a>Perché estendere il file FPHC?

Tutti gli sviluppatori che scrivono applicazioni che chiamano l'API PAM devono scrivere una classe helper NDF che estende FPHC.

FPHC può identificare WFP come causa di un problema di connettività. Se disponibile, FPHC può anche identificare il provider che ha creato il filtro che blocca il traffico di rete. FPHC passa queste informazioni alla funzione NDF, che a sua volta può notificare all'utente che il firewall sta causando il problema di connettività e assegnare il nome del provider che blocca il traffico.

Tuttavia, il filtro FPHC non può suggerire un'azione correttiva all'utente, né può fornire il motivo per cui il filtro blocca il traffico verso l'utente. Solo un'estensione FPHC può eseguire queste attività.

Si consideri un'applicazione firewall di terze parti che chiama l'API WFP. Se il firewall di terze parti implementa un'estensione FPHC, è possibile implementare azioni personalizzate per gestire i problemi di connettività identificati da NDF. Quando NDF diagnostica che un'applicazione è stata bloccata dal firewall di terze parti, l'estensione FPHC può gestire l'evento di blocco. Un modo in cui l'estensione FPHC può gestire un evento è presentare all'utente una richiesta di sbloccare un programma usando il firewall e quindi sbloccare il programma al momento della conferma dell'utente. In alternativa, l'estensione FPHC può gestire un evento notificando all'utente il motivo per cui l'applicazione è stata bloccata, ad esempio un'applicazione è stata bloccata perché è stata considerata malware dal firewall.

## <a name="about-wfp-diagnostics"></a>Informazioni sulla diagnostica DI WINDOWS Server

Quando viene richiamata la funzione NDF per diagnosticare un problema di rete, vengono contattate le classi helper per determinare la causa del problema. Se una classe helper di livello superiore determina che un errore di rete può essere causato da WFP, genera un'ipotesi per FPHC in base alle informazioni disponibili. La funzione definita dall'utente passa questa ipotesi, sotto forma di diversi attributi di evento, a FPHC. Questi attributi sono descritti in dettaglio nella sezione [Attributi evento FPHC riportata](#windows-filtering-platform-extensible-helper-class) di seguito.

Un problema di rete può essere descritto come un problema di connettività che interessa un particolare tentativo di connessione. Ad esempio, l'utente potrebbe aver accidentalmente bloccato **un'applicazione** facendo clic inavvertitamente su Non consentire . Il firewall blocca quindi l'associazione dell'applicazione a qualsiasi porta. L'utente, non conoscendo il motivo per cui l'applicazione è bloccata, può provare a diagnosticare il problema tramite un punto di ingresso offerto dall'applicazione. FPHC guarderà i log e, se trova una corrispondenza, recupererà l'ID filtro e l'ID provider del filtro specifico. A questo punto, FPHC conosce il proprietario del filtro e consegna il processo di diagnostica alla classe helper appropriata per un'ulteriore diagnosi.

L'evento più recente nei registri eventi WFP per la corrispondenza con gli attributi viene selezionato come rilevante per il problema di rete. Se non viene trovato alcun evento corrispondente e l'ora in cui si è verificato l'evento è coperta nel log DI WINDOWS, FPHC indica a NDF che è integro. Se non vengono trovati eventi corrispondenti e i log di PAM non includono l'ora in cui si è verificato l'evento, FPHC restituisce uno stato indeterminato a NDF.

Se viene trovato un evento corrispondente, FPHC usa l'ID provider del filtro che ha causato l'identificazione del provider della regola di sicurezza che ha bloccato la connettività. FPHC controlla quindi se esiste un'estensione della classe helper per tale provider. Se ne viene trovato uno, FPHC genera un'ipotesi per il provider e quindi NDF richiama l'estensione. L'estensione deve restituire informazioni di diagnostica e ripristino utili all'utente.

## <a name="helper-class-registration"></a>Registrazione della classe helper

Un'estensione FPHC deve essere registrata come descritto in [Registrazione delle estensioni della classe helper NDF.](registering-ndf-helper-class-extensions.md) Gli sviluppatori che implementano una classe helper devono registrare le estensioni per assicurarsi che l'estensione sia chiamata da NDF quando appropriato. L'attributo corrispondente descritto di seguito deve essere archiviato nel Registro di sistema in **HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx**  \\ *VendorName* \\ **HostDLLs** \\ *Helper Class HelperClasses* Helper Class \\  \\ *Name* \\ **MatchAttributes**.

La tabella seguente mostra l'attributo corrispondente usato per identificare l'ipotesi da usare nella diagnostica nel registro eventi DI WINDOWS. 

| Nome       | Tipo    | Descrizione                                                                                                                                                                                                                                                                                                 |
|------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProviderID | REG \_ SZ | GUID dell'estensione FPHC. Questo valore deve essere lo stesso del GUID del provider PAM. <br/> Questa stringa fa distinzione tra maiuscole e minuscole. Deve essere archiviato nel Registro di sistema in lettere maiuscole, racchiudendo parentesi graffe e trattini. Ad esempio, {C200E360-38C5-11CE-AE62-08002B2B79EF} è un ProviderID valido.<br/> |



 

Quando il ProviderID di un filtro di blocco corrisponde a quello di una classe helper registrata, FPHC informa NDF di richiamare tale classe helper, estendendo così la funzionalità di diagnostica di FPHC.

## <a name="fphc-event-attributes"></a>Attributi dell'evento FPHC

Nella tabella seguente sono elencati gli attributi degli eventi associati a ogni evento corrispondente. Ogni attributo dell'evento viene archiviato in una [**struttura HELPER \_ ATTRIBUTE.**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) Questi attributi vengono passati da NDF a FPHC quando viene trovato un evento corrispondente. Questi possono a loro volta essere passati alle estensioni FPHC.



| Attributo     | [**ATTRIBUTE \_ Valore TYPE**](/windows/win32/api/ndattrib/ne-ndattrib-attribute_type) | Descrizione                                                                                                                               |
|---------------|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| GUID del provider | AT \_ GUID                                        | GUID del provider associato al filtro.                                                                                      |
| Timestamp     | AT \_ OCTET \_ STRING                               | Buffer di tipo FILETIME che specifica l'ora in cui si è verificato l'evento. Questo timestamp può essere usato per identificare in modo univoco un evento. |
| ipProtocol    | AT \_ UINT32                                      | Protocollo del livello di trasporto, in formato UINT8.                                                                                            |
| LocalAddr     | AT \_ SOCKADDR                                    | Indirizzo IP locale e porta, archiviati in una [**struttura \_ DIAG SOCKADDR.**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr)                                             |
| RemoteAddr    | AT \_ SOCKADDR                                    | Indirizzo IP remoto e porta, archiviati in una [**struttura \_ DIAG SOCKADDR.**](/windows/win32/api/ndattrib/ns-ndattrib-diag_sockaddr)                                            |
| userId        | AT \_ OCTET \_ STRING                               | Buffer di tipo SID che rappresenta l'ID utente. Se userId è di lunghezza 0, il SID non è disponibile.                                        |
| appId         | AT \_ STRING                                      | Buffer in cui è archiviato l'identificatore dell'applicazione recuperato. Se appId ha il valore L"", l'identificatore dell'applicazione non è disponibile.        |



 

## <a name="handling-fphc-events"></a>Gestione degli eventi FPHC

Prima di suggerire informazioni di diagnostica e ripristino all'utente, un'estensione FPHC deve raccogliere più dati di quelli forniti dalle notifiche FPHC. Questi dati possono essere acquisiti dalle funzioni [di gestione degli eventi WFP.](/windows/desktop/FWP/fwp-mgmt-functions) Queste funzioni sono illustrate [nell'esempio di visualizzazione di eventi netti.](/windows/desktop/FWP/displaying-net-events)

Un esempio di gestione degli eventi più dettagliato è incluso nell'SDK. Il codice sorgente per l'esempio è disponibile nel percorso di installazione dell'SDK in C: Programmi \\ \\ Microsoft SDKs \\ Windows Samples \\ <version number> \\ \\ NetDs WFP \\ \\ DiagEvents. L Windows Vista SDK è disponibile [nell'Area download](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf).

## <a name="built-in-fphc-diagnostics"></a>Diagnostica FPHC incorporata

In assenza di un'estensione FPHC, FPHC può diagnosticare gli scenari elencati di seguito. La maggior parte degli errori di connettività diagnosticati da FPHC si verifica perché i firewall bloccano il traffico. Gli scenari IPsec sono meno comuni.

La tabella seguente illustra alcuni scenari che causano errori di connettività che possono essere diagnosticati da FPHC, insieme alla descrizione e alle informazioni di ripristino passate a NDF.



| Scenario                   | Descrizione dell'integrità insufficiente                                                                                                               | Informazioni di ripristino                   |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Eliminazione del firewall              | Le impostazioni del firewall in questo computer bloccano la connessione.                                                                  | Verificare le impostazioni del firewall.       |
| Errore in modalità principale          | Non è possibile connettersi a causa di un criterio di sicurezza IPsec non corrispondente.                                                                     | Contattare il proprietario dei criteri IPsec.      |
| Errore in modalità rapida         | Non è possibile connettersi a causa di un criterio di sicurezza IPsec non corrispondente.                                                                     | Contattare il proprietario dei criteri IPsec.      |
| Errore in modalità utente          | Non è possibile connettersi a causa di un criterio di sicurezza IPsec non corrispondente.                                                                     | Contattare il proprietario dei criteri IPsec.      |
| Errore delle credenziali         | Non è possibile connettersi perché l'autorità di certificazione radice (CA) nel computer non corrisponde alla CA radice nel computer remoto. | Aggiornare il certificato radice attendibile. |
| Certificato scaduto        | Il certificato usato per l'autenticazione IPsec è scaduto.                                                                           | Richiedere un certificato.               |
| Altri errori di certificato | Non è stato trovato un certificato valido per l'autenticazione IPsec.                                                                          | Richiedere un certificato.               |
| Errore Kerberos           | Il computer non fa parte di questo dominio.                                                                                             | Aggiungere il computer a un dominio.      |
| Chiave precondivisa              | Reimpostare le chiavi precondivise.                                                                                                            | Reimpostare le chiavi precondivise.            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Piattaforma filtro Windows](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[Progettazione di estensioni della classe helper NDF](designing-ndf-helper-class-extensions.md)
</dt> <dt>

[Registrazione delle estensioni della classe helper NDF](registering-ndf-helper-class-extensions.md)
</dt> <dt>

[Esempi di classi helper NDF](ndf-helper-class-examples.md)
</dt> </dl>

 

