---
description: Viene illustrato come implementare un'estensione dello spazio dei nomi della shell, inclusi il comportamento del menu di scelta rapida e le attività personalizzate nel browser.
title: Esempio di provider di dati Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6bd15cbef62ff69efcccd28fcb625fc1432fdf89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233566"
---
# <a name="explorer-data-provider-sample"></a>Esempio di provider di dati Explorer

Viene illustrato come implementare un'estensione dello spazio dei nomi della shell, inclusi il comportamento del menu di scelta rapida e le attività personalizzate nel browser.

In questo argomento sono contenute le sezioni seguenti.

-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 6.1                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Location      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio ExplorerDataProvider](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **ExplorerDataProvider** .
2.  Immettere `msbuild ExplorerDataProvider.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **ExplorerDataProvider** .
2.  Fare doppio clic sull'icona per il file ExplorerDataProvider. sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila soluzione** dal menu **Compila** . La DLL verrà compilata nella \\ directory di debug o di \\ versione predefinita.

> [!Note]  
> Nella versione di questo esempio inclusa nella Windows SDK la configurazione per la build di rilascio a 64 bit non include il file ExplorerDataProvider. def nell'opzione del **file di definizione del modulo** del linker. È necessario specificare il file manualmente prima della compilazione in un ambiente a 64 bit. Aggiungere la riga `ModuleDefinitionFile="ExplorerDataProvider.def"` alla sezione VCLinkerTool (inizia alla riga 329) del file ExplorerDataProvider. vcproj, come illustrato di seguito:
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>LinkIncremental=&quot;1&quot;
> AdditionalLibraryDirectories=&quot;&quot;c:\Program Files\Microsoft SDKs\Windows\v6.0\Lib\x64&quot;&quot;
> ModuleDefinitionFile=&quot;ExplorerDataProvider.def&quot;
> GenerateDebugInformation=&quot;true&quot;</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> La versione di questo esempio scaricabile dalla raccolta codici è stata corretta per questo problema e non è richiesta alcuna azione aggiuntiva da parte dell'utente.
>
>  
>
> ## <a name="running-the-sample"></a>Esecuzione dell'esempio
>
> 1.  Passare alla directory che contiene il nuovo file. dll e. propdesc, utilizzando il prompt dei comandi o Esplora risorse.
> 2.  Nella riga di comando digitare `regsvr32.exe` .
>     > [!Note]  
>     > Se si esegue questo comando da un prompt dei comandi con privilegi elevati, la registrazione automatica registrerà automaticamente anche il file con estensione propdesc. Se viene eseguito da un prompt dei comandi non con privilegi elevati, l'estensione dello spazio dei nomi funzionerà, ma senza la funzionalità personalizzata della proprietà.
>
>      
>
> 3.  Aprire la cartella **computer locale** e visualizzare la nuova estensione dello spazio dei nomi presente in tale cartella.
>
>  
>
>  
>


