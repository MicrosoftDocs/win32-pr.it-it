---
title: Personalizzazione del processo di registrazione
description: Personalizzazione del processo di registrazione
ms.assetid: 9453b9d3-ae9c-4f57-8dd6-f84b9a76618e
keywords:
- MCIWndCreate (funzione)
- MCIWndNew (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec46f61ef4624ba613025f01b081ccc1ebda1cad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955444"
---
# <a name="customizing-the-recording-process"></a>Personalizzazione del processo di registrazione

È possibile personalizzare il processo di registrazione, assumendo il controllo completo della maggior parte degli elementi, dalla creazione della finestra MCIWnd per salvare le informazioni registrate in un file. Nell'esempio seguente viene eseguita una query sul dispositivo MCI per la registrazione e il salvataggio delle funzionalità e sono inclusi i comandi di menu da registrare all'inizio o alla fine del contenuto.

L'esempio seguente usa la funzione [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) per creare una nuova finestra e consente di specificare un file esistente per archiviare i dati registrati e la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) per associare un nuovo file alla finestra. In alternativa, è possibile usare la macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) o [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) per specificare un file.

Nell'esempio viene usata la macro [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) per verificare che il dispositivo sia in grado di registrare e la macro [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) per verificare che il dispositivo salvi le informazioni. Nell'esempio viene impostata la posizione di riproduzione corrente usando le macro [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) e [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend) . Nell'esempio viene avviata la registrazione utilizzando la macro [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) . Una volta registrate le informazioni, l'esempio la salva usando la macro [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) .


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, g_hinst, 
                WS_VISIBLE | WS_CHILD | 
                MCIWNDF_RECORD,                   // add Record button
                NULL ); 
 
            MCIWndNew(g_hwndMCIWnd, "waveaudio"); // new file 
 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MessageBox( hwnd, 
                "Press the red button on the toolbar to record.", 
                "MCIWnd Record", 
                MB_OK ); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK ); 
            } 
            break; 
        case IDM_RECORDATSTART: 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MCIWndHome(g_hwndMCIWnd); 
                MCIWndRecord(g_hwndMCIWnd); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK); 
            } 
            break; 
        case IDM_RECORDATEND: 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MCIWndEnd(g_hwndMCIWnd); 
                MCIWndRecord(g_hwndMCIWnd); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK); 
            } 
            break; 
        case IDM_SAVEMCIWND: 
            if( MCIWndCanSave(g_hwndMCIWnd) ) 
                MCIWndSaveDialog(g_hwndMCIWnd); 
    } 
    break; 
 
    // Handle other messages here. 
```



 

 




