---
title: Supporto Unicode per i controlli comuni
description: In questo argomento viene descritto come supportare Unicode per le notifiche di controllo comuni.
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb029d6e1c018f1793c749aefb2f88104559cae
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963580"
---
# <a name="unicode-support-for-common-controls"></a>Supporto Unicode per i controlli comuni

In questo argomento viene descritto come supportare Unicode per le notifiche di controllo comuni.


Per le versioni 5,80 e successive di comctl32.dll, le notifiche dei controlli comuni supportano i formati ANSI e Unicode nei sistemi Windows 95 o versioni successive. Il sistema determina il formato da usare inviando alla finestra un messaggio [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) . Per specificare un formato, restituire NFR \_ ANSI per le notifiche ANSI o NFR \_ Unicode per le notifiche Unicode. Se non si gestisce questo messaggio, il sistema chiama [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) per determinare il formato. Poiché Windows 95 e Windows 98 restituiscono sempre **false** a questa chiamata di funzione, usano le notifiche ANSI per impostazione predefinita.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui controlli comuni](common-controls-intro.md)
</dt> </dl>

 

 