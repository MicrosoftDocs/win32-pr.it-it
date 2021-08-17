---
description: Le informazioni principali fornite da un'applicazione per avviare una sessione di comunicazione sono il tipo di indirizzo, il tipo o i tipi di supporto e l'indirizzo di destinazione.
ms.assetid: 65e53587-0e40-411b-8d6c-d6adfc9d1e6c
title: Avviare una sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0226fc1b04ea5859bc4a96b6f5ca43e3749e7664a9ccf6810b586115171530b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975851"
---
# <a name="initiate-a-session"></a>Avviare una sessione

Le informazioni principali fornite da un'applicazione per avviare una [](media-type-ovr.md) sessione di comunicazione sono il tipo di indirizzo [,](address-type-ovr.md)il tipo o i tipi di supporto e l'indirizzo [di destinazione](address-ovr.md).

L'indirizzo di destinazione può [richiedere la conversione](#address-translation) dell'indirizzo per inserire le informazioni immesse da un utente nel formato corretto per un determinato tipo di indirizzo. Ad esempio, un numero di telefono in una rubrica elettronica in [formato canonico](address-ovr.md) richiederà la traduzione [in formato dialable.](address-ovr.md)

Alcune sessioni possono richiedere parametri di configurazione speciali, se supportati dal provider di servizi. Ad esempio, un provider di servizi di streaming ISDN può trasmettere informazioni utente-utente e alcuni PROVIDER richiedono informazioni sulla direzione del flusso multimediale. Per una [verifica dei](session-information-ovr.md) dati che possono essere impostati o ottenuti in relazione a una sessione, vedere Informazioni sulla sessione.

Dopo l'avvio di una sessione, TAPI informerà l'applicazione dello stato di avanzamento delle chiamate usando il meccanismo di notifica degli eventi configurato durante l'inizializzazione.

**TAPI 2.x:** Le applicazioni avviano una sessione usando [**la funzione lineMakeCall.**](/windows/win32/api/tapi/nf-tapi-linemakecall) La [**funzione lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) viene usata per eseguire la conversione degli indirizzi, se necessario.

I parametri di impostazione delle chiamate possono essere archiviati nella struttura di dati [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams) e un puntatore a questa struttura viene quindi usato come parametro [**di lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall). Se a **lineMakeCall** non viene fornita alcuna struttura **LINECALLPARAMS** , viene richiesta una chiamata di livello vocale POTS predefinita con un set di valori predefiniti.

Se la sessione è stata impostata  [](privilege-ovr.md) correttamente, all'applicazione viene restituito un handle di chiamata con privilegi di proprietario e TAPI invia all'applicazione messaggi [**LINE \_ CALLSTATE**](./line-callstate.md) con informazioni relative all'avanzamento della chiamata. Le applicazioni in genere usano questi messaggi per visualizzare i report di stato per l'utente.

**TAPI 3.x:** Le applicazioni avviano una sessione di comunicazione richiamando il [**metodo ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) su un indirizzo in grado di gestire il tipo di indirizzo e il tipo di supporto necessari. Se l'indirizzo espone [**l'interfaccia ITTerminalSupport,**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) i terminali vengono selezionati nei flussi multimediali dell'oggetto chiamata. Vedere [l'esempio di codice Make a Call](make-a-call.md) per un'illustrazione di questo processo.

I parametri di configurazione delle chiamate possono essere archiviati o modificati usando i metodi esposti [**dall'interfaccia ITCallInfo.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)

Se la sessione è stata impostata correttamente, TAPI restituisce un puntatore a interfaccia [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) che può essere usato per altre operazioni di sessione o per ottenere un puntatore a interfaccia [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) che può essere usato per acquisire informazioni aggiuntive sulla sessione. [**L'interfaccia ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) elabora gli eventi di stato delle chiamate TAPI.

> [!Note]  
> TapI non deve essere usato per le trasmissioni fax. Usare invece le funzioni disponibili tramite MAPI, l'API Microsoft Messaggi.

 

## <a name="address-translation"></a>Conversione degli indirizzi

Un'applicazione server o utente finale può archiviare gli indirizzi in un formato non compatibile con le esigenze di un determinato provider di servizi. Ad esempio, un numero di telefono può essere archiviato in una rubrica elettronica in [formato canonico,](address-ovr.md)ma la maggior parte dei provider di servizi che gestiscono i numeri di telefono richiede [il formato dialable](address-ovr.md).

TAPI fornisce operazioni di conversione degli indirizzi che assiste un'applicazione nella presentazione del tipo di indirizzo corretto a un provider di servizi di configurazione. Il provider di servizi specifica a TAPI quali tipi di indirizzi supporta e non deve includere alcuna forma di conversione degli indirizzi.

**TAPI 2.x:** Vedere [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress).

**TAPI 3:** Vedere [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation), [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo).

## <a name="toll-lists"></a>Elenchi di pedaggi

In alcune località America del Nord, tutte le chiamate telefoniche effettuate al codice locale sono chiamate locali. In altre località, alcune chiamate effettuate al prefisso locale sono a lunga distanza e necessitano di un prefisso "1" da comporre. Le prime tre cifre dell'indirizzo (prefisso) determinano se una chiamata all'interno del prefisso locale è una chiamata a pedaggio.

Un *elenco di pedaggi* è un elenco di prefissi nel prefisso locale i cui indirizzi devono essere digitati come indirizzi a lunga distanza e vengono valutati gli addebiti per le lunghe distanze.

Gli elenchi di pedaggi non sono rilevanti per i provider di servizi o per le applicazioni che non accedono a una rete telefonica.

**TAPI 2.x:** Vedere i bit [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) (LINETRANSLATERESULT \_ INTOLLLIST e LINETRANSLATERESULT \_ NOTINTOLLLIST nella struttura [**LINETRANSLATEOUTPUT),**](/windows/win32/api/tapi/ns-tapi-linetranslateoutput) [**lineSetTollList**](/windows/win32/api/tapi/nf-tapi-linesettolllist).

**TAPI 3:** Vedere [**ITAddressTranslation::TranslateAddress**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-translateaddress), [**ITAddressTranslationInfo::get \_ TranslationResults**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslationinfo-get_translationresults).

 

 
