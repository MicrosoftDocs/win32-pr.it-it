---
description: Le informazioni principali fornite da un'applicazione per avviare una sessione di comunicazione sono il tipo di indirizzo, il tipo di supporto o i tipi e l'indirizzo di destinazione.
ms.assetid: 65e53587-0e40-411b-8d6c-d6adfc9d1e6c
title: Avviare una sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e925ba90460b88c85a9aab1624923acdbc4572a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880501"
---
# <a name="initiate-a-session"></a>Avviare una sessione

Le informazioni principali fornite da un'applicazione per avviare una sessione di comunicazione sono il [tipo di indirizzo](address-type-ovr.md), il [tipo di supporto](media-type-ovr.md) o i tipi e l' [Indirizzo](address-ovr.md)di destinazione.

È possibile che l'indirizzo di destinazione richieda la [conversione degli indirizzi](#address-translation) per inserire le informazioni immesse da un utente nel formato corretto per un tipo di indirizzo specificato. Ad esempio, un numero di telefono che si trovava in una rubrica elettronica in formato [canonico](address-ovr.md) richiederà la conversione in formato di [composizione](address-ovr.md) .

Per alcune sessioni possono essere richiesti parametri di installazione speciali, se supportati dal provider di servizi. Un TSP ISDN può ad esempio trasmettere informazioni utente utente e alcuni MSPs richiedono informazioni sulla direzione del flusso multimediale. Per una verifica dei dati che possono essere impostati o ottenuti per una sessione, vedere [informazioni sulla sessione](session-information-ovr.md) .

Una volta avviata una sessione, TAPI informa l'applicazione dello stato di avanzamento della chiamata utilizzando il meccanismo di notifica degli eventi impostato durante l'inizializzazione.

**TAPI 2. x:** Le applicazioni avviano una sessione utilizzando la funzione [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) . La funzione [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) viene usata per eseguire la conversione degli indirizzi, se necessario.

I parametri di installazione delle chiamate possono essere archiviati nella struttura dei dati [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams) e un puntatore a questa struttura viene quindi utilizzato come parametro di [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall). Se non viene fornita alcuna struttura **LINECALLPARAMS** per **lineMakeCall**, viene richiesta una chiamata di livello vocale di POT predefiniti con un set di valori predefiniti.

Se la sessione è configurata correttamente, all'applicazione viene restituito un handle di chiamata con [privilegi](privilege-ovr.md) di *proprietario* e TAPI invia i messaggi [**\_ CALLSTATE della riga**](./line-callstate.md) dell'applicazione con informazioni relative allo stato della chiamata. Le applicazioni in genere utilizzano questi messaggi per visualizzare i rapporti di stato all'utente.

**TAPI 3. x:** Le applicazioni avviano una sessione di comunicazione richiamando il metodo [**ITAddress:: CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall) su un indirizzo in grado di gestire il tipo di indirizzo e il tipo di supporto richiesto. Se l'indirizzo espone l'interfaccia [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) , i terminali vengono selezionati nei flussi multimediali dell'oggetto chiamata. Per un'illustrazione di questo processo, vedere l'esempio relativo [a un](make-a-call.md) codice di chiamata.

È possibile archiviare o modificare i parametri di installazione delle chiamate usando metodi esposti dall'interfaccia [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .

Se la sessione è configurata correttamente, TAPI restituisce un puntatore a interfaccia [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) che può essere usato per altre operazioni di sessione o per ottenere un puntatore a interfaccia [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) che può essere usato per acquisire informazioni aggiuntive sulla sessione. L'interfaccia [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent) elabora gli eventi di stato della chiamata TAPI.

> [!Note]  
> Non usare TAPI per trasmissioni fax. Usare invece le funzioni disponibili tramite MAPI, l'API Microsoft Messaging.

 

## <a name="address-translation"></a>Traduzione indirizzi

Un'applicazione server o un utente finale può archiviare indirizzi in un formato non compatibile con le esigenze di un determinato provider di servizi. Un numero di telefono, ad esempio, può essere archiviato in una rubrica elettronica in [formato canonico](address-ovr.md), ma la maggior parte dei provider di servizi che gestiscono i numeri di telefono richiede il [formato di composizione](address-ovr.md).

TAPI fornisce operazioni di conversione degli indirizzi che consentono a un'applicazione di presentare il tipo di indirizzo corretto a un TSP. Il provider di servizi specifica a TAPI i tipi di indirizzi supportati e non deve includere alcuna forma di conversione degli indirizzi.

**TAPI 2. x:** Vedere [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress).

**TAPI 3:** Vedere [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation), [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo).

## <a name="toll-lists"></a>Elenchi a pedaggio

In alcune posizioni America del Nord, tutte le chiamate telefoniche effettuate al codice locale sono chiamate locali. In altre posizioni, alcune chiamate effettuate al codice dell'area locale sono lunghe e richiedono un prefisso "1" da comporre. Le prime tre cifre dell'indirizzo (il prefisso) determinano se una chiamata nel codice dell'area locale è una chiamata a pedaggio.

Un *elenco* a discesa è costituito da un elenco di prefissi nel codice di area locale i cui indirizzi devono essere composte come indirizzi a distanza lunga e vengono valutati addebiti a distanza.

Gli elenchi a pedaggio non sono rilevanti per i provider di servizi o per le applicazioni che non accedono a una rete telefonica.

**TAPI 2. x:** Vedere [**lineTranslateAddress**](/windows/win32/api/tapi/nf-tapi-linetranslateaddress) (LINETRANSLATERESULT \_ intoll e LINETRANSLATERESULT \_ NOTINTOLLLIST BITS nella struttura [**LINETRANSLATEOUTPUT**](/windows/win32/api/tapi/ns-tapi-linetranslateoutput) ), [**lineSetTollList**](/windows/win32/api/tapi/nf-tapi-linesettolllist).

**TAPI 3:** Vedere [**ITAddressTranslation:: TranslateAddress**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-translateaddress), [**ITAddressTranslationInfo:: Get \_ TranslationResults**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslationinfo-get_translationresults).

 

 
