---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: A (applicazioni isolate e assembly side-by-side)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41a925d83cf602f5d23c7d043102927748da14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311622"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a>A (applicazioni isolate e assembly side-by-side)

A B C [d](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [i](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**contesto di attivazione**
</dt> <dd>

Struttura di dati in memoria. Ogni sezione di questa struttura contiene i metadati per le funzioni API side-by-side. Ad esempio, una sezione può avere dati di reindirizzamento DLL, che vengono usati dal caricatore della DLL e un altro potrebbe avere dati del server COM. Questi dati possono essere utilizzati per reindirizzare il caricamento di una DLL a una versione specifica, la creazione di un oggetto COM o la creazione di una finestra a una versione più compatibile per l'applicazione.

</dd> <dt>

<span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**configurazione dell'applicazione**
</dt> <dd>

Nomi e versioni degli assembly affiancati necessari per eseguire un'applicazione. Quando un'applicazione viene distribuita con un manifesto, le dipendenze da versioni specifiche degli assembly side-by-side condivise vengono definite in modo esplicito. Per impostazione predefinita, la versione dell'assembly specificata nel manifesto è la versione usata al momento dell'attivazione. Configurazione applicazione globale specifica la configurazione di tutte le applicazioni nel sistema. La configurazione per applicazione può eseguire l'override della configurazione dell'applicazione globale per ogni singola applicazione.

</dd> <dt>

<span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**manifesto di configurazione dell'applicazione**
</dt> <dd>

File che specifica gli assembly affiancati che devono essere utilizzati da un'applicazione completamente o parzialmente isolata. I file manifesto di configurazione dell'applicazione vengono installati nella stessa cartella del file eseguibile dell'applicazione.

</dd> <dt>

<span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**manifesto dell'applicazione**
</dt> <dd>

File che descrive un'applicazione isolata. Specifica le informazioni necessarie per eseguire l'applicazione, incluse le dipendenze da assembly privati, versioni specifiche di assembly e metadati condivisi per gli assembly privati. Il nome di un file manifesto dell'applicazione è il nome dell'eseguibile dell'applicazione seguito da Extension. manifest. Ad esempio, per MySampleApp.exe, il file manifesto sarà MySampleApp.exe. manifest.

</dd> <dt>

<span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**assembly**
</dt> <dd>

Unità di base per la denominazione, l'associazione, il controllo delle versioni, la distribuzione o la configurazione di un blocco di codice di programmazione. Questi assembly di codice possono essere inseriti in dll o assembly COM. Le applicazioni con funzionalità comuni possono eseguire blocchi condivisi del codice di programmazione, detti moduli o assembly di codice. L'infrastruttura per la condivisione sicura degli assembly è detta condivisione degli assembly side-by-side.

</dd> <dt>

<span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**manifesto dell'assembly**
</dt> <dd>

Descrizione di un assembly affiancato. Specifica il nome, la versione, i file, le risorse dell'assembly, i dati di associazione per gli elementi dell'assembly e le dipendenze da altri assembly affiancati. Un file manifesto dell'assembly può avere qualsiasi nome file valido, purché sia seguito da Extension. manifest.

</dd> </dl>

 

 



