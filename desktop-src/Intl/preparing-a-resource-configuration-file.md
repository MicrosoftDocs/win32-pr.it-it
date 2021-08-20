---
description: Preparazione di un file di configurazione delle risorse
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: Preparazione di un file di configurazione delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b862f48f15997300f079a39de0eb385c535758d9392dc452e1d338d86c8d59e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147104"
---
# <a name="preparing-a-resource-configuration-file"></a>Preparazione di un file di configurazione delle risorse

Entrambe le utilità MUIRCT e RC Compiler descritte in [Utilità](resource-utilities.md) risorse forniscono un'opzione della riga di comando che consente di specificare un file di configurazione delle risorse per le risorse del linguaggio di base. L'uso di questo file XML pubblico e leggibile consente un maggiore controllo sulla suddivisione delle risorse rispetto a quello che è possibile ottenere usando le normali opzioni della riga di comando delle utilità. Tuttavia, anche se non si specifica un file di configurazione delle risorse come input, l'LN e i file di risorse specifici della lingua conterranno i dati di configurazione delle risorse.

Tutti i file di configurazione delle risorse per le applicazioni Win32 iniziano e terminano in modo identico:


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



Questo argomento illustra gli aspetti di XML Schema utili per la compilazione di codice non gestito in Windows Vista e versioni successive. In particolare, riguarda solo il comportamento dell'elemento win32Resources.

## <a name="win32resources-element"></a>Elemento win32Resources

L'elemento win32Resources ha gli attributi descritti nella tabella seguente.



| Nome attributo           | Obbligatorio | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| fileType                 | No        | Tipo di file. Deve essere sempre "Application".                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| checksum                 | No        | Valore di checksum da visualizzare nei dati di configurazione delle risorse del file LN e dei file di risorse specifici della lingua. Ad esempio, questo attributo consente di copiare il checksum da un singolo file di risorse specifico della lingua, per convenzione quello per l'inglese (Stati Uniti) e di inserire il checksum in un file di risorse specifico della lingua. Il checksum può essere specificato come stringa di numeri esadecimali che non contiene più di 32 caratteri. Il valore numerico deve essere contenuto in un numero a 128 bit. |
| Linguaggio                 | No        | Lingua specificata usando un formato del nome conforme a RFC 4646 (Windows Vista e versioni successive), ad esempio en-US per l'inglese (Stati Uniti).                                                                                                                                                                                                                                                                                                                                                                             |
| ultimateFallbackLanguage | No        | Lingua da inserire nei dati di configurazione delle risorse per il file LN, che rappresenta la lingua di fallback finale da usare nella ricerca di un file di risorse specifico della lingua corrispondente. Se il caricatore di risorse non riesce a caricare un file di risorse richiesto dalle lingue dell'interfaccia utente preferite del thread, usa un linguaggio di fallback finale come ultimo tentativo. La lingua viene specificata usando un formato del nome conforme a RFC 4646 (Windows Vista e versioni successive), ad esempio en-US per l'inglese (Stati Uniti).       |
| ultimateFallbackLocation | No        | Percorso di fallback. Specificare "internal" se le risorse di fallback finale vengono compilate nel file LN. Specificare "external" (impostazione predefinita) se il file LN deve fare riferimento a un file di risorse specifico della lingua per le risorse di fallback finale.                                                                                                                                                                                                                                                                                |



 

Nel file di configurazione delle risorse, l'elemento win32Resources contiene gli elementi secondari descritti nella tabella seguente.



| Nome dell'elemento       | Descrizione                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| localizedResources | Risorse che incapsulano informazioni sui tipi di risorse e sulle singole risorse contenute in un file di risorse specifico del linguaggio. |
| proprietà neutralResources   | Risorse che incapsulano informazioni sui tipi di risorse contenuti in un file LN.                                                 |



 

## <a name="localizedresources-element"></a>Elemento localizedResources

Elemento resources localizzato. Per impostazione predefinita, questo elemento non ha attributi e un solo tipo di sotto-elemento. È solo un contenitore per gli elementi resourceType.



| Nome attributo | Descrizione                                                                    |
|----------------|--------------------------------------------------------------------------------|
| resourceType   | Tipo di una singola risorsa contenuta in un file di risorse specifico della lingua. |



 

## <a name="neutralresources-element"></a>Elemento neutralResources

Elemento risorse neutre. Questo elemento è solo un contenitore per gli elementi resourceType.



| Nome attributo | Descrizione                                        |
|----------------|----------------------------------------------------|
| resourceType   | Tipo di una singola risorsa contenuta in un file LN. |



 

