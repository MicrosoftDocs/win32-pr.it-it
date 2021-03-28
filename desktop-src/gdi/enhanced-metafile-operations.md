---
description: "È possibile usare l'handle per un metafile migliorato per eseguire le attività seguenti:"
ms.assetid: 8f887c38-6cfa-4918-aa44-dd5fb837b40b
title: Operazioni di Metafile avanzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ba9e2ac2f14c4436c039a66cc3211b471c0461
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130779"
---
# <a name="enhanced-metafile-operations"></a>Operazioni di Metafile avanzate

È possibile usare l'handle per un metafile migliorato per eseguire le attività seguenti:

-   Visualizza l'immagine archiviata in un metafile avanzato.
-   Creazione di copie di un metafile avanzato.
-   Modificare un metafile avanzato.
-   Recuperare la descrizione facoltativa archiviata in un metafile avanzato.
-   Recuperare una copia di un'intestazione Enhanced Metafile.
-   Recuperare una versione binaria di un metafile avanzato.
-   Enumerare i colori nella tavolozza facoltativa.

Queste attività vengono descritte nelle sezioni della parte restante di questo argomento.

## <a name="display-the-picture-stored-in-an-enhanced-metafile"></a>Visualizza l'immagine archiviata in un metafile avanzato

È possibile visualizzare l'immagine archiviata in un metafile migliorato usando la funzione [**PlayEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile) . Passare alla funzione un handle per il metafile migliorato, senza preoccuparsi del formato dei record di metafile avanzati. Tuttavia, a volte è consigliabile enumerare i record del metafile migliorato per cercare una particolare funzione GDI e modificare i parametri della funzione in qualche modo. A tale scopo, è possibile utilizzare [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) e fornire una funzione di callback, [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc), per elaborare i record metafile avanzati. Per modificare i parametri per un record di metafile avanzato, è necessario essere a conoscenza del formato dei parametri all'interno del record.

## <a name="create-copies-of-an-enhanced-metafile"></a>Creazione di copie di un metafile avanzato

Alcune applicazioni creano copie di un file di backup temporaneo (o duplicate) prima di consentire all'utente di modificare l'originale. Un'applicazione può creare una copia di backup di un metafile migliorato chiamando la funzione [**CopyEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea) , fornendo un handle che identifica il metafile migliorato e fornendo un puntatore al nome del nuovo file.

Per creare un metafile in formato avanzato basato sulla memoria, chiamare la funzione [**SetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits) .

## <a name="edit-an-enhanced-metafile"></a>Modificare un metafile avanzato

La maggior parte delle applicazioni di disegno, illustrazione e progettazione assistita da computer (CAD) richiede un mezzo per modificare un'immagine archiviata in un metafile avanzato. Anche se la modifica di un metafile avanzato è un'attività complessa, è possibile usare la funzione [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) in combinazione con altre funzioni per fornire questa funzionalità nell'applicazione. La funzione **EnumEnhMetaFile** e la funzione di callback associata, [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc), consentono all'applicazione di elaborare singoli record in un metafile avanzato.

## <a name="retrieve-the-optional-description-stored-in-an-enhanced-metafile"></a>Recuperare la descrizione facoltativa archiviata in un metafile avanzato

In alcune applicazioni viene visualizzata la descrizione testuale di un metafile migliorato con il nome file corrispondente nella finestra di dialogo **Apri** . È possibile determinare se questa stringa è presente in un metafile migliorato recuperando l'intestazione metafile con la funzione [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) ed esaminando uno dei relativi membri. Se la stringa esiste, l'applicazione la recupera chiamando la funzione [**GetEnhMetaFileDescription**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona) .

## <a name="retrieve-a-binary-version-of-an-enhanced-metafile"></a>Recuperare una versione binaria di un metafile avanzato

È possibile recuperare il contenuto di un metafile chiamando la funzione [**GetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits) . Tuttavia, prima di recuperare il contenuto, è necessario specificare le dimensioni del file. Per ottenere le dimensioni, è possibile usare la funzione [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) ed esaminare il membro appropriato.

## <a name="enumerate-the-colors-in-the-optional-palette"></a>Enumerare i colori nella tavolozza facoltativa

Per ottenere colori coerenti quando un'immagine viene visualizzata in diversi dispositivi di output, è possibile chiamare la funzione [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) e archiviare una tavolozza logica in un metafile avanzato. Un'applicazione che Visualizza l'immagine archiviata nel metafile avanzato recupera questa tavolozza e chiama la funzione [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) prima di visualizzare l'immagine. Per determinare se una tavolozza è archiviata in un metafile migliorato, recuperare l'intestazione metafile ed esaminare il membro appropriato. Se è presente una tavolozza, è possibile chiamare la funzione [**GetEnhMetaFilePaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) per recuperare la tavolozza logica.

 

 
