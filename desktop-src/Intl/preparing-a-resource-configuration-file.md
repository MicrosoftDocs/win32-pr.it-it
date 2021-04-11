---
description: Preparazione di un file di configurazione delle risorse
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: Preparazione di un file di configurazione delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac162ad7f6d20148e0ef60cb9dc15da41cc27186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128926"
---
# <a name="preparing-a-resource-configuration-file"></a>Preparazione di un file di configurazione delle risorse

Entrambe le utilità del compilatore MUIRCT e RC descritte in [Utilità risorse](resource-utilities.md) forniscono un'opzione della riga di comando che consente di specificare un file di configurazione delle risorse per le risorse della lingua di base. L'uso di questo file XML pubblico leggibile consente un maggiore controllo sulla suddivisione delle risorse rispetto a quelle che è possibile ottenere usando le normali opzioni della riga di comando delle utilità. Tuttavia, anche se non si fornisce un file di configurazione delle risorse come input, i file di risorse LN e Language-specific conterranno i dati di configurazione delle risorse.

Tutti i file di configurazione delle risorse per le applicazioni Win32 iniziano e terminano in modo identico:


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



In questo argomento vengono illustrati gli aspetti del XML Schema utili per la compilazione di codice non gestito in Windows Vista e versioni successive. In particolare, è interessato solo dal comportamento dell'elemento win32Resources.

## <a name="win32resources-element"></a>Elemento win32Resources

L'elemento win32Resources ha gli attributi descritti nella tabella seguente.



| Nome attributo           | Obbligatorio | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fileType                 | No        | Tipo di file. Deve sempre essere "Application".                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| checksum                 | No        | Valore di checksum da visualizzare nei dati di configurazione delle risorse dei file di risorse nel file e nel linguaggio specifico. Questo attributo, ad esempio, consente di copiare il checksum da un singolo file di risorse specifico della lingua, per convenzione quello per la lingua inglese (Stati Uniti) e inserire il checksum in un file di risorse specifico della lingua diverso. Il checksum può essere specificato come stringa di numero esadecimale non più lunga di 32 caratteri. Il valore numerico deve essere contenuto in un numero a 128 bit. |
| Linguaggio                 | No        | Lingua specificata utilizzando un formato di nome conforme a RFC 4646 (Windows Vista e versioni successive), ad esempio en-US per la lingua inglese (Stati Uniti).                                                                                                                                                                                                                                                                                                                                                                             |
| ultimateFallbackLanguage | No        | Lingua da inserire nei dati di configurazione della risorsa per il file LN, che rappresenta il linguaggio di fallback finale da usare in una ricerca di un file di risorse specifico per la lingua corrispondente. Se il caricatore di risorse non riesce a caricare un file di risorse richiesto dalle lingue dell'interfaccia utente preferite del thread, viene usato un linguaggio di fallback finale come ultimo tentativo. Il linguaggio viene specificato utilizzando un formato di nome conforme a RFC 4646 (Windows Vista e versioni successive), ad esempio, en-US per la lingua inglese (Stati Uniti).       |
| ultimateFallbackLocation | No        | Percorso di fallback. Specificare "Internal" se le risorse di fallback Ultimate sono compilate nel file LN. Specificare "External" (impostazione predefinita) se il file LN fa riferimento a un file di risorse specifico della lingua per le risorse di fallback finali.                                                                                                                                                                                                                                                                                |



 

Nel file di configurazione delle risorse, l'elemento win32Resources include i sottoelementi descritti nella tabella seguente.



| Nome dell'elemento       | Descrizione                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| localizedResources | Risorse che incapsulano informazioni sui tipi di risorse e le singole risorse contenute in un file di risorse specifico del linguaggio. |
| neutralResources   | Risorse che incapsulano informazioni sui tipi di risorse contenuti in un file LN.                                                 |



 

## <a name="localizedresources-element"></a>Elemento localizedResources

Elemento resources localizzato. Per impostazione predefinita, questo elemento non ha attributi e un solo tipo di sottoelemento. Si tratta semplicemente di un contenitore per gli elementi resourceType.



| Nome attributo | Descrizione                                                                    |
|----------------|--------------------------------------------------------------------------------|
| resourceType   | Tipo di una singola risorsa contenuta in un file di risorse specifico del linguaggio. |



 

## <a name="neutralresources-element"></a>Elemento neutralResources

Elemento resources neutro. Questo elemento è semplicemente un contenitore per gli elementi resourceType.



| Nome attributo | Descrizione                                        |
|----------------|----------------------------------------------------|
| resourceType   | Tipo di una singola risorsa contenuta in un file LN. |



 

## <a name="resourcetype-element"></a>Elemento resourceType

L'elemento resourceType incapsula le informazioni su un singolo tipo di risorsa o singola risorsa. Dispone degli attributi elencati di seguito.