## <a name="resourcetype-element"></a>Elemento resourceType

L'elemento resourceType incapsula informazioni su un singolo tipo di risorsa o su una singola risorsa. Include gli attributi elencati di seguito.

> [!Caution]  
> Alcuni difetti di configurazione delle risorse vengono intercettato solo dal compilatore RC o da MUIRCT, a seconda del file di risorse di input o del contenuto del file binario. Gli errori resourceType nel file di configurazione delle risorse che non esistono nel file di input non vengono rilevati, determinando un comportamento imprevisto. Gli utenti possono usare un file di configurazione delle risorse difettoso e non sanno fino a quando non introducono file binari che usano le parti interrotte del file di configurazione delle risorse, il che crea l'aspetto che le interruzioni derivano dai file binari correnti.

 



| Nome attributo | Obbligatorio | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| typeNameId     | Sì       | Nome o identificatore del tipo per la risorsa. Specificare un nome di stringa o un numero. Se si usa un numero, anteporre alla stringa un " \# " per indicare che rappresenta un numero. Ogni elemento resourceType deve avere un solo *attributo typeNameId.*                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| itemName       | No        | Stringa del nome dell'elemento per la risorsa da inserire nel file di risorse specifico della lingua. È possibile specificare più nomi, separati da spazi vuoti, ad esempio "HTML MOFDATA".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| itemId         | No        | Identificatore del singolo elemento di risorsa da inserire nel file di risorse specifico della lingua. L'elemento può essere specificato come intervallo (ad esempio, "1-12") o da singoli identificatori separati da spazi vuoti (ad esempio, "1 3 4").                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| stringId       | No        | Identificatore di stringa per il singolo elemento di risorsa da inserire nel file di risorse specifico della lingua. La stringa può essere specificata come intervallo (ad esempio, "1-12") o da singoli identificatori separati da spazi vuoti (ad esempio, "1 3 4"). Questo attributo consente la specifica di voci della tabella di stringhe localizzabili e non localizzabili. Deve essere usato in combinazione con il valore *typeNameId* di "6", indicando un tipo di risorsa voce della tabella di stringhe.<br/> Le stringhe vengono archiviate in blocchi di 16 in una tabella di stringhe. Ad esempio, le stringhe da 0 a 15 vengono archiviate in un singolo blocco di elementi di risorsa e è possibile farvi riferimento nel file di configurazione delle risorse come *itemId* 1 o come *stringId* "0-15". Ad esempio, se sono presenti cinque stringhe localizzabili e tre stringhe non localizzabili, è necessario assegnare gli identificatori di stringa da 0 a 4 per le stringhe localizzabili e gli identificatori di stringa 16-18 per le stringhe non localizzabili. Se le stringhe non vengono organizzate in questo modo, i blocchi di stringhe interessati vengono inseriti sia nel file LN che nel file di risorse specifico della lingua.<br/> |



 

Se si specificano gli attributi *itemName,* *itemId* e/o *stringId* per un particolare tipo di risorsa nell'elemento localizedResource, solo questi elementi o stringhe specificati per il tipo di risorsa designato vengono inseriti nel file di risorse specifico della lingua. Se un elemento resourceType viene specificato senza un nome di elemento esplicito, un identificatore di elemento o un identificatore di stringa, tutti gli elementi del tipo di risorsa specificato vengono inseriti nel file di risorse specifico della lingua. Gli elementi o i tipi non elencati in alcun elemento localizedResource vengono inseriti nel file LN.

Di seguito sono riportati i tipi di risorsa standard e i relativi identificatori numerici:

-   CURSOR(1)
-   BITMAP(2)
-   ICON(3)
-   MENU(4)
-   DIALOG(5)
-   STRING(6)
-   FONTDIR(7)
-   FONT(8)
-   ACCELERATORS(9)
-   RCDATA(10)
-   MESSAGETABLE(11)
-   GROUP \_ CURSOR(12)
-   ICONA \_ GRUPPO (14)
-   VERSION(16)
-   HTML(23)

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

Se si include un tipo di risorsa ICON(3), DIALOG(5), STRING(6) o VERSION(16) nell'elemento neutralResources, è necessario duplicare tale voce nell'elemento localizedResources. Come illustrato nell'esempio precedente, il tipo di risorsa 16 viene visualizzato nelle sezioni delle risorse neutre e localizzate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Preparazione delle risorse](preparing-resources.md)
</dt> </dl>

 

 




