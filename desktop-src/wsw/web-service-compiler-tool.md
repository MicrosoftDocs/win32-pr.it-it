---
title: Strumento compilatore servizio Web
description: Per supportare il modello di servizio, wsutil.exe genera un'intestazione da usare sia sul lato client che sul lato servizio. Genera il file proxy C per il lato client e il file stub C per il lato del servizio, in base alle esigenze.
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Servizi Web per lo strumento di compilazione del servizio Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9931f228a36832fc83d84d584a151de41f5868d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399961"
---
# <a name="web-service-compiler-tool"></a>Strumento compilatore servizio Web

Per supportare il modello di servizio, wsutil.exe genera un'intestazione da usare sia sul lato client che sul lato servizio. Genera il file proxy C per il lato client e il file stub C per il lato del servizio, in base alle esigenze.


Per supportare la [serializzazione](serialization.md), il compilatore genera intestazioni per le descrizioni di elementi per le definizioni di elementi globali e tutte le informazioni sulla definizione del tipo nel file proxy che devono essere utilizzate dal motore di serializzazione.

Utilizzo

**WsUtil.exe \[ Opzioni switch della riga di comando \[ \] :\]<filename>**

opzioni della riga di comando

Specifica WsUtil.exe opzioni del compilatore. Le opzioni possono essere visualizzate in qualsiasi ordine. Il trattino ('-') e la barra ('/') vengono considerati uguali.

Elenco di opzioni della riga di comando

-   @filename Specifica che il file di input deve essere trattato come un file di risposta. Questa opzione può essere usata più volte, in qualsiasi posizione nell'elenco di argomenti.
-   /WSDL: <filename> : <\_ url facoltativo> specifica che il file di input deve essere trattato come un file WSDL. Sono consentiti più input WSDL e vengono elaborati tutti i file WSDL specificati. L' \_ URL facoltativo specifica il percorso da cui vengono recuperati i metadati. Se non \_ viene specificato alcun URL facoltativo, WSUTIL genera internamente un URL univoco. Vedere anche [supporto dei criteri](policy-support.md).
-   /xsd: <filename> specifica che il nome file di input deve essere considerato come un file di schema. Sono consentiti più input XSD e vengono elaborati tutti i file di schema specificati.
-   /wsp: <filename> : <\_ url facoltativo> specifica che il nome del file di input deve essere trattato come metadati del criterio. Sono consentiti più input WSP e vengono elaborati tutti i file di criteri specificati. L' \_ URL facoltativo specifica il percorso da cui vengono recuperati i metadati. Se non \_ viene specificato alcun URL facoltativo, WSUTIL genera internamente un URL univoco. I file dei criteri vengono ignorati se viene specificato il flag/nopolicy. Vedere anche [supporto dei criteri](policy-support.md).
-   /nopolicy Disabilita l'elaborazione dei criteri.
-   /out: <dirname> specifica il nome di directory per i file di output
-   /NoClient non generano lo stub lato client.
-   /noservice non genera lo stub del lato servizio.
-   /prefix: <string> anteporre la stringa specificata a tutti gli identificatori generati.
-   /FullName anteporre il nome file normalizzato agli identificatori generati. Per impostazione predefinita, solo il nome specificato nell'attributo "Name" verrà usato per generare gli identificatori per le descrizioni correlate.
-   /String: <WS \_ string>\|<WCHAR \*> per impostazione predefinita, WSUTIL genera WCHAR \* per il tipo XSD: String. L'applicazione può utilizzare questo flag per sovrascrivere tale comportamento e genera \_ invece una stringa WS per xsd: Type.
-   /Help Visualizza il messaggio della Guida
-   /? Uguale a/Help
-   /W: x opzioni di gestione degli errori. Potrebbe essere W:0-W: 4 \| WX
-   /nologo non generano informazioni specifiche del compilatore nell'output della console.
-   /nostamp non generano informazioni specifiche del compilatore sui file generati.

Per impostazione predefinita, il compilatore genera i file seguenti per il file WSDL o WSDL restituito dallo scambio di metadati:

-   Proxy client ({inputFilename}. c)
-   Stub servizio ({inputFilename}. c)
-   File di intestazione ({inputFilename}. h)

    La radice del nome file generato è il nome del file di input. Le estensioni di file di input originali vengono mantenute per impedire il conflitto di nomi di file per i file generati. Per impostazione predefinita, gli stub client e servizio vengono generati nello stesso file, con codice stub servizio generato dopo il codice proxy.

    Per impostazione predefinita, il compilatore genera i seguenti file per un file XSD per lo schema restituito dallo scambio di metadati:

-   descrizioni della serializzazione ({inputFilename}. c)
-   File di intestazione ({inputFilename}. h)

    La radice del nome file è il nome del servizio.

Wsutil.exe genera una sezione "timbro" all'inizio di tutti i file generati, che indica l'opzione del compilatore, la versione dello strumento, l'opzione della riga di comando applicabile e così via. Questa sezione può essere disattivata utilizzando l'opzione/nostamp per evitare rumore con il confronto dei file generati.

Wsutil non supporta il download dei metadati

Il compilatore WSUTIL funziona solo dal file di metadati locale. Lo strumento non supporta il download dei metadati dall'esecuzione di servizi Web. Gli sviluppatori possono utilizzare altri strumenti WebService supportati, ad esempio Svcutil, per scaricare i metadati nel computer locale, controllare i file salvati e passare i file a wsutil.exe per la compilazione.

Supporto di più file di input/output

