---
title: Strumento del compilatore del servizio Web
description: Per supportare il modello di servizio, wsutil.exe genera un'intestazione da usare sia sul lato client che sul lato servizio. Genera il file proxy C per il lato client e il file stub C per il lato servizio, in base alle esigenze.
ms.assetid: 1c73297d-0d3d-421c-9e19-44a6012a5c65
keywords:
- Web Service Compiler Tool Web Services for Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92e1195cd9d3a8e8d9fa1b7be94421d68f3cbdf2242be6fa0d05be5cc3c743f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962840"
---
# <a name="web-service-compiler-tool"></a>Strumento del compilatore del servizio Web

Per supportare il modello di servizio, wsutil.exe genera un'intestazione da usare sia sul lato client che sul lato servizio. Genera il file proxy C per il lato client e il file stub C per il lato servizio, in base alle esigenze.


Per [supportare la serializzazione](serialization.md), il compilatore genera intestazioni per le descrizioni degli elementi per le definizioni di elementi globali e tutte le informazioni sulla definizione del tipo nel file proxy che verranno utilizzate dal motore di serializzazione.

Utilizzo

**WsUtil.exe opzioni \[ della riga di comando \[ switch-options \] :\]<filename>**

opzioni della riga di comando

Specifica le WsUtil.exe del compilatore. I commutatori possono essere visualizzati in qualsiasi ordine. Trattino ('-') e barra ('/') vengono considerati uguali.

Elenco di opzioni della riga di comando

-   @filename Specifica che il file di input deve essere considerato come un file di risposta. Questa opzione può essere usata più volte, in qualsiasi luogo nell'elenco di argomenti.
-   /wsdl: :<url facoltativo> specifica che il file di <filename> input deve essere considerato come file \_ wsdl. Sono consentiti più input wsdl e vengono elaborati tutti i file wsdl specificati. \_L'URL facoltativo specifica il percorso da cui sono stati recuperati i metadati. Se non viene \_ specificato alcun URL facoltativo, Wsutil genera un URL univoco internamente. Vedere anche [Supporto dei criteri](policy-support.md).
-   /xsd: <filename> specifica che il nome file di input deve essere considerato come file di schema. Sono consentiti più input xsd e vengono elaborati tutti i file di schema specificati.
-   /wsp: :<url facoltativo> specifica che il nome file di <filename> input deve essere considerato come metadati dei \_ criteri. Sono consentiti più input wsp e vengono elaborati tutti i file di criteri specificati. \_L'URL facoltativo specifica il percorso da cui sono stati recuperati i metadati. Se non viene \_ specificato alcun URL facoltativo, Wsutil genera un URL univoco internamente. I file di criteri vengono ignorati se viene specificato il flag /nopolicy. Vedere anche [Supporto dei criteri](policy-support.md).
-   /nopolicy Disabilita l'elaborazione dei criteri.
-   /out: <dirname> specifica il nome della directory per i file di output
-   /noclient Non genera lo stub sul lato client.
-   /noservice Non genera lo stub sul lato servizio.
-   /prefix: <string> antepone la stringa specificata a tutti gli identificatori generati.
-   /fullname Antepone il nome file normalizzato agli identificatori generati. Per impostazione predefinita, verrà usato solo il nome specificato nell'attributo "name" per generare identificatori per le descrizioni correlate.
-   /string:<WS STRING><WCHAR> Per impostazione predefinita, wsutil genera WCHAR per il tipo \_ \| \* \* xsd:string. L'applicazione può usare questo flag per sovrascrivere tale comportamento e genera invece WS \_ STRING per xsd:type.
-   /help Visualizza il messaggio della Guida
-   /? Uguale a /help
-   /W:x Opzioni di gestione degli errori. Potrebbe essere W:0-W:4 \| WX
-   /nologo Non genera informazioni specifiche del compilatore sull'output della console.
-   /nostamp Non genera informazioni specifiche del compilatore sui file generati.

Per impostazione predefinita, il compilatore genera i file seguenti per il file WSDL o WSDL restituiti dallo scambio di metadati:

-   Proxy client ({inputfilename}.c)
-   Stub del servizio ({inputfilename}.c)
-   File di intestazione ({inputfilename}.h)

    La radice del nome file generato è il nome del file di input. Le estensioni dei file di input originali vengono mantenute per evitare conflitti di nomi file per i file generati. Per impostazione predefinita, gli stub client e del servizio vengono generati nello stesso file, con il codice stub del servizio generato dopo il codice proxy.

    Per impostazione predefinita, il compilatore genera i file seguenti per un file XSD per lo schema restituito dallo scambio di metadati:

-   descrizioni di serializzazione ({inputfilename}.c)
-   File di intestazione ({inputfilename}.h)

    La radice del nome file è il nome del servizio.

Wsutil.exe genera una sezione "stamp" all'inizio di tutti i file generati, che indica l'opzione del compilatore, la versione dello strumento, l'opzione della riga di comando applicabile e così via. Questa sezione può essere disattivata usando l'opzione /nostamp per evitare problemi con il confronto dei file generati.

