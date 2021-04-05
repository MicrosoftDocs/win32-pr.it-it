---
title: Salvataggio del contenuto registrato
description: Salvataggio del contenuto registrato
ms.assetid: 0c159c44-f96c-4c08-bd3f-9e65b413026c
keywords:
- MCIWndSave (macro)
- MCIWndSaveDialog (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bb2cd89a72af4412b2555dd9b7c88f2d277ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710447"
---
# <a name="saving-recorded-content"></a>Salvataggio del contenuto registrato

Dopo aver completato la registrazione, è possibile salvare il contenuto usando la macro [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) o [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) oppure usando la funzione [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) con **MCIWndSave**. La macro **MCIWndSave** Salva i dati nel file associato alla finestra MCIWnd. La macro **MCIWndSaveDialog** consente all'utente di specificare un nome file e salvare i dati registrati nel file specificato. La funzione **GetSaveFileNamePreview** Visualizza la finestra di dialogo **SaveAs** per la scelta di un file e consente all'utente di visualizzare l'anteprima (riproduzione) del file. Quando si specifica il nome di un file esistente nella finestra di dialogo **SaveAs** , **GetSaveFileNamePreview** fornisce un piccolo controllo nella finestra di dialogo per consentire all'utente di visualizzare in anteprima il contenuto del file. È possibile salvare i dati registrati in un file selezionato con **GetSaveFileNamePreview** usando **MCIWndSave**.

 

 




