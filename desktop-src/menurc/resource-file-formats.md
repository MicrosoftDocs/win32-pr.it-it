---
title: Formati di file di risorse
description: Questa sezione descrive il formato del file di risorse binario creato dal compilatore di risorse in base al contenuto del file di definizione delle risorse.
ms.assetid: a0b17555-f50a-4d58-b2bc-760843dd67eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90c789cd1684c1f5ca31af0e2d60a31052ca03f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872498"
---
# <a name="resource-file-formats"></a>Formati di file di risorse

Questa sezione descrive il formato del file di risorse binario creato dal compilatore di risorse in base al contenuto del file di definizione delle risorse. Questo file contiene in genere un'estensione res. Il linker riformatta il file res in un file oggetto risorsa e quindi lo collega al file eseguibile di un'applicazione.

Un file di risorse binario è costituito da un numero di voci di risorse concatenate. Ogni voce è costituita da un'intestazione di risorsa e dai dati per tale risorsa. Un'intestazione di risorsa è allineata a **DWORD** nel file ed è costituita dagli elementi seguenti:

-   **Valore DWORD** che contiene la dimensione dell'intestazione della risorsa
-   **Valore DWORD** che contiene la dimensione dei dati della risorsa.
-   Tipo di risorsa
-   Nome della risorsa
-   Informazioni aggiuntive sulle risorse

La struttura [**RESOURCEHEADER**](resourceheader.md) descrive il formato di questa intestazione. I dati della risorsa seguono l'intestazione della risorsa ed è specifico per ogni tipo di risorsa. Alcune risorse usano anche una struttura di intestazione di gruppo specifica della risorsa per fornire informazioni su un gruppo di risorse.

## <a name="accelerator-table-resources"></a>Risorse tabella acceleratore

Una tabella di tasti di scelta rapida è una voce di risorsa in un file di risorse. Non dispone di un'intestazione di gruppo. Una struttura [**ACCELTABLEENTRY**](acceltableentry.md) descrive ogni voce nella tabella dei tasti di scelta rapida. Sono consentite più tabelle di tasti di scelta rapida.

## <a name="cursor-and-icon-resources"></a>Risorse Cursor e Icon

Il sistema gestisce ogni icona e cursore come singolo file. Tuttavia, vengono archiviati in file con estensione res e nei file eseguibili come gruppo di risorse icona o un gruppo di risorse del cursore. I formati di file delle risorse icona e cursore sono simili. Nel file res un'intestazione del gruppo di risorse segue tutti i singoli componenti dell'icona o del gruppo di cursori.

Il formato di ogni componente icona è simile al formato del file con estensione ico. Ogni immagine dell'icona viene archiviata in una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) seguita dai bit DIB (Device-Independent Bitmap) della maschera **Xor** dell'icona. I bit di DIB monocromatico delle icone **e** della maschera seguono i bit DIB del colore.

Il formato di ogni componente del cursore è simile al formato del file cur. Ogni immagine del cursore viene archiviata in una struttura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) seguita da bit DIB monocromi della maschera **Xor** del cursore e quindi dai bit DIB monocromatici delle maschere **e** del cursore. Si noti che c'è una differenza tra le bitmap delle due risorse: diversamente dalle icone, le maschere del cursore XOR non hanno bit DIB di colore. Sebbene le bitmap delle maschere del cursore siano monocromatiche e non dispongano di intestazioni o tabelle dei colori DIB, i bit sono ancora in formato DIB rispetto all'allineamento e alla direzione. Un'altra differenza significativa tra cursori e icone è che i cursori hanno un hotspot e le icone non lo sono.

L'intestazione di gruppo per le risorse icona e cursore è costituita da una struttura [**NEWHEADER**](newheader.md) più una o più strutture [**RESDIR**](resdir.md) . Esiste una struttura **RESDIR** per ogni icona o cursore. L'intestazione di gruppo contiene le informazioni necessarie a un'applicazione per selezionare l'icona o il cursore corretto da visualizzare. Sia l'intestazione di gruppo che i dati ripetuti per ogni icona o cursore del gruppo hanno una lunghezza fissa. Ciò consente all'applicazione di accedere in modo casuale alle informazioni.

## <a name="dialog-box-resources"></a>Risorse della finestra di dialogo

Una finestra di dialogo è anche una voce di risorsa nel file di risorse. È costituito da una struttura di intestazione della finestra di dialogo [**DLGTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgtemplate) più una struttura [**DLGITEMTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate) per ogni controllo nella finestra di dialogo. Le strutture [**DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) e [**DLGITEMTEMPLATEEX**](/windows/desktop/dlgbox/dlgitemtemplateex) descrivono il formato delle risorse della finestra di dialogo estese.

## <a name="font-resources"></a>Risorse dei tipi di carattere

I tipi di carattere vengono archiviati nel file di risorse come gruppo di risorse. I singoli tipi di carattere costituiscono un gruppo di tipi di carattere. Istruzione di definizione di risorsa dell' [istruzione del tipo di carattere](./font-statement.md) in. Il file RC definisce tutti i tipi di carattere. Ogni singolo carattere nella risorsa è costituito dal contenuto completo del file con estensione FNT correlato. Una struttura [**FONTGROUPHDR**](fontgrouphdr.md) segue tutti i singoli componenti del tipo di carattere nel file res.

Le risorse del tipo di carattere non vengono aggiunte alle risorse di un'applicazione specifica. Al contrario, vengono in genere aggiunti ai file eseguibili con estensione fon. Questi file sono in genere DLL di solo risorse anziché applicazioni.

## <a name="menu-resources"></a>Risorse di menu

Una *risorsa di menu* è costituita da una struttura [**MENUHEADER**](menuheader.md) seguita da una o più strutture [**NORMALMENUITEM**](normalmenuitem.md) o [**POPUPMENUITEM**](popupmenuitem.md) , una per ogni voce di menu nel modello di menu. L' [**\_ \_ intestazione del modello menuex**](menuex-template-header.md) e le strutture degli [**\_ \_ elementi del modello menuex**](menuex-template-item.md) descrivono il formato delle risorse di menu estese.

## <a name="message-table-resources"></a>Risorse tabella messaggi

Una *tabella messaggi* è una risorsa che contiene testo formattato da visualizzare come messaggio di errore o in una finestra di messaggio. La struttura principale in una risorsa della tabella messaggi è la struttura [**\_ \_ dei dati della risorsa del messaggio**](/windows/desktop/api/Winnt/ns-winnt-message_resource_data) .

## <a name="version-resources"></a>Risorse della versione

La struttura principale in una risorsa di versione è la struttura di [**Visual Studio \_ informazione FixedFileInfo**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) . Altre strutture includono la struttura [**VarFileInfo**](varfileinfo.md) per archiviare i dati delle informazioni sulla lingua e [**StringFileInfo**](stringfileinfo.md) per le informazioni sulle stringhe definite dall'utente. Tutte le stringhe in una risorsa di versione sono in formato Unicode. Ogni blocco di informazioni è allineato a un limite **DWORD** .

 

 