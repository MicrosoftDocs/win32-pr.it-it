---
description: Questa sezione descrive le considerazioni per la distribuzione dell'applicazione MUI per un uso ottimale da parte della logica di caricamento dell'applicazione e del caricatore di risorse.
ms.assetid: 6c10b355-9bdd-4dba-8446-91034d4fe9b8
title: Distribuzione dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb2d7605a2c6a39629749c00d175be4df8a3c66d8b0dc6c870926ec665d9ce6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041611"
---
# <a name="application-deployment"></a>Distribuzione dell'applicazione

Questa sezione descrive le considerazioni per la distribuzione dell'applicazione MUI per un uso ottimale da parte della logica di caricamento dell'applicazione e del caricatore di risorse.

## <a name="packaging"></a>Packaging

La creazione di pacchetti per l'applicazione dipende dal tipo di supporto linguistico fornito, Windows i Language Pack in base alle preferenze dell'utente. Ad esempio, se si è deciso di supportare le impostazioni della lingua di sistema, è possibile fornire tutto il supporto linguistico in un singolo pacchetto, indipendentemente dall'utente desiderato.

Se l'applicazione e le risorse sono di grandi dimensioni, è consigliabile usare un pacchetto per ogni lingua supportata. Ad esempio, è possibile usare questo tipo di creazione di pacchetti se l'applicazione presenta lingue selezionabili dall'utente e l'utente necessita di aggiunta e rimozione dinamica delle risorse linguistiche.

## <a name="file-placement-on-windows-vista-and-later"></a>Posizionamento dei file Windows Vista e versioni successive

Questa sezione descrive il posizionamento dei file per un'applicazione MUI destinata solo Windows Vista e versioni successive.

### <a name="place-the-ln-file"></a>Inserire il file LN

Un file LN tipico per un'applicazione MUI è un file .exe o un file .dll, ad esempio BakerDelta.dll. È necessario inserire questo file nella cartella radice in cui è installata l'applicazione, ad esempio X: \\ \\ <somepath> \\BakerDelta.dll.

### <a name="place-language-specific-resource-files"></a>Inserire Language-Specific file di risorse

I file di risorse specifici della lingua devono avere nomi stimabili formati aggiungendo ".mui" al nome completo del file LN, ad esempio BakerDelta.dll.mui. Questi file devono essere inseriti in sottocartelle denominate in base ai nomi [di lingua appropriati.](language-names.md) L'esempio seguente illustra il posizionamento delle risorse per il file LN BakerDelta.dll, con file di risorse specifici della lingua per inglese (Regno Unito), inglese (Stati Uniti), inglese neutro, spagnolo (Spagna), spagnolo (Messico) e spagnolo neutro:

-   X: \\ \\ <somepath> \\BakerDelta.dll
-   X: \\ \\ <somepath> \\ en-GB \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ en-US \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ en \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ es-ES \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ es-MX \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ es \\BakerDelta.dll.mui

I file di risorse devono essere posizionati nei percorsi corretti durante l'installazione dell'applicazione MUI o di un pacchetto linguistico. È importante inserire ogni file nella cartella corretta, perché il caricatore di risorse non può funzionare correttamente in caso contrario. Usando l'esempio precedente, il caricatore di risorse esamina le risorse X: \\ <somepath> \\ en-USBakerDelta.dll.mui per l'inglese \\ (Stati Uniti). Se il caricatore cerca nel file e rileva solo risorse in lingua spagnola, l'operazione ha esito negativo.

## <a name="file-placement-on-a-pre-windows-vista-operating-system"></a>Posizionamento dei file in un sistema operativo Windows Vista preliminare

Un'applicazione da eseguire in un sistema operativo Windows Vista precedente può usare la convenzione di Windows Vista per inserire file di risorse specifici della lingua nelle cartelle in base ai nomi delle lingue. In alternativa, l'applicazione può essere conforme a una convenzione precedente che forma i percorsi dagli [identificatori del linguaggio](language-identifiers.md). Per le applicazioni che supportano una sola lingua, è sufficiente inserire il file di risorse specifico della lingua nella directory radice con il file binario.

Si consideri ad esempio un file LN denominato BakerDelta.dll, con file di risorse specifici della lingua per inglese (Regno Unito), inglese (Stati Uniti), inglese neutro, spagnolo (Spagna), spagnolo (Messico) e spagnolo neutro. Un'installazione in un sistema operativo Windows Vista precedente potrebbe inserire questi file nel modo seguente:

-   X: \\ \\ <somepath> \\BakerDelta.dll
-   X: \\ \\ <somepath>BakerDelta.dll.mui (file con estensione mui facoltativo contenente le risorse nella lingua del sistema operativo come \\ fallback finale)
-   X: \\ \\ <somepath> \\ MUI \\ 0809 \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ MUI \\ 0409 \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ MUI \\ 0209 \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ MUI \\ 040a \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ MUI \\ 080a \\BakerDelta.dll.mui
-   X: \\ \\ <somepath> \\ MUI \\ 0209 \\BakerDelta.dll.mui

Oltre a questi file, l'applicazione può configurare un file di risorse specifico della lingua di fallback finale, per risiedere nella stessa cartella dell'applicazione stessa. Per l'esempio precedente, questo file è X: \\ <somepath> \\BakerDelta.dll.mui.

## <a name="installation"></a>Installazione

La logica di installazione per la copia e la configurazione dei file dell'applicazione si basa sulle lingue supportate e sul percorso dei file di risorse di lingua nei percorsi di installazione corretti. Un programma di installazione deve installare e configurare l'applicazione in modo che l'utente possa aggiungere e rimuovere facilmente le lingue.

Se l'applicazione installa semplicemente la lingua del sistema operativo di destinazione, il programma di installazione deve rilevare l'interfaccia utente del sistema operativo per determinare le risorse dell'applicazione da installare. Per supportare la migliore esperienza utente, il programma di installazione deve anche rilevare la lingua dell'interfaccia utente per presentare un'interfaccia utente localizzata per l'installazione stessa.

È consigliabile usare il Windows installer (MSI) per creare il software di installazione. Le risorse associate devono essere incluse nel file di risorse della lingua di base, come descritto in Creazione del file di [risorse della lingua di base](creating-the-base-language-resource-file.md). Per istruzioni sull'uso dell'msi per preparare il programma di installazione dell'applicazione, vedere [Windows Installer](../msi/windows-installer-portal.md).

## <a name="uninstall-program"></a>Disinstallare il programma

È anche possibile fornire un programma di disinstallazione con l'applicazione MUI. Msi è consigliato anche per la creazione di questo programma. Per istruzioni sull'uso di MSI per preparare il software di disinstallazione, vedere [Windows Installer](../msi/windows-installer-portal.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di interfaccia utente multilingue](using-multilingual-user-interface.md)
</dt> </dl>

 

 
