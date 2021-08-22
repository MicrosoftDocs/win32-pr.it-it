---
description: Le funzioni seguenti forniscono il supporto per più monitoraggi.
ms.assetid: a64b256c-e7a1-4ee2-a346-4b7abcab9e90
title: Funzioni di monitoraggio a più monitoraggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e35ab6fef353f793257721077074271915a3628859471a2f5d89694f6d47440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779141"
---
# <a name="multiple-display-monitors-functions"></a>Funzioni di monitoraggio a più monitoraggi

Le funzioni seguenti forniscono il supporto per più monitoraggi.



| Funzione                                           | Descrizione                                                                                                                                                  |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) | Enumera i monitoraggi di visualizzazione che intersecano un'area formata dall'intersezione di un rettangolo di ritaglio specificato e dell'area visibile di un contesto di dispositivo. |
| [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa)           | Recupera informazioni su un monitor di visualizzazione.                                                                                                               |
| [**MonitorEnumProc**](/windows/desktop/api/Winuser/nc-winuser-monitorenumproc)         | Funzione di callback definita dall'applicazione chiamata dalla [**funzione EnumDisplayMonitors.**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors)                                  |
| [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint)       | Recupera un handle per il monitor di visualizzazione che contiene un punto specificato.                                                                                   |
| [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)         | Recupera un handle per il monitor di visualizzazione con l'area di intersezione più grande con un rettangolo specificato.                                              |
| [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)     | Recupera un handle per il monitor di visualizzazione con l'area di intersezione più grande con il rettangolo di delimitazione di una finestra specificata.                       |



 

 

 



