---
title: Consentire all'utente di specificare i dispositivi e i file
description: Consentire all'utente di specificare i dispositivi e i file
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- MCIWndOpenDialog (macro)
- MCIWndOpen (macro)
- MCIWndOpenInterface (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4191f18409a1fb1f23ba3a2128b4aaed1b30e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710984"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a>Consentire all'utente di specificare i dispositivi e i file

È possibile associare un dispositivo o un file a una finestra MCIWnd esistente usando le macro [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)e [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) e la funzione [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) .

Per consentire a un utente dell'applicazione di selezionare un file da riprodurre, usare **MCIWndOpenDialog**. Questa macro Visualizza la finestra di dialogo **Apri** (mostrata nella schermata seguente) per la scelta di un file e associa il file selezionato alla finestra MCIWnd corrente.

![immagine della finestra MCIWnd](images/mciwnd3.gif)

È possibile consentire a un utente dell'applicazione di selezionare un file da associare a una finestra MCIWnd e di visualizzare in anteprima il file usando [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) e [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen). La funzione **GetOpenFileNamePreview** Visualizza la finestra di dialogo **Apri** per la scelta di un file e consente all'utente di visualizzare in anteprima (riprodurre) il contenuto. Quando si specifica il nome di un file esistente nella finestra di dialogo, **GetOpenFileNamePreview** fornisce un piccolo controllo che consente all'utente di visualizzare in anteprima il contenuto del file. È possibile associare un file specificato, selezionato con **GetOpenFileNamePreview** o specificato in un altro modo, con una finestra MCIWnd usando **MCIWndOpen**.

È anche possibile usare **MCIWndOpen** per specificare un dispositivo da associare a una finestra di MCIWnd. Ad esempio, è possibile usare un nome di dispositivo, ad esempio "CDAudio".

Per associare una finestra MCIWnd con un'interfaccia di file o un'interfaccia del flusso di dati ai dati multimediali, usare la macro [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) . Per altre informazioni sulle interfacce di flusso di dati e file, vedere [funzioni e macro di avifile](avifile-functions-and-macros.md).

> [!Note]  
> Prima di associare un nuovo file o dispositivo a una finestra MCIWnd, [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) e [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) chiudono tutti i dispositivi attualmente associati alla finestra. Non è necessario che l'applicazione chiuda tutti i dispositivi aperti prima di usare queste macro.

 

 

 




