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
# <a name="localizing-message-strings"></a><span data-ttu-id="f4555-103">Localizzazione delle stringhe di messaggio</span><span class="sxs-lookup"><span data-stu-id="f4555-103">Localizing Message Strings</span></span>

<span data-ttu-id="f4555-104">Ogni stringa di messaggio specificata nel manifesto deve fare riferimento a una stringa nella sezione **localizzazione** del manifesto.</span><span class="sxs-lookup"><span data-stu-id="f4555-104">Each message string that you specify in the manifest must reference a string in the **localization** section of the manifest.</span></span> <span data-ttu-id="f4555-105">La sezione localizzazione contiene una sezione della tabella di stringhe per ogni impostazione locale supportata.</span><span class="sxs-lookup"><span data-stu-id="f4555-105">The localization section contains a string table section for each locale that you support.</span></span>

<span data-ttu-id="f4555-106">Nell'esempio seguente viene illustrato come definire una tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="f4555-106">The following example shows how to define a string table.</span></span> <span data-ttu-id="f4555-107">È necessario specificare gli attributi **ID** e **value** della stringa.</span><span class="sxs-lookup"><span data-stu-id="f4555-107">You must specify the string's **id** and **value** attributes.</span></span> <span data-ttu-id="f4555-108">Usare il valore dell'attributo **ID** per fare riferimento alla stringa nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="f4555-108">You use the value of the **id** attribute to reference the string in your manifest.</span></span> <span data-ttu-id="f4555-109">L'attributo **value** contiene la stringa localizzata.</span><span class="sxs-lookup"><span data-stu-id="f4555-109">The **value** attribute contains the localized string.</span></span>


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


<span data-ttu-id="f4555-110">Anziché aggiungere stringhe localizzate al manifesto, è necessario creare un file di interfaccia utente multilingue (MUI) per ogni lingua supportata.</span><span class="sxs-lookup"><span data-stu-id="f4555-110">Instead of adding localized strings to the manifest, you should create a multilingual user interface (MUI) file for each language that you support.</span></span> <span data-ttu-id="f4555-111">Utilizzare un file di testo del messaggio per specificare le stringhe localizzate.</span><span class="sxs-lookup"><span data-stu-id="f4555-111">Use a message text file to specify your localized strings.</span></span>

<span data-ttu-id="f4555-112">Nella procedura seguente viene descritto come creare un file MUI per l'inglese e il francese.</span><span class="sxs-lookup"><span data-stu-id="f4555-112">The following procedure describes how to create a MUI file for English and French.</span></span>

<span data-ttu-id="f4555-113">**Per creare un file MUI per l'inglese e il francese**</span><span class="sxs-lookup"><span data-stu-id="f4555-113">**To create a MUI file for English and French**</span></span>

1.  <span data-ttu-id="f4555-114">Creare un file di testo del messaggio per la creazione delle stringhe di messaggio francesi.</span><span class="sxs-lookup"><span data-stu-id="f4555-114">Create a message text file that creates the French message strings.</span></span> <span data-ttu-id="f4555-115">Per informazioni dettagliate sulla creazione di un file di testo del messaggio, vedere [file di testo del messaggio](/windows/desktop/EventLog/message-text-files).</span><span class="sxs-lookup"><span data-stu-id="f4555-115">For details on creating a message text file, see [Message Text Files](/windows/desktop/EventLog/message-text-files).</span></span> <span data-ttu-id="f4555-116">Gli identificatori di messaggio specificati nel file di testo del messaggio devono corrispondere agli identificatori di risorsa generati dal compilatore di messaggi per le stesse stringhe nel manifesto.</span><span class="sxs-lookup"><span data-stu-id="f4555-116">The message identifiers that you specify in the message text file must match the resource identifiers that the message compiler generated for the same strings in the manifest.</span></span> <span data-ttu-id="f4555-117">Per determinare gli identificatori di risorsa usati per le stringhe nel manifesto, vedere il file con estensione h generato dal compilatore di messaggi durante la compilazione del manifesto.</span><span class="sxs-lookup"><span data-stu-id="f4555-117">To determine the resource identifiers used for the strings in the manifest, see the .h file that the message compiler generated when you compiled the manifest.</span></span>
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


