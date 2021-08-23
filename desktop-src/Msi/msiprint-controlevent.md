---
description: Questo evento viene pubblicato dal controllo ScrollableText per consentire all'utente di stampare il contenuto del controllo.
ms.assetid: 8cb91b21-f6db-4f49-827d-1ec739ff4f45
title: MsiPrint ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbd2107e4930e7d2d410846f656f25143926f8675f354976d866b2ee5d547b0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519781"
---
# <a name="msiprint-controlevent"></a>MsiPrint ControlEvent

Questo evento viene pubblicato dal [controllo ScrollableText per](scrollabletext-control.md) consentire all'utente di stampare il contenuto del controllo.

**[Windows Installer 4.5 o versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato. Questo ControlEvent è disponibile a partire da Windows Installer 5.0.

Questo evento deve essere sottoscritto da un [controllo PushButton](pushbutton-control.md) che si trova nella stessa finestra di dialogo del [controllo ScrollableText](scrollabletext-control.md). TheMsiPrint ControlEvent deve essere creato nella [tabella ControlEvent](controlevent-table.md).

## <a name="published-by"></a>Pubblicato da

[ScrollableText](scrollabletext-control.md)

## <a name="argument"></a>Argomento

Questo ControlEvent non usa un argomento.

## <a name="action-on-subscribers"></a>Azione nei Sottoscrittori

Questo ControlEvent non esegue un'azione sui sottoscrittori.

## <a name="typical-use"></a>Utilizzo tipico

Un [controllo PushButton](pushbutton-control.md) nella stessa finestra di dialogo del controllo [ScrollableText](scrollabletext-control.md) può essere usato per visualizzare una finestra di dialogo modale che consente all'utente di stampare il contenuto del controllo ScrollableText.

 

 



