---
description: Un assembly privato è un assembly distribuito con un'applicazione ed è disponibile per l'uso esclusivo di tale applicazione.
ms.assetid: 5E0E7423-85BD-4ED0-9149-9541F4D2371F
title: Informazioni sugli assembly privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c785b30ca8654071a9816aaf9a11ecc69a029f605d06f39f44a6a490a2a7aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142614"
---
# <a name="about-private-assemblies"></a>Informazioni sugli assembly privati

Un assembly privato è un assembly distribuito con un'applicazione ed è disponibile per l'uso esclusivo di tale applicazione. In altre parole, altre applicazioni non condividono l'assembly privato. Gli assembly privati sono uno dei metodi che possono essere usati per creare [applicazioni isolate.](isolated-applications.md) Per altre informazioni, vedere [Informazioni sulle applicazioni isolate e sugli assembly side-by-side.](about-isolated-applications-and-side-by-side-assemblies.md)

Gli assembly privati devono essere progettati per funzionare side-by-side con altre versioni dell'assembly nel sistema. Per altre informazioni, vedere [Linee guida per la creazione di assembly side-by-side.](guidelines-for-creating-side-by-side-assemblies.md)

Gli assembly privati devono essere accompagnati da un manifesto [dell'assembly](assembly-manifests.md). Si noti che le restrizioni relative ai nomi si applicano durante la creazione del pacchetto di una DLL come assembly privato per supportare la modalità Windows ricerca di assembly privati. Quando si cercano assembly privati, il metodo consigliato è includere il manifesto dell'assembly nella DLL come risorsa. In questo caso, l'ID risorsa deve essere uguale a 1 e il nome dell'assembly privato può corrispondere al nome della DLL. Ad esempio, se il nome della DLL è MICROSOFT.WINDOWS.MYSAMPLE.DLL, anche il valore dell'attributo name usato nell'elemento **assemblyIdentity** del manifesto può essere Microsoft. Windows.mysample. Un metodo alternativo per la ricerca di assembly privati è fornire il manifesto dell'assembly in un file separato. In questo caso, il nome dell'assembly e il relativo manifesto devono essere diversi dal nome della DLL. Ad esempio, Microsoft. Windows.mysampleAsm, Microsoft. Windows.mysampleAsm.manifest e Microsoft.Windows.mysample.dll. Per altre informazioni sulla modalità di ricerca side-by-side degli assembly privati, vedere [Sequenza di ricerca di assembly.](assembly-searching-sequence.md)

Gli assembly privati vengono installati in una cartella della struttura di directory dell'applicazione. In genere, si tratta della cartella contenente il file eseguibile dell'applicazione. Gli assembly privati possono essere distribuiti nella stessa cartella dell'applicazione, in una cartella con lo stesso nome dell'assembly o in una sottocartella specifica del linguaggio con lo stesso nome dell'assembly. Ad esempio, usare una delle strutture di directory seguenti per distribuire un assembly privato, Microsoft.tools.pop, senza alcun linguaggio specificato.



| Struttura di directory                                       | Descrizione                                                                                            |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| AppDIR \\MICROSOFT.TOOLS.POP.DLL                           | Il manifesto viene distribuito come risorsa nella DLL.                                                     |
| Appdir \\ Microsoft.Tools.Pop.MANIFEST                      | Il manifesto viene distribuito come file separato.                                                           |
| APPDIR \\ MICROSOFT. Strumenti. Pop \\MICROSOFT.TOOLS.POP.DLL      | Il manifesto viene distribuito come risorsa nella DLL, che si trova in una sottocartella con il nome dell'assembly. |
| Appdir \\ Microsoft.Tools.Pop \\ Microsoft.Tools.Pop.MANIFEST | Il manifesto viene distribuito come file separato in una sottocartella con il nome dell'assembly.                 |



 

> [!IMPORTANT]
>
> Per le versioni del sistema operativo Windows precedenti Windows 7 e Windows Server 2008 R2, gli assembly privati nativi devono essere distribuiti nella cartella che contiene il file eseguibile dell'applicazione. L'installazione in una cartella specifica del linguaggio o nella cartella con lo stesso nome dell'assembly non è supportata per gli assembly privati nativi.

 

Usare una delle strutture di directory seguenti per distribuire un assembly privato, Microsoft.tools.pop, con una lingua specificata. Nell'esempio seguente la lingua usata da Microsoft.Tools.Pop è l'inglese (Stati Uniti) e il codice lingua è en-us. È necessario sostituire il codice del linguaggio DHTML corretto per l'assembly.

``` syntax
appdir\en-us\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop.MANIFEST
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.DLL
appdir\en-us\Microsoft.tools.pop\Microsoft.tools.pop.MANIFEST
```

Gli assembly privati possono essere installati da qualsiasi metodo di installazione in grado di copiare il file dell'assembly in questa cartella, ad esempio il **comando xcopy.** Per altre informazioni su come installare assembly privati usando il programma di Windows, vedere Installazione di [assembly Win32.](../msi/installation-of-win32-assemblies.md)

Gli assembly privati possono essere installati anche in sistemi operativi precedenti a Windows XP. In questo caso, l'assembly deve essere registrato e in questi sistemi operativi il manifesto non viene usato. Una copia dell'assembly privato viene installata in una cartella privata per l'uso esclusivo dell'applicazione. Un'altra versione dell'assembly può essere registrata a livello globale nel sistema e disponibile per qualsiasi applicazione associata. La versione globale dell'assembly può essere la versione installata con l'applicazione o una versione precedente. Per altre informazioni, vedere [Reindirizzamento DLL/COM Windows](dll-com-redirection-on-windows.md). Un assembly può anche essere installato come assembly condiviso per l'uso da parte di più applicazioni. Per altre informazioni, vedere [Assembly condivisi.](/windows/desktop/Msi/shared-assemblies)

Si noti che i passaggi per la creazione di un assembly privato sono identici a quelli per la creazione di un assembly condiviso con due eccezioni:

-   Non è necessario che un assembly privato sia firmato e **publickeyToken** non è necessario **nell'elemento assemblyIdentity** del manifesto dell'assembly.
-   Gli assembly privati possono essere installati nella cartella dell'applicazione usando qualsiasi tecnologia di installazione. Gli assembly privati non devono essere installati tramite il programma di Windows installazione.

 

 
