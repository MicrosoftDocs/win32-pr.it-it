---
description: Illustra come implementare un'estensione dello spazio dei nomi shell, inclusi il comportamento del menu di scelta rapida e le attività personalizzate nel browser.
title: Esempio di provider di dati Explorer
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B1B20AF8-3DDE-467b-A49E-A77849CF9F1B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 223f498f42e33dda09206b1e21a44138fda54e261ec957efb62e55148a014d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677838"
---
# <a name="explorer-data-provider-sample"></a>Esempio di provider di dati Explorer

Illustra come implementare un'estensione dello spazio dei nomi shell, inclusi il comportamento del menu di scelta rapida e le attività personalizzate nel browser.

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

| Località      | URL del percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio di ExplorerDataProvider](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/explorerdataprovider) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory **del progetto ExplorerDataProvider.**
2.  Immettere `msbuild ExplorerDataProvider.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta preferita):

1.  Aprire Windows Explorer e passare alla directory **del progetto ExplorerDataProvider.**
2.  Fare doppio clic sull'icona per il file ExplorerDataProvider.sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila** soluzione dal menu **Compila**. La DLL verrà compilata nella \\ directory Debug o Release \\ predefinita.

> [!Note]  
> Nella versione di questo esempio inclusa in Windows SDK, la configurazione per la build di rilascio a 64 bit non include il file ExplorerDataProvider.def nell'opzione **Module Definition File** del linker. È necessario specificare il file manualmente prima di compilare in un ambiente a 64 bit. Aggiungere la riga `ModuleDefinitionFile="ExplorerDataProvider.def"` alla sezione VCLinkerTool (inizia dalla riga 329) del file ExplorerDataProvider.vcproj, come illustrato di seguito:
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
> La versione di questo esempio scaricabile da Code Gallery è stata corretta per questo problema e non è necessaria alcuna azione aggiuntiva da parte dell'utente.
>
>  
>
> ## <a name="running-the-sample"></a>Esecuzione dell'esempio
>
> 1.  Passare alla directory che contiene il nuovo .dll e il file con estensione propdesc, usando il prompt dei comandi o Windows Explorer.
> 2.  Nella riga di comando digitare `regsvr32.exe` .
>     > [!Note]  
>     > Se si esegue questo comando da un prompt dei comandi con privilegi elevati, la registrazione automatica registrerà automaticamente anche il file propdesc. Se viene eseguito da un prompt dei comandi senza privilegi elevati, l'estensione dello spazio dei nomi funzionerà, ma senza funzionalità di proprietà personalizzate.
>
>      
>
> 3.  Aprire la cartella **Computer locale** ed esplorare la nuova estensione dello spazio dei nomi presente in questa cartella.
>
>  
>
>  
>


