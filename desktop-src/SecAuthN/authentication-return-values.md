---
description: Elenca i valori restituiti dalle funzioni nelle API di autenticazione.
ms.assetid: ea519e5c-98b0-4a01-b2cc-e5ff736a5396
title: Valori restituiti di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2831fbce55523b3d55a649ef18fb6a622f3ec0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050246"
---
# <a name="authentication-return-values"></a>Valori restituiti di autenticazione

## <a name="network-provider-values"></a>Valori del provider di rete

L' [API del provider di rete](network-provider-api.md) usa i valori definiti seguenti.



| Valore                                                                           | Descrizione                                               |
|---------------------------------------------------------------------------------|-----------------------------------------------------------|
| [Valori restituiti dalla sicurezza di rete](network-security-return-values.md)<br/> | Valori restituiti che possono essere impostati da un provider di rete.<br/> |



 

## <a name="smart-card-return-values"></a>Valori restituiti da Smart Card

Le [funzioni Smart Card](authentication-functions.md) restituiscono i valori restituiti seguenti. Questi valori restituiti sono definiti in Scarderr. h.

> [!Note]  
> Alcuni valori restituiti possono avere lo stesso valore dei valori restituiti di Windows esistenti che indicano una condizione simile. Per informazioni sui codici di errore non elencati qui, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

 