2.  <span data-ttu-id="f4555-118">Eseguire i comandi seguenti per creare la DLL di risorse che contiene le stringhe localizzate.</span><span class="sxs-lookup"><span data-stu-id="f4555-118">Run the following commands to create the resource DLL that contains your localized strings.</span></span> <span data-ttu-id="f4555-119">Il file messages.mc è il file di testo del messaggio creato nel passaggio 1.</span><span class="sxs-lookup"><span data-stu-id="f4555-119">The messages.mc file is the message text file that you created in step 1.</span></span>
    ```cmd
    mc -u -U messages.mc

    rc -r messages.rc

    link -dll -noentry -out:messages.dll messages.res
    ```

    

3.  <span data-ttu-id="f4555-120">Nella cartella che contiene il provider creare una sottocartella per ogni impostazione locale supportata.</span><span class="sxs-lookup"><span data-stu-id="f4555-120">In the folder that contains your provider, create a subfolder for each locale that you support.</span></span> <span data-ttu-id="f4555-121">Il nome della sottocartella deve corrispondere al nome della lingua per le impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="f4555-121">The name of the subfolder must be the language name for that locale.</span></span> <span data-ttu-id="f4555-122">Per 0x0409, ad esempio, usare en-US come nome della cartella.</span><span class="sxs-lookup"><span data-stu-id="f4555-122">For example, for 0x0409, use en-US as the folder name.</span></span>
4.  <span data-ttu-id="f4555-123">Creare un file con estensione rcconfig che indichi allo strumento Muirct.exe che si desidera suddividere le risorse della stringa del messaggio dal file eseguibile e dalle DLL della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f4555-123">Create a .rcconfig file that tells the Muirct.exe tool that you want to split the message string resources from the executable and the resource DLLs.</span></span> <span data-ttu-id="f4555-124">Di seguito è riportato un esempio di file con estensione rcconfig.</span><span class="sxs-lookup"><span data-stu-id="f4555-124">The following is an example .rcconfig file.</span></span>
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
  

5.  <span data-ttu-id="f4555-125">Eseguire i comandi di Muirct.exe seguenti per suddividere le stringhe inglesi dal file eseguibile del provider.</span><span class="sxs-lookup"><span data-stu-id="f4555-125">Run the following Muirct.exe commands to split the English strings from the provider executable file.</span></span>
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x0409 -g 0x0409 provider.exe provider.exe.ln en-US\provider.exe.mui

    muirct -c provider.exe.ln -e en-US\provider.exe.mui
    ```
 

6.  <span data-ttu-id="f4555-126">Eseguire i comandi di Muirct.exe seguenti per suddividere le stringhe francesi dalla DLL della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f4555-126">Run the following Muirct.exe commands to split the French strings from the resource DLL.</span></span> <span data-ttu-id="f4555-127">Rimuovere il file indipendente dalla lingua (fr-FR \\messages.dll) dopo la creazione del file MUI.</span><span class="sxs-lookup"><span data-stu-id="f4555-127">Remove the language neutral file (fr-FR\\messages.dll) after the MUI file is created.</span></span>
    ```cmd
    muirct -q split.rcconfig -v 2 -x 0x040C -g 0x0409 messages.dll fr-FR\messages.dll fr-FR\provider.exe.mui

    muirct -c provider.exe.ln -e fr-FR\provider.exe.mui
    ```
  

7.  <span data-ttu-id="f4555-128">Rinominare provider.exe. LN provider.exe.</span><span class="sxs-lookup"><span data-stu-id="f4555-128">Rename provider.exe.ln to provider.exe.</span></span>