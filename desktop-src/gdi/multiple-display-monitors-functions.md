---
description: Le funzioni seguenti forniscono supporto per più monitoraggi.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Funzioni per più monitor di visualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0bb4477b325d0e9c79cbb7ba6d22683e31bf4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978535"
---
# <a name="multiple-display-monitors-functions"></a>Funzioni per più monitor di visualizzazione

Le funzioni seguenti forniscono supporto per più monitoraggi.



| Funzione                                           | Descrizione                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | Enumera i monitoraggi di visualizzazione che intersecano un'area costituita dall'intersezione tra un rettangolo di ritaglio specificato e l'area visibile di un contesto di dispositivo. |
| [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | Recupera le informazioni su un monitor di visualizzazione.                                                                                                               |
| [**MonitorEnumProc**](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | Funzione di callback definita dall'applicazione chiamata dalla funzione [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) .                                  |
| [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | Recupera un handle per il monitor di visualizzazione che contiene un punto specificato.                                                                                   |
| [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | Recupera un handle per il monitor di visualizzazione con l'area di intersezione più ampia con un rettangolo specificato.                                              |
| [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | Recupera un handle per il monitor di visualizzazione con l'area di intersezione più ampia con il rettangolo di delimitazione di una finestra specificata.                       |



 

 

 



