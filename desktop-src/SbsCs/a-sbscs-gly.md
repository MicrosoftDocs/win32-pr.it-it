---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: A (applicazioni isolate e assembly side-by-side)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac40ba2393bb2d043957e04b8d34ca93fede605bbcd11ad601667e97f79f057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142722"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a>A (applicazioni isolate e assembly side-by-side)

A B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**contesto di attivazione**
</dt> <dd>

Struttura di dati in memoria. Ogni sezione di questa struttura contiene i metadati per le funzioni API side-by-side. Ad esempio, una sezione può avere dati di reindirizzamento DLL, che vengono usati dal caricatore DLL, e un'altra può avere dati del server COM. Questi dati possono essere usati per reindirizzare il caricamento di una DLL a una versione specifica, la creazione di un oggetto COM o la creazione di una finestra a una versione più compatibile per l'applicazione.

</dd> <dt>

<span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**configurazione dell'applicazione**
</dt> <dd>

Nomi e versioni degli assembly side-by-side necessari per eseguire un'applicazione. Quando un'applicazione viene distribuita con un manifesto, le dipendenze da versioni specifiche di assembly side-by-side condivisi vengono definite in modo esplicito. Per impostazione predefinita, la versione dell'assembly specificata nel manifesto è la versione usata al momento dell'attivazione. La configurazione globale dell'applicazione specifica la configurazione di tutte le applicazioni nel sistema. La configurazione per applicazione può eseguire l'override della configurazione globale dell'applicazione per ogni applicazione.

</dd> <dt>

<span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**manifesto di configurazione dell'applicazione**
</dt> <dd>

File che specifica gli assembly side-by-side che devono essere utilizzati da un'applicazione completamente o parzialmente isolata. I file manifesto di configurazione dell'applicazione vengono installati nella stessa cartella del file eseguibile dell'applicazione.

</dd> <dt>

<span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**manifesto dell'applicazione**
</dt> <dd>

File che descrive un'applicazione isolata. Specifica le informazioni necessarie per eseguire l'applicazione, incluse le dipendenze da assembly privati, versioni specifiche di assembly condivisi e metadati per gli assembly privati. Il nome di un file manifesto dell'applicazione è il nome del file eseguibile dell'applicazione seguito dall'estensione manifest. Ad esempio, per MySampleApp.exe, il file manifesto sarà MySampleApp.exe.manifest.

</dd> <dt>

<span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**Assemblea**
</dt> <dd>

Unità fondamentale per la denominazione, l'associazione, il controllo delle versioni, la distribuzione o la configurazione di un blocco di codice di programmazione. Questi assembly di codice possono essere inseriti in DLL o assembly COM. Le applicazioni con funzionalità comuni possono eseguire blocchi condivisi di codice di programmazione definiti moduli o assembly di codice. L'infrastruttura per la condivisione sicura degli assembly è detta condivisione di assembly side-by-side.

</dd> <dt>

<span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**manifesto dell'assembly**
</dt> <dd>

Descrizione di un assembly side-by-side. Specifica il nome, la versione, i file, le risorse dell'assembly, i dati di associazione per gli elementi dell'assembly e le dipendenze da altri assembly side-by-side. Un file manifesto dell'assembly può avere qualsiasi nome di file valido, purché sia seguito dall'estensione manifest.

</dd> </dl>

 

 



