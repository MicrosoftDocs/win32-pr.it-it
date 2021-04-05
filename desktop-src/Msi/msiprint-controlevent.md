---
description: Questo evento viene pubblicato dal controllo ScrollableText per consentire all'utente di stampare il contenuto del controllo.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: ControlEvent MsiPrint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0dd876f1a98e68c6ad61c7c122e1b51fa9c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885289"
---
# <a name="msiprint-controlevent"></a>ControlEvent MsiPrint

Questo evento viene pubblicato dal [controllo ScrollableText](scrollabletext-control.md) per consentire all'utente di stampare il contenuto del controllo.

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. Questo ControlEvent è disponibile a partire da Windows Installer 5,0.

Questo evento deve essere sottoscritto da un [controllo pulsante](pushbutton-control.md) che si trova nella stessa finestra di dialogo del [controllo ScrollableText](scrollabletext-control.md). TheMsiPrint ControlEvent deve essere creato nella [tabella ControlEvent](controlevent-table.md).

## <a name="published-by"></a>Pubblicato da

[ScrollableText](scrollabletext-control.md)

## <a name="argument"></a>Argomento

Questo ControlEvent non usa un argomento.

## <a name="action-on-subscribers"></a>Azione sui sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

È possibile utilizzare un controllo [pulsante](pushbutton-control.md) nella stessa finestra di dialogo del [controllo ScrollableText](scrollabletext-control.md) per visualizzare una finestra di dialogo modale che consente all'utente di stampare il contenuto del controllo ScrollableText.

 

 



