---
title: Consentire all'utente di specificare dispositivi e file
description: Consentire all'utente di specificare dispositivi e file
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- Macro MCIWndOpenDialog
- Macro MCIWndOpen
- Macro MCIWndOpenInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb9e388e4b7998a932cb22545c05509277f1f7fa705a81fbde02d4d5fb35cdd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786266"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a>Consentire all'utente di specificare dispositivi e file

È possibile associare un dispositivo o un file a una finestra MCIWnd esistente usando le macro [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog), [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)e [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) e la [**funzione GetOpenFileNamePreview.**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa)

Per consentire a un utente dell'applicazione di selezionare un file da riprodurre, **usare MCIWndOpenDialog.** Questa macro visualizza **la finestra** di dialogo Apri (illustrata nella schermata seguente) per la scelta di un file e associa il file selezionato alla finestra MCIWnd corrente.

![Immagine della finestra mciwnd](images/mciwnd3.gif)

È possibile consentire a un utente dell'applicazione di selezionare un file da associare a una finestra MCIWnd e visualizzare in anteprima il file usando [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) e [**MCIWndOpen.**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) La **funzione GetOpenFileNamePreview** visualizza la finestra di dialogo Apri per la scelta di un file e consente all'utente di visualizzare in anteprima (riprodurre) il contenuto.  Quando il nome di un file esistente viene specificato nella finestra di dialogo, **GetOpenFileNamePreview** fornisce un piccolo controllo per consentire all'utente di visualizzare in anteprima il contenuto del file. È possibile associare un file specificato, selezionato con **GetOpenFileNamePreview** o specificato in un altro modo, a una finestra MCIWnd usando **MCIWndOpen.**

È anche possibile usare **MCIWndOpen** per specificare un dispositivo da associare a una finestra MCIWnd. Ad esempio, è possibile usare un nome di dispositivo, ad esempio "CDAudio".

Per associare una finestra MCIWnd a un'interfaccia file o un'interfaccia del flusso di dati ai dati multimediali, usare la macro [**MCIWndOpenInterface.**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) Per altre informazioni sulle interfacce di file e flusso di dati, vedere [Funzioni e macro AVIFile.](avifile-functions-and-macros.md)

> [!Note]  
> Prima di associare un nuovo file o dispositivo a una finestra [**MCIWnd, MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) e [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) chiudono tutti i dispositivi attualmente associati alla finestra. Non è necessario che l'applicazione chiuda i dispositivi aperti prima di usare queste macro.

 

 

 




