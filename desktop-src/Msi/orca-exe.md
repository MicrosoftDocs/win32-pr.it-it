---
description: Orca.exe è un editor di tabelle di database per la creazione e la modifica Windows pacchetti del programma di installazione e dei moduli unione.
ms.assetid: 4dddc262-1271-4e00-a986-53380b957b17
title: Orca.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9f1b0d31936bf81e60efd8eb9799ddb30b4d5a6f78363e2ff5d3d638ae40c4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082681"
---
# <a name="orcaexe"></a>Orca.exe

Orca.exe è un editor di tabelle di database per la creazione e la modifica Windows pacchetti del programma di installazione e dei moduli unione. Lo strumento fornisce un'interfaccia grafica per la convalida, evidenziando le voci specifiche in cui si verificano errori o avvisi di convalida.

Questo strumento è disponibile solo in componenti Windows [SDK per sviluppatori Windows Programma di installazione](platform-sdk-components-for-windows-installer-developers.md). Viene fornito come file Orca.msi. Dopo aver installato Windows SDK Components for Windows Installer Developers, fare doppio clic su Orca.msi per installare il file Orca.exe.

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
| -c         | Eseguire il commit del merge nel database se non sono presenti errori.                                     |
| -!         | Eseguire il commit del merge in un database anche se sono presenti errori.                       |
| -M         | <*Modulo>* Merge Module da unire nel database.                      |
| -f         | \[Funzionalità:Funzionalità2 \] Funzionalità per la connessione al modulo di unione.                |
| -r         | <*ID directory>* directory per il reindirizzamento radice del modulo.    |
| -X         | <*directory*> estrai i file in un'immagine nella directory .         |
| -g         | <*language*> linguaggio usato per aprire un modulo.                         |
| -l         | <*file di log*> file da usare come log, aggiungere se esiste già.      |
| -i         | <*directory*> estrai i file nell'immagine di origine nella directory . |
| -cab       | <*filename>* Estrai l'archivio MSM nel file.                        |
| -lfn       | Usare nomi file lunghi durante l'estrazione.                                 |
| -configure | <*filename*> Configurare il modulo usando i dati di un file.            |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Strumenti di sviluppo del programma di installazione](windows-installer-development-tools.md)
</dt> <dt>

[Versioni rilasciate, strumenti e ridistribuibili](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