> [!Caution]  
> Alcuni difetti di configurazione delle risorse vengono intercettati solo dal compilatore RC o MUIRCT, a seconda del contenuto del file di risorse di input o del file binario. Gli errori resourceType nel file di configurazione delle risorse che non esistono nel file di input non vengono rilevati, causando un comportamento imprevisto. Gli utenti possono usare un file di configurazione delle risorse difettoso e non conoscono fino a quando non introducono file binari che usano le parti interrotte del file di configurazione delle risorse, che consente di creare l'aspetto delle interruzioni rispetto ai file binari correnti.

 



| Nome attributo | Obbligatorio | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeNameId     | Sì       | Nome del tipo o identificatore per la risorsa. Specificare un nome di stringa o un numero. Se si usa un numero, anteporre la stringa a " \# " per indicare che rappresenta un numero. Ogni elemento resourceType deve avere un solo attributo *typeNameId* .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| itemName       | No        | Stringa del nome dell'elemento per la risorsa, da inserire nel file di risorse specifico del linguaggio. È possibile specificare più nomi, separati da spazi vuoti, ad esempio, "HTML MOFDATA".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| itemId         | No        | Identificatore dell'elemento di risorsa singolo da inserire nel file di risorse specifico della lingua. L'elemento può essere specificato come intervallo (ad esempio, "1-12") o da identificatori singoli separati da spazi vuoti (ad esempio, "1 3 4").                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| stringId       | No        | Identificatore di stringa per un singolo elemento di risorsa, da inserire nel file di risorse specifico del linguaggio. La stringa può essere specificata come intervallo (ad esempio, "1-12") o da identificatori singoli separati da spazi vuoti (ad esempio, "1 3 4"). Questo attributo consente di specificare le voci della tabella di stringhe localizzabili e non localizzabili. Deve essere usato in combinazione con il valore di *typeNameId* "6", che indica un tipo di risorsa voce della tabella di stringhe.<br/> Le stringhe vengono archiviate in blocchi di 16 in una tabella di stringhe. Le stringhe da 0 a 15, ad esempio, vengono archiviate in un singolo blocco di elementi di risorsa ed è possibile farvi riferimento nel file di configurazione delle risorse come *ItemId* 1 o come *stringId* "0-15". Se ad esempio sono presenti cinque stringhe localizzabili e tre stringhe non localizzabili, è necessario assegnare gli identificatori di stringa 0-4 per le stringhe localizzabili e gli identificatori di stringa 16-18 per le stringhe non localizzabili. Se non si organizzano stringhe in questo modo, i blocchi di stringhe interessati vengono inseriti sia nel file di risorse che nel file di risorse specifico del linguaggio.<br/> |



 

Se si specificano gli attributi *ItemName*, *ItemId* e/o *stringId* per un determinato tipo di risorsa nell'elemento localizedResource, solo gli elementi o le stringhe specificate per il tipo di risorsa designato vengono inseriti nel file di risorse specifico della lingua. Se viene specificato un elemento resourceType senza un nome di elemento esplicito, un identificatore di elemento o un identificatore di stringa, tutti gli elementi del tipo di risorsa specificato vengono inseriti nel file di risorse specifico del linguaggio. Gli elementi o i tipi non elencati in nessun elemento localizedResource vengono inseriti nel file LN.

Di seguito sono riportati i tipi di risorse standard e i relativi identificatori numerici:

-   CURSORE (1)
-   BITMAP (2)
-   ICONA (3)
-   MENU (4)
-   FINESTRA DI DIALOGO (5)
-   STRINGA (6)
-   FONTDIR (7)
-   CARATTERE (8)
-   ACCELERATORI (9)
-   RCDATA (10)
-   MESSAGETABLE (11)
-   \_Cursore gruppo (12)
-   Icona di gruppo \_ (14)
-   VERSIONE (16)
-   HTML (23)

## <a name="example"></a>Esempio


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>
  <resources>
    <win32Resources fileType="Application">
      <neutralResources>
        <resourceType
           typeNameId="#16"
        />
      </neutralResources>
      <localizedResources> 
         <resourceType
                typeNameId="#2"
                itemId="5 6 7 8 9 10 11 12"
                itemName="HTML PRI"
         />
         <resourceType
                typeNameId="#4"
         />
         <resourceType
                typeNameId="#5"
         />
         <resourceType
                typeNameId="#6"
         />
         <resourceType
                typeNameId="#9"
         />
         <resourceType
                typeNameId="#11"
         />
         <resourceType
                typeNameId="#16"
         />
         <resourceType
                typeNameId="HTML"
         />
         <resourceType
                typeNameId="#23"
         />
         <resourceType
                typeNameId="#240"
         />
         <resourceType
                typeNameId="#1024"
         />
         <resourceType
                typeNameId="MY_TYPE"
         />
      </localizedResources> 
    </win32Resources>
  </resources>
</localization>
```



## <a name="remarks"></a>Commenti

Se si include un tipo di risorsa ICON (3), DIALOG (5), STRING (6) o VERSION (16) nell'elemento neutralResources, è necessario duplicare tale voce nell'elemento localizedResources. È possibile osservare questo aspetto nell'esempio precedente, in cui il tipo di risorsa 16 viene visualizzato nelle sezioni risorse neutre e localizzate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Preparazione delle risorse](preparing-resources.md)
</dt> </dl>

 

 




