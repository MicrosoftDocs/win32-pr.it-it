---
description: Questa sezione descrive le considerazioni per la distribuzione dell'applicazione MUI per un uso ottimale da parte della logica di caricamento dell'applicazione e del caricatore di risorse.
ms.assetid: 6c10b355-9bdd-4dba-8446-91034d4fe9b8
title: Distribuzione dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2023e5fc2dbde51a6ef996126e7557c9ffce8d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319991"
---
# <a name="application-deployment"></a>Distribuzione dell'applicazione

Questa sezione descrive le considerazioni per la distribuzione dell'applicazione MUI per un uso ottimale da parte della logica di caricamento dell'applicazione e del caricatore di risorse.

## <a name="packaging"></a>Packaging

La creazione di pacchetti per l'applicazione dipende dal tipo di supporto della lingua fornito, perché Windows installa i Language Pack in base alle preferenze dell'utente. Se, ad esempio, si è deciso di supportare le impostazioni della lingua di sistema, potrebbe essere necessario fornire il supporto per tutte le lingue in un unico pacchetto, indipendentemente dall'utente previsto.

Se l'applicazione e le risorse sono di grandi dimensioni, è necessario utilizzare un pacchetto per ogni lingua supportata. Ad esempio, è possibile usare questo tipo di creazione pacchetto se l'applicazione presenta lingue selezionabili dall'utente e l'utente deve aggiungere e rimuovere dinamicamente le risorse della lingua.

## <a name="file-placement-on-windows-vista-and-later"></a>Selezione host per file in Windows Vista e versioni successive

In questa sezione viene descritta la posizione dei file per un'applicazione MUI destinata solo a Windows Vista e versioni successive.

### <a name="place-the-ln-file"></a>Inserire il file LN

Un file in tipico per un'applicazione MUI è un file exe o un file con estensione dll, ad esempio BakerDelta.dll. Inserire questo file nella cartella radice in cui è installata l'applicazione, ad esempio, X: \\ \\ <somepath> \\BakerDelta.dll.

### <a name="place-language-specific-resource-files"></a>Inserire i file di risorse Language-Specific

Per i file di risorse specifici della lingua deve essere presente un nome prevedibile formato dall'aggiunta di ". mui" al nome completo del file in, ad esempio BakerDelta.dll. mui. Questi file devono essere inseriti in sottocartelle denominate in base ai [nomi di lingua](language-names.md)appropriati. Nell'esempio seguente viene illustrato il posizionamento delle risorse per il file BakerDelta.dll LN, con file di risorse specifici della lingua per la lingua inglese (Regno Unito), inglese (Stati Uniti), inglese neutro, spagnolo (Spagna), spagnolo (Messico) e spagnolo neutro:

-   X: \\ \\ <somepath> \\BakerDelta.dll
-   X: \\ \\ <somepath> \\ en-GB \\BakerDelta.dll. mui
-   X: \\ \\ <somepath> \\ en-US \\BakerDelta.dll. mui
-   X: \\ \\ <somepath> \\ en \\BakerDelta.dll. mui
-   X: \\ \\ <somepath> \\ es-es \\BakerDelta.dll. mui
-   X: \\ \\ <somepath> \\ es-MX \\BakerDelta.dll. mui
-   X: \\ \\ <somepath> \\ es \\BakerDelta.dll. mui

I file di risorse devono essere inseriti nei percorsi corretti durante l'installazione dell'applicazione MUI o di un pacchetto di lingua. È importante inserire ogni file nella cartella corretta, perché il caricatore di risorse non può funzionare correttamente in caso contrario. Usando l'esempio precedente, il caricatore di risorse esamina X: \\ <somepath> \\ en-US \\BakerDelta.dll. MUI per le risorse in lingua inglese (Stati Uniti). Se il caricatore Cerca in tale file e rileva solo le risorse in lingua spagnola, l'operazione ha esito negativo.

## <a name="file-placement-on-a-pre-windows-vista-operating-system"></a>Posizionamento di file in un sistema operativo precedente a Windows Vista

Un'applicazione da eseguire in un sistema operativo precedente a Windows Vista può utilizzare la convenzione di Windows Vista per inserire i file di risorse specifici della lingua in cartelle in base ai nomi dei linguaggi. In alternativa, l'applicazione può essere conforme a una convenzione precedente che forma i percorsi dagli [identificatori della lingua](language-identifiers.md). Per le applicazioni che supportano solo una singola lingua, è possibile inserire il file di risorse specifico della lingua nella directory radice con il file binario.

Si consideri ad esempio un file in BakerDelta.dll, con file di risorse specifici della lingua per la lingua inglese (Regno Unito), inglese (Stati Uniti), inglese neutro, spagnolo (Spagna), spagnolo (Messico) e spagnolo neutro. Un'installazione in un sistema operativo precedente a Windows Vista potrebbe inserire questi file nel modo seguente:

-   X: \\ \\ <somepath> \\BakerDelta.dll
-   X: \\ \\ <somepath> \\BakerDelta.dll. MUI (file con estensione MUI facoltativo contenente le risorse nella lingua del sistema operativo come fallback finale)
-   X: \\ \\ <somepath> \\ MUI \\ 0809 \\BakerDelta.dll. mui
-   X: \\ \\ <somepath> \\ MUI \\ 0409 \\BakerDelta.dll. mui
-   X: \\ \\ <somepath> \\ MUI \\ 0209 \\BakerDelta.dll. mui
-   X: \\ \\ <somepath> \\ MUI \\ 040a \\BakerDelta.dll. mui
-   X: \\ \\ <somepath> \\ MUI \\ 080A \\BakerDelta.dll. mui
-   X: \\ \\ <somepath> \\ MUI \\ 0209 \\BakerDelta.dll. mui

Oltre a questi file, l'applicazione può configurare un file di risorse specifico per il linguaggio di fallback, che si trova nella stessa cartella dell'applicazione stessa. Per l'esempio precedente, questo file è X: \\ <somepath> \\BakerDelta.dll. mui.

## <a name="installation"></a>Installazione

La logica di installazione per la copia e la configurazione dei file dell'applicazione si basa sulle lingue supportate e sul percorso dei file di risorse della lingua nei percorsi di installazione corretti. Un programma di installazione deve installare e configurare l'applicazione in modo che l'utente possa aggiungere e rimuovere facilmente le lingue.

Se l'applicazione installa semplicemente la lingua del sistema operativo di destinazione, il programma di installazione deve rilevare l'interfaccia utente del sistema operativo per determinare le risorse dell'applicazione da installare. Per supportare la migliore esperienza utente, il programma di installazione deve anche rilevare la lingua dell'interfaccia utente per presentare un'interfaccia utente localizzata per l'installazione.

È consigliabile utilizzare Windows Installer (MSI) per creare il software di installazione. Le risorse associate devono essere incluse nel file di risorse della lingua di base, come descritto in [creazione del file di risorse della lingua di base](creating-the-base-language-resource-file.md). Per istruzioni sull'uso di MSI per preparare il programma di installazione dell'applicazione, vedere [Windows Installer](../msi/windows-installer-portal.md).

## <a name="uninstall-program"></a>Disinstalla programma

Potrebbe anche essere necessario fornire un programma di disinstallazione con l'applicazione MUI. Il servizio MSI è consigliato anche per la creazione di questo programma. Per istruzioni sull'utilizzo di MSI per preparare il software di disinstallazione, vedere [Windows Installer](../msi/windows-installer-portal.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dell'interfaccia utente multilingue](using-multilingual-user-interface.md)
</dt> </dl>

 

 
