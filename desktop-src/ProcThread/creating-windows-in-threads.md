---
description: Qualsiasi thread può creare una finestra.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: Creazione di Windows nei thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2084536ff43ea4c52efb179177fe6f6c803c49b9f580b2d298b73e9b528f1a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143094"
---
# <a name="creating-windows-in-threads"></a>Creazione di Windows nei thread

Qualsiasi thread può creare una finestra. Il thread che crea la finestra è proprietario della finestra e della coda di messaggi associata. Pertanto, il thread deve fornire un ciclo di messaggi per elaborare i messaggi nella relativa coda di messaggi. Inoltre, è necessario usare [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) o [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) in tale thread, anziché le altre funzioni di attesa [,](/windows/desktop/Sync/wait-functions)in modo che possa elaborare i messaggi. In caso contrario, il sistema può diventare in deadlock quando al thread viene inviato un messaggio mentre è in attesa.

La [**funzione AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) può essere usata per consentire a un set di thread di condividere lo stesso stato di input. Condividendo lo stato di input, i thread condividono il concetto di finestra attiva. In questo modo, un thread può sempre attivare la finestra di un altro thread. Questa funzione è utile anche per condividere lo stato attivo, lo stato mouse capture, lo stato della tastiera e lo stato di ordine Z della finestra tra finestre create da thread diversi il cui stato di input è condiviso.

Per informazioni sulla creazione di finestre, vedere [Windows classi](../winmsg/window-classes.md).

 

 
