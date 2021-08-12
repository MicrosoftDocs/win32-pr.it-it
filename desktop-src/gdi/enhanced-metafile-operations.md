---
description: "È possibile usare l'handle per un metafile avanzato per eseguire le attività seguenti:"
ms.assetid: 8f887c38-6cfa-4918-aa44-dd5fb837b40b
title: Operazioni avanzate sui metafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5daf08ef5d8d48b81aea4daa5d2696ececec3fce44b1303c9ff7ccd692151a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118250285"
---
# <a name="enhanced-metafile-operations"></a>Operazioni avanzate sui metafile

È possibile usare l'handle per un metafile avanzato per eseguire le attività seguenti:

-   Visualizzare l'immagine archiviata in un metafile avanzato.
-   Creare copie di un metafile avanzato.
-   Modificare un metafile avanzato.
-   Recuperare la descrizione facoltativa archiviata in un metafile avanzato.
-   Recuperare una copia di un'intestazione enhanced-metafile.
-   Recuperare una versione binaria di un metafile avanzato.
-   Enumerare i colori nella tavolozza facoltativa.

Queste attività vengono illustrate nelle sezioni rimanenti di questo argomento.

## <a name="display-the-picture-stored-in-an-enhanced-metafile"></a>Visualizzare l'immagine archiviata in un metafile avanzato

È possibile visualizzare l'immagine archiviata in un metafile avanzato usando la [**funzione PlayEnhMetaFile.**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile) Passare alla funzione un handle al metafile avanzato, senza preoccuparsi del formato dei record del metafile avanzato. Tuttavia, a volte è consigliabile enumerare i record nel metafile avanzato per cercare una particolare funzione GDI e modificare i parametri della funzione in qualche modo. A tale scopo, è possibile usare [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) e fornire una funzione di callback, [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc), per elaborare i record del metafile avanzato. Per modificare i parametri per un record metafile avanzato, è necessario conoscere il formato dei parametri all'interno del record.

## <a name="create-copies-of-an-enhanced-metafile"></a>Creare copie di un metafile avanzato

Alcune applicazioni creano copie di backup temporanee (o duplicate) di un file prima di consentire all'utente di modificare l'originale. Un'applicazione può creare una copia di backup di un metafile avanzato chiamando la funzione [**CopyEnhMetaFile,**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea) fornendo un handle che identifica il metafile avanzato e fornendo un puntatore al nome del nuovo file.

Per creare un metafile in formato avanzato basato sulla memoria, chiamare la [**funzione SetEnhMetaFileBits.**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits)

## <a name="edit-an-enhanced-metafile"></a>Modificare un metafile avanzato

La maggior parte delle applicazioni CAD (Computer-Aided Design) richiede un modo per modificare un'immagine archiviata in un metafile avanzato. Anche se la modifica di un metafile avanzato è un'attività complessa, è possibile usare la funzione [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) in combinazione con altre funzioni per fornire questa funzionalità nell'applicazione. La **funzione EnumEnhMetaFile** e la funzione di callback associata, [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc), consentono all'applicazione di elaborare singoli record in un metafile avanzato.

## <a name="retrieve-the-optional-description-stored-in-an-enhanced-metafile"></a>Recuperare la descrizione facoltativa archiviata in un metafile avanzato

Alcune applicazioni visualizzano la descrizione testuale di un metafile avanzato con il nome file corrispondente nella **finestra di dialogo** Apri. È possibile determinare se questa stringa esiste in un metafile avanzato recuperando l'intestazione del metafile con la [**funzione GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) ed esaminando uno dei relativi membri. Se la stringa esiste, l'applicazione la recupera chiamando la [**funzione GetEnhMetaFileDescription.**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona)

## <a name="retrieve-a-binary-version-of-an-enhanced-metafile"></a>Recuperare una versione binaria di un metafile avanzato

È possibile recuperare il contenuto di un metafile chiamando la [**funzione GetEnhMetaFileBits.**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits) Tuttavia, prima di recuperare il contenuto, è necessario specificare le dimensioni del file. Per ottenere le dimensioni, è possibile usare la [**funzione GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) ed esaminare il membro appropriato.

## <a name="enumerate-the-colors-in-the-optional-palette"></a>Enumerare i colori nella tavolozza facoltativa

Per ottenere colori coerenti quando un'immagine viene visualizzata in vari dispositivi di output, è possibile chiamare la [**funzione CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) e archiviare una tavolozza logica in un metafile avanzato. Un'applicazione che visualizza l'immagine archiviata nel metafile avanzato recupera questa tavolozza e chiama la funzione [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) prima di visualizzare l'immagine. Per determinare se un riquadro è archiviato in un metafile avanzato, recuperare l'intestazione del metafile ed esaminare il membro appropriato. Se esiste un riquadro, è possibile chiamare la [**funzione GetEnhMetaFilePaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) per recuperare il riquadro logico.

 

 
