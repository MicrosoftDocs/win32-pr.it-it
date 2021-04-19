---
description: Un assembly privato è un assembly distribuito con un'applicazione ed è disponibile per l'utilizzo esclusivo di tale applicazione.
ms.assetid: 5E0E7423-85BD-4ED0-9149-9541F4D2371F
title: Informazioni sugli assembly privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7ccfe8c63a8435a33085f607c2040a0a42345c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311621"
---
# <a name="about-private-assemblies"></a>Informazioni sugli assembly privati

Un assembly privato è un assembly distribuito con un'applicazione ed è disponibile per l'utilizzo esclusivo di tale applicazione. Ovvero, le altre applicazioni non condividono l'assembly privato. Gli assembly privati sono uno dei metodi che possono essere utilizzati per creare [applicazioni isolate](isolated-applications.md). Per ulteriori informazioni, vedere [informazioni sulle applicazioni isolate e gli assembly affiancati](about-isolated-applications-and-side-by-side-assemblies.md).

Gli assembly privati devono essere progettati per funzionare side-by-side con altre versioni dell'assembly nel sistema. Per ulteriori informazioni, vedere [linee guida per la creazione di assembly affiancati](guidelines-for-creating-side-by-side-assemblies.md).

Gli assembly privati devono essere accompagnati da un [manifesto dell'assembly](assembly-manifests.md). Si noti che le restrizioni relative ai nomi si applicano quando si crea il pacchetto di una DLL come assembly privato per gestire il modo in cui Windows cerca gli assembly privati. Quando si cercano gli assembly privati, il metodo consigliato consiste nell'includere il manifesto dell'assembly nella DLL come risorsa. In questo caso, l'ID risorsa deve essere uguale a 1 e il nome dell'assembly privato può corrispondere al nome della DLL. Se, ad esempio, il nome della DLL è MICROSOFT.WINDOWS.MYSAMPLE.DLL, anche il valore dell'attributo Name usato nell'elemento **assemblyIdentity** del manifesto potrebbe essere Microsoft. Windows. di esempio. Un metodo alternativo per la ricerca di assembly privati consiste nel fornire il manifesto dell'assembly in un file separato. In questo caso, il nome dell'assembly e il relativo manifesto devono essere diversi dal nome della DLL. Ad esempio, Microsoft. Windows. mysampleAsm, Microsoft. Windows. mysampleAsm. manifest e Microsoft.Windows.mysample.dll. Per ulteriori informazioni sul modo in cui le ricerche affiancate degli assembly privati, vedere [sequenza di ricerca degli assembly](assembly-searching-sequence.md).

Gli assembly privati vengono installati in una cartella della struttura di directory dell'applicazione. Si tratta in genere della cartella che contiene il file eseguibile dell'applicazione. Gli assembly privati possono essere distribuiti nella stessa cartella dell'applicazione, in una cartella con lo stesso nome dell'assembly o in una sottocartella specifica del linguaggio con lo stesso nome dell'assembly. Usare, ad esempio, una delle seguenti strutture di directory per distribuire un assembly privato, Microsoft. Tools. pop, senza alcuna lingua specificata.



| Struttura di directory                                       | Descrizione                                                                                            |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| \\MICROSOFT.TOOLS.POP.DLL appdir                           | Il manifesto viene distribuito come risorsa nella DLL.                                                     |
| Appdir \\ Microsoft. Tools. pop. manifest                      | Il manifesto viene distribuito come file separato.                                                           |
| APPDIR \\ Microsoft. Strumenti. \\MICROSOFT.TOOLS.POP.DLL pop      | Il manifesto viene distribuito come risorsa nella DLL, che si trova in una sottocartella con il nome dell'assembly. |
| Appdir \\ Microsoft. Tools. pop \\ Microsoft. Tools. pop. manifest | Il manifesto viene distribuito come file separato in una sottocartella con il nome dell'assembly.                 |



 

> [!IMPORTANT]
>
> Per le versioni del sistema operativo Windows precedenti a Windows 7 e Windows Server 2008 R2, gli assembly privati nativi devono essere distribuiti nella cartella che contiene il file eseguibile dell'applicazione. L'installazione in una cartella specifica del linguaggio o nella cartella con lo stesso nome dell'assembly non è supportata per gli assembly privati nativi.

 

Utilizzare una delle seguenti strutture di directory per distribuire un assembly privato, Microsoft. Tools. pop, con una lingua specificata. Nell'esempio seguente il linguaggio usato da Microsoft. Tools. pop è l'inglese (Stati Uniti) e il codice della lingua è en-US. È necessario sostituire il codice della lingua DHTML corretto per l'assembly.

``` syntax
appdir\en-us\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop.MANIFEST
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.MANIFEST
```

Gli assembly privati possono essere installati da qualsiasi metodo di installazione in grado di copiare il file dell'assembly in questa cartella, ad esempio il comando **xcopy** . Per altre informazioni su come installare gli assembly privati usando il Windows Installer, vedere [installazione degli assembly Win32](../msi/installation-of-win32-assemblies.md).

Gli assembly privati possono anche essere installati nei sistemi operativi precedenti a Windows XP. In questo caso, è necessario che l'assembly sia registrato e che in questi sistemi operativi non venga utilizzato il manifesto. Una copia dell'assembly privato viene installata in una cartella privata per l'uso esclusivo dell'applicazione. Un'altra versione dell'assembly può essere registrata a livello globale nel sistema e disponibile per qualsiasi applicazione associata a tale assembly. La versione globale dell'assembly può essere la versione installata con l'applicazione o una versione precedente. Per ulteriori informazioni, vedere la pagina [relativa al reindirizzamento DLL/com in Windows](dll-com-redirection-on-windows.md). Un assembly può essere installato anche come assembly condiviso per l'uso da più applicazioni. Per altre informazioni, vedere [assembly condivisi](/windows/desktop/Msi/shared-assemblies).

Si noti che i passaggi per la creazione di un assembly privato sono identici a quelli per la creazione di un assembly condiviso con due eccezioni:

-   Non è necessario firmare un assembly privato e **publickeyToken** non è necessario nell'elemento **assemblyIdentity** del manifesto dell'assembly.
-   Gli assembly privati possono essere installati nella cartella dell'applicazione usando qualsiasi tecnologia di installazione. Non è necessario installare assembly privati usando il Windows Installer.

 

 
