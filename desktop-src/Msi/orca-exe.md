---
description: Orca.exe è un editor di tabelle di database per la creazione e la modifica di Windows Installer pacchetti e Unione di moduli.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3f17874e08fcdbfdbab38c480219579897b9896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049430"
---
# <a name="orcaexe"></a>Orca.exe

Orca.exe è un editor di tabelle di database per la creazione e la modifica di Windows Installer pacchetti e Unione di moduli. Lo strumento fornisce un'interfaccia grafica per la convalida, evidenziando le voci specifiche in cui si verificano errori o avvisi di convalida.

Questo strumento è disponibile solo nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md). Viene fornito come file di Orca.msi. Dopo aver installato i componenti Windows SDK per gli sviluppatori di Windows Installer, fare doppio clic su Orca.msi per installare il file Orca.exe.

## <a name="syntax"></a>Sintassi

**Orca***\[<options>\]\[<source file>\]*

## <a name="command-line-options"></a>Opzioni da riga di comando

Orca.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole. Al posto di un trattino, può essere utilizzato anche un delimitatore di barra.



| Opzione | Descrizione                                                 |
|--------|-------------------------------------------------------------|
| -Q     | Modalità non interattiva                                                  |
| -S     | <*Database Schema>* database \[ "Orca. dat"-predefinito\] |
| -?     | Finestra di dialogo della Guida                                                 |



 

Orca.exe usa le seguenti opzioni della riga di comando senza distinzione tra maiuscole e minuscole con i moduli merge. Al posto di un trattino, può essere utilizzato anche un delimitatore di barra. Quando si esegue un'operazione di merge, il valore-f,-m e <*sourcefile*> sono tutti obbligatori.



| Opzione     | Descrizione                                                                |
|------------|----------------------------------------------------------------------------|
| -c         | Eseguire il commit del merge nel database se non si verificano errori.                                     |
| -!         | Eseguire il commit del merge in un database anche in caso di errori.                       |
| -M         | <*modulo> Unione* del modulo da unire nel database.                      |
| -f         | Funzionalità \[ : \] funzionalità di Funzionalità2 per la connessione al modulo merge.                |
| -r         | <*ID directory*> voce di directory per il reindirizzamento radice del modulo.    |
| -X         | <*directory*> estrarre i file in un'immagine nella directory.         |
| -g         | <*lingua> lingua* utilizzata per aprire un modulo.                         |
| -l         | <file di *log*> file da utilizzare come log, aggiungere se esiste già.      |
| -i         | <*directory*> estrarre i file nell'immagine di origine sotto la directory. |
| -CAB       | <*filename*> estrarre il file CAB msm nel file.                        |
| -LFN       | Usare nomi di file lunghi durante l'estrazione.                                 |
| -Configura | <*filename*> configurare il modulo usando i dati di un file.            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Strumenti di sviluppo Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



