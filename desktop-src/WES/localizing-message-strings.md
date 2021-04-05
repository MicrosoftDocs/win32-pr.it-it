---
title: Localizzazione delle stringhe di messaggio
description: Ogni stringa di messaggio specificata nel manifesto deve fare riferimento a una stringa nella sezione localizzazione del manifesto.
ms.assetid: aeae9ef6-6ef7-46f5-a9ab-fabe418549b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7812aed8bf376994a2cbecfa5997737d9740ec1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047045"
---
# <a name="localizing-message-strings"></a>Localizzazione delle stringhe di messaggio

Ogni stringa di messaggio specificata nel manifesto deve fare riferimento a una stringa nella sezione **localizzazione** del manifesto. La sezione localizzazione contiene una sezione della tabella di stringhe per ogni impostazione locale supportata.

Nell'esempio seguente viene illustrato come definire una tabella di stringhe. È necessario specificare gli attributi **ID** e **value** della stringa. Usare il valore dell'attributo **ID** per fare riferimento alla stringa nel manifesto. L'attributo **value** contiene la stringa localizzata.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="https://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="https://www.w3.org/2001/XMLSchema"    
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


Anziché aggiungere stringhe localizzate al manifesto, è necessario creare un file di interfaccia utente multilingue (MUI) per ogni lingua supportata. Utilizzare un file di testo del messaggio per specificare le stringhe localizzate.

Nella procedura seguente viene descritto come creare un file MUI per l'inglese e il francese.

**Per creare un file MUI per l'inglese e il francese**

1.  Creare un file di testo del messaggio per la creazione delle stringhe di messaggio francesi. Per informazioni dettagliate sulla creazione di un file di testo del messaggio, vedere [file di testo del messaggio](/windows/desktop/EventLog/message-text-files). Gli identificatori di messaggio specificati nel file di testo del messaggio devono corrispondere agli identificatori di risorsa generati dal compilatore di messaggi per le stesse stringhe nel manifesto. Per determinare gli identificatori di risorsa usati per le stringhe nel manifesto, vedere il file con estensione h generato dal compilatore di messaggi durante la compilazione del manifesto.
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


2.  Eseguire i comandi seguenti per creare la DLL di risorse che contiene le stringhe localizzate. Il file messages.mc è il file di testo del messaggio creato nel passaggio 1.
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  Nella cartella che contiene il provider creare una sottocartella per ogni impostazione locale supportata. Il nome della sottocartella deve corrispondere al nome della lingua per le impostazioni locali. Per 0x0409, ad esempio, usare en-US come nome della cartella.
4.  Creare un file con estensione rcconfig che indichi allo strumento Muirct.exe che si desidera suddividere le risorse della stringa del messaggio dal file eseguibile e dalle DLL della risorsa. Di seguito è riportato un esempio di file con estensione rcconfig.
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
  

5.  Eseguire i comandi di Muirct.exe seguenti per suddividere le stringhe inglesi dal file eseguibile del provider.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  Eseguire i comandi di Muirct.exe seguenti per suddividere le stringhe francesi dalla DLL della risorsa. Rimuovere il file indipendente dalla lingua (fr-FR \\messages.dll) dopo la creazione del file MUI.
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  Rinominare provider.exe. LN provider.exe.