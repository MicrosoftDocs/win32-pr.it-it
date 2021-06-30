---
description: Orca.exe è un editor di tabelle di database per la creazione e la modifica di Windows Installer pacchetti e moduli unione.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4647b137650bfba521dba3976ea7a1ae66451ce
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102160"
---
# <a name="orcaexe"></a>Orca.exe

Orca.exe è un editor di tabelle di database per la creazione e la modifica di Windows Installer pacchetti e moduli unione. Lo strumento fornisce un'interfaccia grafica per la convalida, evidenziando le voci specifiche in cui si verificano errori o avvisi di convalida.

Questo strumento è disponibile solo nella pagina [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md). Viene fornito come file Orca.msi. Dopo aver installato i componenti Windows SDK per Windows Installer, fare doppio clic su Orca.msi per installare il file Orca.exe.

## <a name="syntax"></a>Sintassi

**orca***\[\<options>\]\[\<source file>\]*

## <a name="command-line-options"></a>Opzioni da riga di comando

Orca.exe usa le opzioni della riga di comando seguenti senza distinzione tra maiuscole e minuscole. È anche possibile usare un delimitatore barra al posto di un trattino.



| Opzione | Descrizione                                                 |
|--------|-------------------------------------------------------------|
| -Q     | Modalità non interattiva                                                  |
| -S     | <*database*> Schema database \[ "orca.dat": impostazione predefinita\] |
| -?     | Finestra di dialogo Della Guida                                                 |



 

Orca.exe usa le opzioni della riga di comando seguenti senza distinzione tra maiuscole e minuscole con i moduli unione. È anche possibile usare un delimitatore barra al posto di un trattino. Quando si esegue un'unione, sono necessari i <-f, -m *> sourcefile.*



| Opzione     | Descrizione                                                                |
|------------|----------------------------------------------------------------------------|
| -c         | Eseguire il commit del merge nel database se non si verificano errori.                                     |
| -!         | Eseguire il commit del merge in un database anche se sono presenti errori.                       |
| -M         | <*Modulo>* Merge Module da unire nel database.                      |
| -f         | \[Funzionalità:Funzionalità2 \] Funzionalità per la connessione al modulo di unione.                |
| -r         | <*ID directory>* directory per il reindirizzamento radice del modulo.    |
| -X         | <*directory*> estrai i file in un'immagine nella directory .         |
| -g         | <*language*> linguaggio usato per aprire un modulo.                         |
| -l         | <*file di log*> file da usare come log, aggiungere se esiste già.      |
| -i         | <*directory*> estrai i file nell'immagine di origine nella directory . |
| -cab       | <*filename>* Extract the MSM cabinet to file.                        |
| -lfn       | Usare nomi file lunghi durante l'estrazione.                                 |
| -configure | <*nome*> configurare il modulo usando i dati di un file.            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Installer di sviluppo](windows-installer-development-tools.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



