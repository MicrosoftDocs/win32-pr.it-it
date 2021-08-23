---
description: Msistuff.exe è un'utilità della riga di comando che può essere usata per visualizzare o configurare le risorse nel Setup.exe eseguibile bootstrap.
ms.assetid: df79574c-d0e7-45e3-97c1-d62f700260ce
title: Msistuff.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a29c3fd904f137679cf1ce42f3718be151e07c3368b03e6f2807dbfc08656ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145624"
---
# <a name="msistuffexe"></a>Msistuff.exe

Msistuff.exe è un'utilità della riga di comando che può essere usata per visualizzare o configurare le risorse nel Setup.exe eseguibile bootstrap.

Questo strumento è disponibile solo nei componenti di [Windows SDK per Windows programma di installazione](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Sintassi

**msistuff setup.exe** *option{value}*

Se non vengono specificati dati dopo un'opzione, tale risorsa viene rimossa.

## <a name="command-line-options"></a>Opzioni da riga di comando

Msistuff.exe usa le opzioni della riga di comando senza distinzione tra maiuscole e minuscole seguenti. È anche possibile usare un delimitatore di barra al posto di un trattino. Se un'opzione è elencata più volte, viene usata solo l'ultima occorrenza.



| Opzione               | ID risorsa                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nessuna opzione specificata |                              | Visualizzare le risorse configurabili in Setup.exe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **-u**               | ISETUPPROPNAME \_ BASEURL      | Impostare BaseURL, il percorso dell'URL di base Setup.exe. Se non è presente alcun valore, per impostazione predefinita la posizione Setup.exe supporti rimovibili. Solo le installazioni basate su URL sono soggette a un controllo con [**WinVerifyTrust.**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust) La barra finale nell'URL è facoltativa. Questa opzione può essere omessa.                                                                                                                                                                                                                     |
| **-d**               | ISETUPPROPNAME \_ DATABASE     | Impostare Msi, il nome del file .msi file. Si tratta di un percorso relativo al file .msi in relazione al percorso del Setup.exe programma. Questa opzione è obbligatoria se l'opzione -m non è specificata. Le opzioni -d e -m si escludono a vicenda. Non è possibile specificare entrambi.                                                                                                                                                                                                                                                    |
| **-m**               | ISETUPPROPNAME \_ PATCH        | Impostare Msp, il nome del file msp. Si tratta di un percorso relativo del file con estensione msp in relazione al percorso del Setup.exe programma. Questa opzione è obbligatoria se l'opzione -d non è specificata. Le opzioni -m e -d si escludono a vicenda. Non è possibile specificare entrambi.                                                                                                                                                                                                                                                    |
| **-n**               | ISETUPPROPNAME \_ PRODUCTNAME  | Impostare Nome prodotto, il nome del prodotto. Fornisce il nome usato nel testo del banner per l'interfaccia utente scaricata. Questa opzione può essere omessa. Se omesso, il valore predefinito è "il prodotto".                                                                                                                                                                                                                                                                                                                            |
| **-o**               | OPERAZIONE \_ ISETUPPROPNAME    | Specificare il tipo di operazione da eseguire. I valori validi sono INSTALL, MINPATCH, MAJPATCH e INSTALLUPD. Per altre informazioni su queste opzioni, vedere [Bootstrap del download Internet.](internet-download-bootstrapping.md)                                                                                                                                                                                                                                                                                           |
| **-v**               | ISETUPPROPNAME \_ MINIMO \_ MSI | Impostare Versione minima msi, la versione minima del Windows installatore richiesto nel computer. Se la versione minima del programma di Windows non è [](instmsi-exe.md) presente nel computer, viene installata la versioneInstmsi.exeper aggiornare il Windows installer. Il valore di questa proprietà ha lo stesso formato del valore PID \_ PAGECOUNT. Vedere [**Proprietà Riepilogo conteggio**](page-count-summary.md) pagine. Il valore deve essere almeno 200, il valore per Windows Installer versione 2.0. Questa opzione è obbligatoria. |
| **-i**               | ISETUPPROPNAME \_ INSTLOCATION | Impostare Percorso URL InstMsi, il percorso DELL'URL di base Windows eseguibili di aggiornamento del programma di installazione. Se questo valore non è presente, il percorso dei file eseguibili di aggiornamento viene impostato per impostazione predefinita sul percorso Setup.exe. Questa opzione può essere omessa.                                                                                                                                                                                                                                                                                                |
| **-a**               | ISETUPPROPNAME \_ INSTMSIA     | Impostare InstMsiA, il nome della versione ANSI del Windows di aggiornamento del programma di installazione. Si tratta di un percorso relativo alla versione ANSI Instmsi.exe rispetto al percorso specificato da ISETUPPROPNAME \_ INSTLOCATION. Questa opzione è obbligatoria.                                                                                                                                                                                                                                                                                   |
| **-w**               | ISETUPPROPNAME \_ INSTMSIW     | Impostare InstMsiW, il nome della versione Unicode del Windows di aggiornamento del programma di installazione. Si tratta di un percorso relativo alla versione Unicode Instmsi.exe rispetto al percorso specificato da ISETUPPROPNAME \_ INSTLOCATION. Questa opzione è obbligatoria.                                                                                                                                                                                                                                                                             |
| **-p**               | PROPRIETÀ \_ ISETUPPROPNAME   | Impostare le stringhe PROPERTY=VALUE. Si tratta delle coppie PROPERTY=VALUE da includere nella riga di comando. Questa opzione può essere omessa. Questa opzione non può essere elencata più volte e deve essere elencata per ultima nella riga di comando. Tutta la riga di comando che segue -p viene considerata come parte di {value}.                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Strumenti di sviluppo del programma di installazione](windows-installer-development-tools.md)
</dt> <dt>

[Bootstrap di download Internet](internet-download-bootstrapping.md)
</dt> <dt>

[Esempio di installazione del Windows basato su URL](a-url-based-windows-installer-installation-example.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 