Wsutil non supporta il download dei metadati

Il compilatore Wsutil funziona solo dal file di metadati locale. Lo strumento non supporta il download di metadati dall'esecuzione di servizi Web. Gli sviluppatori possono usare altri strumenti di servizio Web supportati, ad esempio svcutil, per scaricare metadati nel computer locale, esaminare i file salvati e passare tali file wsutil.exe per la compilazione.

Supporto di più file di input/output

WSDL e XML Schema consentono di includere/importare definizioni da altri spazi dei nomi specificati in altri file o percorso. Wsutil supporta più input schema/wsdl/criteri e genera un set di stub/intestazione per ogni file di input. Wsutil non segue le istruzioni include e import. L'applicazione deve invece passare i file contenenti tutti gli spazi dei nomi necessari a wsutil in modo che lo strumento possa risolvere tutte le dipendenze durante la compilazione.

**WsUtil.exe /xsd:stockquote.xsd /wsdl:stockquote.wsdl /wsdl:stockquoteservice.wsdl**

wsutil genera tre set di file di output:

-   stockquote.xsd.c stockquote.xsd.h
-   stockquote.wsdl.c stockquote.wsdl.h
-   stockquoteservice.wsdl.h stockquoteservices.wsdl.c

Tipi di file di output

Per ogni file di output, wsutil genera definizioni disponibili esternamente nel file di intestazione. Oltre alle definizioni di struttura C e ai prototipi di funzione stub, tutte le altre definizioni correlate ai servizi Web vengono incapsulate in una struttura globale denominata con nome file normalizzato.

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

Si noti che non tutti i campi vengono generati per la struttura globale. Un campo di primo livello viene generato solo quando le definizioni correlate vengono specificate nel file di input. Ad esempio, non vengono generati campi di messaggio, operazioni e contratti per i file xsd.

Livelli di avviso e livello di errore

Analogamente al compilatore C, WsUtil.exe supporta quattro livelli di avviso e un livello di errore:

-   WsUtil.exe genera errori con errori irreversibili, ad esempio file wsdl non validi, opzioni del compilatore non valide e così via.
-   WsUtil genera avvisi W1 con gravi problemi ripristinabili. Il compilatore può andare avanti, ma l'utente deve essere a conoscenza del problema. Ad esempio, verrà generato un avviso W1 se sono presenti attributi non supportati, ad esempio alcuni facet WSDL, in wsdl che non influiscono sulla generazione del codice.
-   WsUtil genera avvisi W2 con problemi meno gravi. Non c'è perdita di funzionalità, ma lo sviluppatore di applicazioni potrebbe voler sapere questo. Come i comportamenti che potrebbero essere diversi da altre piattaforme.
-   WsUtil genera avvisi W3 con un impatto minimo sul codice generato. Ad esempio, wsutil.exe genera un avviso W3 quando la stringa normalizzata è diversa dalla stringa originale.
-   L'avviso W4 è più simile agli avvisi "in formato informativo" e WsUtil emettere W4 in casi come ignorare l'attributo della documentazione in WSDL.
-   WX indica che il compilatore considera l'avviso come errore. Ad esempio, wsutil genera un errore per tutti gli avvisi W1 se si specifica /W:1 /WX.

/W:{N} specifica il livello di messaggio di avviso da generare. /W:1 indica che devono essere generati avvisi di livello 1 e gli avvisi del livello di avviso 2 e inferiore devono essere mascherati e non generati dallo strumento.

## <a name="fullname"></a>/fullname

Questa opzione indica che WsUtil.exe nome completo per gli identificatori per evitare potenziali conflitti di nomi. Ad esempio, in example.xsd sono presenti:

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

Per impostazione predefinita, WsUtil.exe genera:

``` syntax
typedef struct SimpleStruct {
  int a;
  int b;
};
```

Se tuttavia si specifica l'opzione della riga di comando /fullname, WsUtil.exe genera invece la definizione di struttura seguente:

``` syntax
typedef struct exmaple_xsd_SimpleStruct {
  int a;
  int b;
};
```

## <a name="globalization"></a>Globalizzazione

Lo strumento è indipendente dalla lingua e può essere localizzato in lingue diverse. Tutti i messaggi di errore o l'output della console possono essere localizzati. Tuttavia, le opzioni della riga di comando rimangono in inglese.

## <a name="environment-variable"></a>Variabile di ambiente

WsUtil.exe non usa variabili di ambiente.

## <a name="platform-independent"></a>Indipendente dalla piattaforma

I file di output WsUtil.exe sono indipendenti dalla piattaforma. Nello stub non viene generato codice dipendente dall'architettura. qualsiasi architettura specifica verrà curata dal compilatore C. Lo stub può essere usato in tutte le piattaforme supportate.

La descrizione dellwsutil.exe output è disponibile nella parte [Supporto WSDL](wsdl-support.md) e [Supporto](schema-support.md) schema.

 

 




