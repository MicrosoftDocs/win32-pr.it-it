---
title: Come ridimensionare automaticamente i controlli Rich Edit
description: Un'applicazione può ridimensionare un controllo Rich Edit in base alle esigenze, in modo che sia sempre della stessa dimensione del contenuto.
ms.assetid: CCAFC039-AC9E-4BC4-ABE1-8C56FA9DD3F5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee9ead05c4c04526a9290dc115f7a2fa7741397
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047452"
---
# <a name="how-to-automatically-resize-rich-edit-controls"></a>Come ridimensionare automaticamente i controlli Rich Edit

Un'applicazione può ridimensionare un controllo Rich Edit in base alle esigenze, in modo che sia sempre della stessa dimensione del contenuto. Un controllo Rich Edit supporta questa cosiddetta funzionalità senza *fondo* inviando la finestra padre di un codice di notifica [en \_ REQUESTRESIZE](en-requestresize.md) ogni volta che viene modificata la dimensione del contenuto del controllo.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="automatically-resize-a-rich-edit-control"></a>Ridimensiona automaticamente un controllo Rich Edit

Quando si elabora il codice di notifica [en \_ REQUESTRESIZE](en-requestresize.md) , un'applicazione deve ridimensionare il controllo alle dimensioni nella struttura [**REQRESIZE**](/windows/desktop/api/Richedit/ns-richedit-reqresize) specificata. Un'applicazione può anche spostare le informazioni che si avvicinano al controllo per adattarsi alla modifica dell'altezza del controllo. Per ridimensionare il controllo, è possibile usare la funzione [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) .

È possibile forzare un controllo Rich Edit senza fondo per inviare un codice di notifica [en \_ REQUESTRESIZE](en-requestresize.md) usando il messaggio [**em \_ REQUESTRESIZE**](em-requestresize.md) . Questo messaggio può essere utile quando si elabora il messaggio di [**\_ dimensioni WM**](/windows/desktop/winmsg/wm-size) .

## <a name="remarks"></a>Commenti

Per ricevere i codici di notifica di [ \_ REQUESTRESIZE](en-requestresize.md) , è necessario abilitare la notifica usando il messaggio [em \_ SETEVENTMASK](em-seteventmask.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Rich Edit](using-rich-edit-controls.md)
</dt> <dt>

[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 