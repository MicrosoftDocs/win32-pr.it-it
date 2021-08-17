---
title: Formati di file di risorse
description: In questa sezione viene descritto il formato del file di risorse binario creato dal compilatore di risorse in base al contenuto del file di definizione delle risorse.
ms.assetid: a0b17555-f50a-4d58-b2bc-760843dd67eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bfc85190993992b7bf87001f3d807b777ed2fe27b4d66cba0b7f7c948d8cfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869792"
---
# <a name="resource-file-formats"></a>Formati di file di risorse

In questa sezione viene descritto il formato del file di risorse binario creato dal compilatore di risorse in base al contenuto del file di definizione delle risorse. Questo file ha in genere l'estensione res. Il linker riformatta il file con estensione res in un file oggetto risorsa e quindi lo collega al file eseguibile di un'applicazione.

Un file di risorse binario è costituito da una serie di voci di risorse concatenate. Ogni voce è costituita da un'intestazione di risorsa e dai dati per tale risorsa. Un'intestazione di risorsa **è allineata** a DWORD nel file ed è costituita dai seguenti elementi:

-   Valore **DWORD che** contiene le dimensioni dell'intestazione della risorsa
-   Valore **DWORD** che contiene le dimensioni dei dati della risorsa
-   Tipo di risorsa
-   Nome della risorsa
-   Informazioni aggiuntive sulle risorse

La [**struttura RESOURCEHEADER**](resourceheader.md) descrive il formato di questa intestazione. I dati per la risorsa seguono l'intestazione della risorsa ed è specifici per ogni tipo di risorsa. Alcune risorse utilizzano anche una struttura di intestazione di gruppo specifica della risorsa per fornire informazioni su un gruppo di risorse.

## <a name="accelerator-table-resources"></a>Risorse della tabella dei tasti di scelta rapida

Una tabella dei tasti di scelta rapida è una voce di risorsa in un file di risorse. Non dispone di un'intestazione di gruppo. Una [**struttura ACCELTABLEENTRY**](acceltableentry.md) descrive ogni voce nella tabella dei tasti di scelta rapida. Sono consentite più tabelle dei tasti di scelta rapida.

## <a name="cursor-and-icon-resources"></a>Risorse per cursori e icone

Il sistema gestisce ogni icona e cursore come un singolo file. Tuttavia, vengono archiviati in file con estensione res e in file eseguibili come un gruppo di risorse icona o un gruppo di risorse cursore. I formati di file delle risorse icona e cursore sono simili. Nel file con estensione res un'intestazione del gruppo di risorse segue tutti i singoli componenti icona o gruppo di cursori.

Il formato di ogni componente icona è molto simile al formato del file con estensione ico. Ogni immagine icona viene archiviata in una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) seguita dai bit DIB (Device Independent Bitmap) a colori della maschera **XOR** dell'icona. I bit DIB monocromatici della maschera **AND** dell'icona seguono i bit DIB di colore.

Il formato di ogni componente del cursore è simile al formato del file con estensione cur. Ogni immagine del cursore viene archiviata in una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) seguita dai bit DIB monocromatici della maschera **XOR** del cursore e quindi dai bit DIB monocromatici della maschera **AND** del cursore. Si noti che esiste una differenza nelle bitmap delle due risorse: a differenza delle icone, le maschere XOR del cursore non hanno bit DIB di colore. Anche se le bitmap delle maschere di cursore sono monocroma e non hanno intestazioni DIB o tabelle dei colori, i bit sono ancora in formato DIB in relazione all'allineamento e alla direzione. Un'altra differenza significativa tra i cursori e le icone è che i cursori hanno un hotspot e le icone no.

L'intestazione di gruppo per le risorse icona e cursore è costituita da una [**struttura NEWHEADER**](newheader.md) più una [**o più strutture RESDIR.**](resdir.md) Esiste una struttura **RESDIR** per ogni icona o cursore. L'intestazione del gruppo contiene le informazioni necessarie a un'applicazione per selezionare l'icona o il cursore corretto da visualizzare. Sia l'intestazione del gruppo che i dati ripetuti per ogni icona o cursore nel gruppo hanno una lunghezza fissa. In questo modo l'applicazione può accedere in modo casuale alle informazioni.

## <a name="dialog-box-resources"></a>Risorse della finestra di dialogo

Una finestra di dialogo è anche una voce di risorsa nel file di risorse. È costituito da una struttura di intestazione della finestra di dialogo [**DLGTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgtemplate) più una [**struttura DLGITEMTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate) per ogni controllo nella finestra di dialogo. Le [**strutture DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) e [**DLGITEMTEMPLATEEX**](/windows/desktop/dlgbox/dlgitemtemplateex) descrivono il formato delle risorse estese della finestra di dialogo.

## <a name="font-resources"></a>Risorse dei tipi di carattere

I tipi di carattere vengono archiviati nel file di risorse come gruppo di risorse. I singoli tipi di carattere costituiscono un gruppo di caratteri. Istruzione [FONT Statement](./font-statement.md) per la definizione della risorsa in . Il file RC definisce ogni tipo di carattere. Ogni singolo tipo di carattere nella risorsa è costituito dal contenuto completo del file con estensione fnt correlato. Una [**struttura FONTGROUPHDR**](fontgrouphdr.md) segue tutti i singoli componenti del tipo di carattere nel file con estensione res.

Le risorse del tipo di carattere non vengono aggiunte alle risorse di un'applicazione specifica. In genere vengono invece aggiunti ai file eseguibili con estensione fon. Questi file sono in genere DLL di solo risorse anziché applicazioni.

## <a name="menu-resources"></a>Risorse di menu

Una *risorsa di menu* è costituita da una struttura [**MENUHEADER**](menuheader.md) seguita da una o più strutture [**NORMALMENUITEM**](normalmenuitem.md) o [**POPUPMENUITEM,**](popupmenuitem.md) una per ogni voce di menu nel modello di menu. Le [**strutture MENUEX \_ TEMPLATE \_ HEADER**](menuex-template-header.md) e [**MENUEX TEMPLATE \_ \_ ITEM**](menuex-template-item.md) descrivono il formato delle risorse di menu estese.

## <a name="message-table-resources"></a>Risorse della tabella dei messaggi

Una *tabella di messaggi* è una risorsa che contiene testo formattato da visualizzare come messaggio di errore o in una finestra di messaggio. La struttura principale in una risorsa tabella messaggi è la [**struttura MESSAGE \_ RESOURCE \_ DATA.**](/windows/desktop/api/Winnt/ns-winnt-message_resource_data)

## <a name="version-resources"></a>Risorse della versione

La struttura principale in una risorsa di versione è la [**struttura \_ FIXEDFILEINFO di VS.**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) Altre strutture includono la struttura [**VarFileInfo per**](varfileinfo.md) archiviare i dati delle informazioni sulla lingua e [**StringFileInfo per**](stringfileinfo.md) le informazioni sulle stringhe definite dall'utente. Tutte le stringhe in una risorsa di versione sono in formato Unicode. Ogni blocco di informazioni è allineato su un **limite DWORD.**

 

 