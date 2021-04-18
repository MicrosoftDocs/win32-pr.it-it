---
description: Msistuff.exe è un'utilità della riga di comando che può essere utilizzata per visualizzare o configurare le risorse nell'eseguibile di bootstrap Setup.exe.
ms.assetid: df79574c-d0e7-45e3-97c1-d62f700260ce
title: Msistuff.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b56d6b183128971501fd3ad8ddb7a88d08cee70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316258"
---
# <a name="msistuffexe"></a>Msistuff.exe

Msistuff.exe è un'utilità della riga di comando che può essere utilizzata per visualizzare o configurare le risorse nell'eseguibile di bootstrap Setup.exe.

Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Sintassi

**msistuff setup.exe** *opzione {value}*

Se non viene specificato alcun dato dopo un'opzione, la risorsa viene rimossa.

## <a name="command-line-options"></a>Opzioni da riga di comando

Msistuff.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole. Al posto di un trattino, può essere utilizzato anche un delimitatore di barra. Se un'opzione è elencata più volte, viene utilizzata solo l'ultima occorrenza.



| Opzione               | ID risorsa                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nessuna opzione specificata |                              | Visualizza le risorse configurabili in Setup.exe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **-u**               | \_BASEURL ISETUPPROPNAME      | Impostare BaseURL, il percorso dell'URL di base del Setup.exe. Se non è presente alcun valore, il percorso di Setup.exe viene impostato su un supporto rimovibile. Solo le installazioni basate su URL sono soggette a un controllo con [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust). La barra finale nell'URL è facoltativa. Questa opzione può essere omessa.                                                                                                                                                                                                                     |
| **-d**               | \_database ISETUPPROPNAME     | Impostare MSI, il nome del file con estensione msi. Si tratta di un percorso relativo del file con estensione msi in relazione al percorso del programma Setup.exe. Questa opzione è obbligatoria se non si specifica l'opzione-m. Le opzioni-d e-m si escludono a vicenda. Non possono essere specificati entrambi.                                                                                                                                                                                                                                                    |
| **-m**               | \_patch ISETUPPROPNAME        | Impostare msp, il nome del file con estensione msp. Si tratta di un percorso relativo del file con estensione msp in relazione al percorso del programma Setup.exe. Questa opzione è obbligatoria se non si specifica l'opzione-d. Le opzioni-m e-d si escludono a vicenda. Non possono essere specificati entrambi.                                                                                                                                                                                                                                                    |
| **-n**               | ISETUPPROPNAME \_ ProductName  | Impostare nome prodotto, il nome del prodotto. Fornisce il nome usato nel testo del banner per l'interfaccia utente scaricata. Questa opzione può essere omessa. Se omesso, il valore predefinito è "The Product".                                                                                                                                                                                                                                                                                                                            |
| **-o**               | \_operazione ISETUPPROPNAME    | Consente di specificare il tipo di operazione da eseguire. I valori validi sono INSTALL, MINPATCH, MAJPATCH e INSTALLUPD. Per ulteriori informazioni su queste opzioni, vedere [bootstrap di download Internet](internet-download-bootstrapping.md).                                                                                                                                                                                                                                                                                           |
| **-v**               | \_MSI minimo \_ ISETUPPROPNAME | Impostare la versione minima di MSI, ovvero la versione minima di Windows Installer richiesta nel computer. Se la versione minima del Windows Installer non è presente nel computer, per aggiornare il Windows Installer viene installato il [Instmsi.exe](instmsi-exe.md) appropriato. Il valore di questa proprietà ha lo stesso formato del valore di \_ PageCount PID. Vedere Proprietà di [**Riepilogo del conteggio delle pagine**](page-count-summary.md) . Il valore deve essere almeno 200, il valore per la Windows Installer versione 2,0. Questa opzione è obbligatoria. |
| **-i**               | \_INSTLOCATION ISETUPPROPNAME | Impostare il percorso dell'URL di InstMsi, il percorso dell'URL di base dei file eseguibili di aggiornamento Windows Installer. Se questo valore non è presente, per impostazione predefinita il percorso dei file eseguibili di aggiornamento è il percorso del Setup.exe. Questa opzione può essere omessa.                                                                                                                                                                                                                                                                                                |
| **-a**               | \_instmsia ISETUPPROPNAME     | Impostare InstMsiA, il nome della versione ANSI di Windows Installer eseguibile di aggiornamento. Si tratta di un percorso relativo della versione ANSI di Instmsi.exe rispetto al percorso specificato da ISETUPPROPNAME \_ INSTLOCATION. Questa opzione è obbligatoria.                                                                                                                                                                                                                                                                                   |
| **-w**               | \_Instmsiw ISETUPPROPNAME     | Impostare InstMsiW, il nome della versione Unicode di Windows Installer eseguibile di aggiornamento. Si tratta di un percorso relativo della versione Unicode di Instmsi.exe rispetto al percorso specificato da ISETUPPROPNAME \_ INSTLOCATION. Questa opzione è obbligatoria.                                                                                                                                                                                                                                                                             |
| **-p**               | Proprietà di ISETUPPROPNAME \_   | Impostare le stringhe PROPERTY = VALUE. Queste sono le coppie proprietà = valore da includere nella riga di comando. Questa opzione può essere omessa. Questa opzione non può essere elencata più volte e deve essere elencata per ultima nella riga di comando. Tutta la riga di comando che segue-p viene considerata come parte del {valore}.                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di sviluppo Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Bootstrap di download Internet](internet-download-bootstrapping.md)
</dt> <dt>

[Esempio di installazione di Windows Installer basato su URL](a-url-based-windows-installer-installation-example.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 
