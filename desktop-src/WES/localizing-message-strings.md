---
title: Localizzazione di stringhe di messaggio
description: Ogni stringa di messaggio specificata nel manifesto deve fare riferimento a una stringa nella sezione localizzazione del manifesto.
ms.assetid: aeae9ef6-6ef7-46f5-a9ab-fabe418549b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b55b94ea8e8a40de1401cf3aba97488d5531a77b441361e38f1ff98219940afc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587899"
---
# <a name="localizing-message-strings"></a>Localizzazione di stringhe di messaggio

Ogni stringa di messaggio specificata nel manifesto deve fare riferimento a una stringa nella **sezione localizzazione** del manifesto. La sezione localizzazione contiene una sezione della tabella di stringhe per ogni impostazione locale che è possibile supportare.

Nell'esempio seguente viene illustrato come definire una tabella di stringhe. È necessario specificare gli attributi **id** e **value della** stringa. Usare il valore dell'attributo **id** per fare riferimento alla stringa nel manifesto. **L'attributo** value contiene la stringa localizzata.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider" 
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}" 
                symbol="PROVIDER_GUID" 
                resourceFileName="<path to the exe or dll that contains the metadata resources>" 
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.ProviderName)">

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="ProviderName" value="Sample Provider"/>
                <string id="PathNotFound" value="The path %1 was not found."/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```


Invece di aggiungere stringhe localizzate al manifesto, è necessario creare un file mui (Multilingual User Interface) per ogni lingua che si supporta. Usare un file di testo del messaggio per specificare le stringhe localizzate.

La procedura seguente descrive come creare un file MUI per l'inglese e il francese.

**Per creare un file MUI per inglese e francese**

1.  Creare un file di testo del messaggio che crea le stringhe di messaggio in francese. Per informazioni dettagliate sulla creazione di un file di testo del messaggio, vedere [File di testo dei messaggi](/windows/desktop/EventLog/message-text-files). Gli identificatori di messaggio specificati nel file di testo del messaggio devono corrispondere a quello generato dal compilatore di messaggi per le stesse stringhe nel manifesto. Per determinare gli identificatori di risorsa usati per le stringhe nel manifesto, vedere il file con estensione h generato dal compilatore di messaggi durante la compilazione del manifesto.
    ```Text
    LanguageNames=(French=0x40C:MSG0040C)

    ; // The following are message definitions.

    MessageId=0x00000065
    SymbolicName=MSG_ProviderName
    Language=French
    <FRENCH STRING GOES HERE>
    .


    MessageId=0x00000066
    SymbolicName=MSG_PathNotFound
    Language=French
    <FRENCH STRING GOES HERE>
    .
    
    ```


2.  Eseguire i comandi seguenti per creare la DLL della risorsa che contiene le stringhe localizzate. Il messages.mc file è il file di testo del messaggio creato nel passaggio 1.
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  Nella cartella che contiene il provider creare una sottocartella per ogni impostazioni locali supportate. Il nome della sottocartella deve essere il nome della lingua per le impostazioni locali. Ad esempio, per 0x0409, usare en-US come nome della cartella.
4.  Creare un file con estensione rcconfig che indica Muirct.exe che si desidera dividere le risorse della stringa di messaggio dal file eseguibile e dalle DLL delle risorse. Di seguito è riportato un file con estensione rcconfig di esempio.
    ```XML
    <localization>
          <resources>
                <win32Resources fileType="Application">
                      <neutralResources>
                      </neutralResources>
                      <localizedResources>
                            <resourceType typeNameId="#11"/>
                      </localizedResources>
                </win32Resources>
          </resources>
    </localization>
    ```
  

5.  Eseguire i comandi seguenti Muirct.exe per dividere le stringhe in inglese dal file eseguibile del provider.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  Eseguire i comandi Muirct.exe seguenti per dividere le stringhe in francese dalla DLL della risorsa. Rimuovere il file indipendente dalla lingua (fr-FRmessages.dll) dopo \\ la creazione del file MUI.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  Rinominare provider.exe.ln in provider.exe.
