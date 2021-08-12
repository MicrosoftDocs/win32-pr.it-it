---
title: Supporto Unicode per i controlli comuni
description: Questo argomento descrive come supportare Unicode per le notifiche di controllo comuni.
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01ab987516f1a91b47f8e5fd5f031631956d8c7bf59cd164edd83d414d5e72d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668893"
---
# <a name="unicode-support-for-common-controls"></a>Supporto Unicode per i controlli comuni

Questo argomento descrive come supportare Unicode per le notifiche di controllo comuni.


Per le versioni 5.80 e successive di comctl32.dll, le notifiche dei controlli comuni supportano sia i formati ANSI che Unicode nei sistemi Windows 95 o versioni successive. Il sistema determina il formato da usare inviando alla finestra un [**messaggio WM \_ NOTIFYFORMAT.**](wm-notifyformat.md) Per specificare un formato, restituire NFR ANSI per le notifiche \_ ANSI o UNICODE NFR \_ per le notifiche Unicode. Se non si gestisce questo messaggio, il sistema chiama [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) per determinare il formato. Poiché Windows 95 e Windows 98 restituiscono sempre **FALSE** a questa chiamata di funzione, per impostazione predefinita usano le notifiche ANSI.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui controlli comuni](common-controls-intro.md)
</dt> </dl>

 

 