| Valore                                                               | Descrizione                                                                                                                                                                                                 |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRORE \_ con \_ pipe interrotta<br/> 0x00000109<br/>                | Il client ha tentato un'operazione di smart card in una sessione remota, ad esempio una sessione client in esecuzione in un server terminal, e il sistema operativo in uso non supporta il reindirizzamento delle smart card.<br/> |
| \_ \_ ricerca errata E non valida \_<br/> 0x80100029<br/>                | Si è verificato un errore durante l'impostazione del puntatore all'oggetto file della smart card.<br/>                                                                                                                                 |
| \_ \_ cancellato E annullato<br/> 0x80100002<br/>                | L'azione è stata annullata da una richiesta [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel) .<br/>                                                                                                                        |
| Dispose non riuscita \_ E \_ cant \_<br/> 0x8010000E<br/>            | Il sistema non è stato in grado di eliminare i supporti nel modo richiesto.<br/>                                                                                                                               |
| Smart \_ card E \_ scheda non \_ supportata<br/> 0x8010001C<br/>        | La smart card non soddisfa i requisiti minimi per il supporto.<br/>                                                                                                                                   |
| certificato spaventato \_ E \_ non \_ disponibile<br/> 0x8010002D<br/> | Non è stato possibile ottenere il certificato richiesto.<br/>                                                                                                                                                 |
| perdita di \_ \_ dati E \_ comunicazione \_<br/> 0x8010002F<br/>         | È stato rilevato un errore di comunicazione con la smart card. <br/>                                                                                                                                   |
| \_ \_ dir E dir \_ non \_ trovato<br/> 0x80100023<br/>          | La directory specificata non esiste nella smart card.<br/>                                                                                                                                        |
| \_ \_ lettore duplicato E duplicato \_<br/> 0x8010001B<br/>        | Il driver del [*lettore*](/windows/desktop/SecGloss/r-gly) non ha generato un nome univoco del lettore.<br/>                                                                            |
| il \_ file E \_ non è stato \_ \_ trovato<br/> 0x80100024<br/>         | Il file specificato non esiste nella smart card.<br/>                                                                                                                                             |
| \_ \_ CREATEORDER E ICC \_<br/> 0x80100021<br/>         | L'ordine richiesto per la creazione di oggetti non è supportato.<br/>                                                                                                                                         |
| installazione di \_ \_ ICC E \_<br/> 0x80100020<br/>        | Non è possibile trovare alcun provider primario per la smart card.<br/>                                                                                                                                             |
| \_ \_ buffer insufficiente E insufficiente \_<br/> 0x80100008<br/>     | Il buffer dei dati per i dati restituiti è troppo piccolo per i dati restituiti.<br/>                                                                                                                            |
| \_ \_ ATR non valido E non valido \_<br/> 0x80100015<br/>             | Una [*stringa ATR*](/windows/desktop/SecGloss/a-gly) ottenuta dal registro di sistema non è una stringa ATR valida.<br/>                                                        |
| \_ \_ CHV non valido E non valido \_<br/> 0x8010002A<br/>             | Il PIN specificato non è corretto.<br/>                                                                                                                                                                   |
| \_ \_ handle non valido E non valido \_<br/> 0x80100003<br/>          | Handle fornito non valido.<br/>                                                                                                                                                               |
| parametro spaventato \_ E \_ non valido \_<br/> 0x80100004<br/>       | Non è stato possibile interpretare correttamente uno o più parametri forniti.<br/>                                                                                                                        |
| \_ \_ destinazione non valida E non valida \_<br/> 0x80100005<br/>          | Informazioni di avvio del registro di sistema mancanti o non valide.<br/>                                                                                                                                            |
| \_ \_ valore non valido E non valido \_<br/> 0x80100011<br/>           | Non è stato possibile interpretare correttamente uno o più valori di parametro forniti.<br/>                                                                                                                  |
| \_ \_ Nessun accesso spaventato E \_<br/> 0x80100027<br/>               | Accesso negato al file.<br/>                                                                                                                                                                    |
| DIR spaventato \_ E \_ Nessuna \_ dir<br/> 0x80100025<br/>                  | Il percorso specificato non rappresenta una directory della smart card.<br/>                                                                                                                                     |
| \_ \_ nessun \_ file spaventato<br/> 0x80100026<br/>                 | Il percorso specificato non rappresenta un file di smart card.<br/>                                                                                                                                          |
| \_ \_ nessun \_ contenitore di chiavi \_ spaventato E<br/> 0x80100030<br/>       | Il contenitore di chiavi richiesto non esiste nella smart card.<br/>                                                                                                                                    |
| \_ \_ \_ memoria E memoria insufficiente<br/> 0x80100006<br/>               | Memoria disponibile insufficiente per completare il comando.<br/>                                                                                                                                            |
| \_ \_ cache E senza \_ pin \_<br/> 0x80100033<br/>           | Il PIN della smart card non può essere memorizzato nella cache.<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo codice di errore non è disponibile.<br/> <br/>                        |
| Nessun lettore è stato spaventato \_ E \_ \_ \_ disponibile<br/> 0x8010002E<br/>   | Nessun lettore di smart card disponibile.<br/>                                                                                                                                                               |
| \_E \_ nessun \_ servizio<br/> 0x8010001D<br/>              | Il gestore di [*risorse*](/windows/desktop/SecGloss/r-gly) della smart card non è in esecuzione.<br/>                                                                |
| \_E \_ Nessuna \_ Smart Card<br/> 0x8010000C<br/>            | Per l'operazione è necessaria una smart card, ma non è attualmente disponibile alcuna smart card nel dispositivo.<br/>                                                                                                               |
| il \_ \_ \_ \_ certificato non è stato spaventato<br/> 0x8010002C<br/>    | Il certificato richiesto non esiste.<br/>                                                                                                                                                        |
| SPAVENTATO \_ E \_ non \_ pronto<br/> 0x80100010<br/>               | Il lettore o la scheda non è pronta per accettare i comandi.<br/>                                                                                                                                              |
| E non sottoposto a \_ \_ \_ transazione<br/> 0x80100016<br/>          | È stato effettuato un tentativo di terminare una transazione inesistente.<br/>                                                                                                                                            |
| SCARd \_ E \_ PCI \_ troppo \_ piccolo<br/> 0x80100019<br/>          | Il buffer di ricezione PCI è troppo piccolo.<br/>                                                                                                                                                            |
| la \_ cache del PIN E l'allarme sono \_ \_ \_ scaduti<br/> 0x80100032<br/>      | La cache del PIN della smart card è scaduta.<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo codice di errore non è disponibile.<br/> <br/>                       |
| \_ \_ MANCAta corrispondenza del proto E proto \_<br/> 0x8010000F<br/>          | I protocolli richiesti non sono compatibili con il protocollo attualmente in uso con la scheda.<br/>                                                                                                       |
| scheda di \_ sola \_ lettura \_ E con cicatrice \_<br/> 0x80100034<br/>         | La smart card è di sola lettura e non è possibile scrivervi.<br/> **Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Questo codice di errore non è disponibile.<br/> <br/>       |
| lettore spaventato \_ E \_ non \_ disponibile<br/> 0x80100017<br/>      | Il lettore specificato non è attualmente disponibile per l'utilizzo.<br/>                                                                                                                                         |
| lettore spaventato \_ E \_ lettore non \_ supportato<br/> 0x8010001A<br/>      | Il driver del lettore non soddisfa i requisiti minimi per il supporto.<br/>                                                                                                                                |
| Server spaventato \_ E \_ \_ troppo \_ occupato<br/> 0x80100031<br/>        | Il gestore di risorse della smart card è troppo occupato per completare questa operazione.<br/>                                                                                                                          |
| servizio spaventato \_ E \_ \_ arrestato<br/> 0x8010001E<br/>         | Il gestore di risorse della smart card è stato arrestato.<br/>                                                                                                                                                   |
| violazione della \_ \_ condivisione E \_<br/> 0x8010000B<br/>       | Non è possibile accedere alla smart card a causa di altre connessioni in attesa.<br/>                                                                                                                      |
| sistema eliminato \_ E \_ \_ annullato<br/> 0x80100012<br/>        | L'azione è stata annullata dal sistema, presumibilmente disconnettersi o arrestarsi.<br/>                                                                                                                       |
| TIMEOUT di \_ E \_<br/> 0x8010000A<br/>                  | Il valore di timeout specificato dall'utente è scaduto.<br/>                                                                                                                                                   |
| SPAVENTATO \_ E \_ imprevisto<br/> 0x8010001F<br/>               | Si è verificato un errore imprevisto della scheda.<br/>                                                                                                                                                           |
| \_ \_ scheda sconosciuta E sconosciuta \_<br/> 0x8010000D<br/>            | Il nome della smart card specificato non è stato riconosciuto.<br/>                                                                                                                                                 |
| lettore spaventato \_ E \_ sconosciuto \_<br/> 0x80100009<br/>          | Il nome del lettore specificato non è riconosciuto.<br/>                                                                                                                                                     |
| SCARd \_ E \_ \_ MNG res \_ sconosciuti<br/> 0x8010002B<br/>        | È stato restituito un codice di errore non riconosciuto.<br/>                                                                                                                                                         |
| funzionalità non \_ supportata E non \_ supportata \_<br/> 0x80100022<br/>     | Questa smart card non supporta la funzionalità richiesta.<br/>                                                                                                                                          |
| \_E \_ scrittura \_ troppe \_<br/> 0x80100028<br/>         | È stato effettuato un tentativo di scrittura di più dati rispetto all'oggetto di destinazione.<br/>                                                                                                                      |
| \_ \_ errore F comm \_ spaventato<br/> 0x80100013<br/>              | È stato rilevato un errore interno di comunicazione.<br/>                                                                                                                                              |
| \_ \_ errore interno F spaventato \_<br/> 0x80100001<br/>          | Verifica coerenza interna non riuscita.<br/>                                                                                                                                                            |
| \_ \_ errore sconosciuto F \_<br/> 0x80100014<br/>           | È stato rilevato un errore interno, ma l'origine è sconosciuta.<br/>                                                                                                                                  |
| F spaventato \_ \_ troppo a \_ \_ lungo<br/> 0x80100007<br/>        | Un timer di coerenza interno è scaduto.<br/>                                                                                                                                                       |
| \_arresto P spaventato \_<br/> 0x80100018<br/>                 | L'operazione è stata interrotta per consentire la chiusura dell'applicazione server.<br/>                                                                                                                          |
| \_ \_ esito negativo<br/>                                        | Nessun errore riscontrato.<br/>                                                                                                                                                                        |
| \_W \_ annullato \_ dall' \_ utente<br/> 0x8010006E<br/>      | L'azione è stata annullata dall'utente.<br/>                                                                                                                                                             |
| non è \_ stato \_ trovato alcun elemento della cache \_ \_ spaventato \_<br/> 0x80100070<br/>  | L'elemento richiesto non è stato trovato nella cache.<br/>                                                                                                                                              |
| \_ \_ elemento della cache non \_ \_ aggiornato<br/> 0x80100071<br/>       | L'elemento della cache richiesto è troppo vecchio ed è stato eliminato dalla cache.<br/>                                                                                                                              |
| \_ \_ \_ troppa voce della cache \_ impaurita \_<br/> 0x80100072<br/>    | Il nuovo elemento della cache supera le dimensioni massime per singolo elemento definite per la cache.<br/>                                                                                                                      |
| scheda con \_ W \_ spaventato \_ non \_ autenticata<br/> 0x8010006F<br/> | Nessun PIN presentato alla smart card.<br/>                                                                                                                                                          |
| il \_ CHV è \_ stato \_ bloccato<br/> 0x8010006C<br/>             | Non è possibile accedere alla scheda perché è stato raggiunto il numero massimo di tentativi di immissione del PIN.<br/>                                                                                                   |
| SPAVENTATO \_ W \_ EOF<br/> 0x8010006D<br/>                      | È stata raggiunta la fine del file della smart card.<br/>                                                                                                                                                 |
| \_ \_ scheda rimossa da \_ W<br/> 0x80100069<br/>            | La smart card è stata rimossa, quindi non è possibile continuare la comunicazione.<br/>                                                                                                                       |
| scheda di \_ \_ ripristino con cicatrice \_<br/> 0x80100068<br/>              | La smart card è stata reimpostata.<br/>                                                                                                                                                                        |
| violazione della \_ \_ sicurezza W \_<br/> 0x8010006A<br/>      | L'accesso è stato negato a causa di una violazione della sicurezza.<br/>                                                                                                                                               |
| Smart \_ Card non \_ alimentata \_<br/> 0x80100067<br/>          | La funzionalità Power è stata rimossa dalla smart card, in modo che non sia possibile ulteriori comunicazioni.<br/>                                                                                                       |
| Smart \_ card senza \_ risposta \_<br/> 0x80100066<br/>       | La smart card non risponde a una reimpostazione.<br/>                                                                                                                                                     |
| scheda non \_ \_ supportata W \_<br/> 0x80100065<br/>        | Il lettore non è in grado di comunicare con la scheda, a causa di conflitti di configurazione di stringa ATR.<br/>                                                                                                          |
| \_ \_ CHV non corretto \_<br/> 0x8010006B<br/>               | Non è possibile accedere alla scheda perché è stato presentato un PIN errato.<br/>                                                                                                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codici di errore di sistema](/windows/desktop/Debug/system-error-codes)
</dt> </dl>

 