WSDL e XML Schema consentono di includere/importare definizioni da altri spazi dei nomi specificati in altri percorsi o file. Wsutil supporta più input schema/WSDL/Policy e genera un set di Stub/intestazione per ogni file di input. Wsutil non segue le istruzioni include e Import. Al contrario, l'applicazione deve passare i file contenenti tutti gli spazi dei nomi necessari a WSUTIL in modo che lo strumento possa risolvere tutte le dipendenze durante la compilazione.

**WsUtil.exe/xsd: stockquote. xsd/WSDL: stockquote. WSDL/WSDL: StockQuoteService. WSDL**

wsutil genera tre set di file di output:

-   stockquote. xsd. c stockquote. xsd. h
-   stockquote. WSDL. c stockquote. WSDL. h
-   StockQuoteService. WSDL. h stockquoteservices. WSDL. c

Tipi di file di output

Per ogni file di output, WSUTIL genera definizioni disponibili esternamente nel file di intestazione. A parte le definizioni della struttura C e i prototipi di funzioni stub, tutte le altre definizioni correlate ai servizi Web sono incapsulate in una struttura globale denominata con il nome file normalizzato.

``` syntax
typedef struct _stockquote_wsdl {
  struct {
  ... // list of WS_STRUCT_DESCRIPTION for all global complex types.
  } globalTypes;
  struct {
  ... // WS_ELEMENT_DESCRIPTION for all global elements.
  } globalElements;
  struct {
  ...
  } messages;
  struct {
  ...
  } contracts;
} _stockquote_wsdl;

EXTERN_C _stockquote_wsdl stockquote_wsdl;
```

Si noti che non tutti i campi vengono generati per la struttura globale. Un campo di livello principale viene generato solo quando le definizioni correlate vengono specificate nel file di input. Per i file XSD, ad esempio, non viene generato alcun campo relativo a messaggi, operazioni e contratti.

Livelli di avviso e livello di errore

Analogamente al compilatore C, WsUtil.exe supporta quattro livelli di avviso e un livello di errore:

-   WsUtil.exe genera errori con errori irreversibili, ad esempio file WSDL non valido, opzioni del compilatore non valide e così via.
-   WsUtil genera avvisi W1 con gravi problemi reversibili. Il compilatore può continuare, ma è necessario che l'utente sia a conoscenza del problema. Ad esempio, verrà generato un avviso W1 se sono presenti attributi non supportati, come alcuni facet WSDL, in WSDL che non influisce sulla generazione del codice.
-   WsUtil genera avvisi W2 con problemi meno gravi. Non vi è alcuna perdita di funzionalità, ma lo sviluppatore di applicazioni potrebbe volerne saperlo. Comportamenti simili che potrebbero essere diversi dalle altre piattaforme.
-   WsUtil genera avvisi W3 con un minimo effetto sul codice generato. wsutil.exe, ad esempio, genera un avviso W3 quando la stringa normalizzata è diversa dalla stringa originale.
-   W4 Warning è più simile a "Informational" Warnings e WsUtil Issue W4 in casi come ignorare l'attributo Documentation in WSDL.
-   WX indica che il compilatore considera l'avviso come errore. Ad esempio, WSUTIL genera un errore per tutti gli avvisi W1 se/W: 1/WX è specificato.

/W: {N} specificare il livello di messaggio di avviso da generare. /W: 1 indica che devono essere generati avvisi di livello 1, mentre gli avvisi di livello 2 e di avviso indicati di seguito devono essere mascherati e non generati dallo strumento.

## <a name="fullname"></a>/fullname

Questa opzione indica che WsUtil.exe genera il nome completo per gli identificatori per evitare potenziali conflitti di nomi. Ad esempio, in XSD sono disponibili:

``` syntax
<wsdl:definitions xmlns:soap="http://schemas.xmlsoap.org/wsdl/soap/" xmlns:tns="http://Example.org" 
xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:xs="http://www.w3.org/2001/XMLSchema" 
xmlns:wsaw="http://www.w3.org/2006/05/addressing/wsdl" targetNamespace="http://Example.org" 
xmlns:wsdl="http://schemas.xmlsoap.org/wsdl/">
 <wsdl:types>
  <xs:element name="SimpleStruct">
   <xs:complexType>
    <xs:sequence>
     <xs:element name="a" type="xs:int" />
     <xs:element name="b" type="xs:int" />
    </xs:sequence>
   </xs:complexType>
  </xs:element>
 </wsdl:types>
</wsdl:definitions>
```

Per impostazione predefinita WsUtil.exe genera:

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

Tuttavia, se viene specificata l'opzione della riga di comando/FullName, WsUtil.exe genera invece la definizione della struttura seguente:

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a>Globalizzazione

Lo strumento è indipendente dalla lingua e può essere localizzato in lingue diverse. È possibile localizzare tutti i messaggi di errore o l'output della console. Tuttavia, le opzioni della riga di comando restano in inglese.

## <a name="environment-variable"></a>Variabile di ambiente

WsUtil.exe non utilizza alcuna variabile di ambiente.

## <a name="platform-independent"></a>Indipendente dalla piattaforma

I file di output di WsUtil.exe sono indipendenti dalla piattaforma. Nessun codice dipendente dall'architettura generato nello stub; qualsiasi architettura specifica verrà gestita dal compilatore C. Lo stub può essere usato in tutte le piattaforme supportate.

La descrizione dell'output wsutil.exe è disponibile nel [supporto WSDL](wsdl-support.md) e nella parte relativa al [supporto dello schema](schema-support.md) .

 

 




