---
description: Qualsiasi thread può creare una finestra.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: Creazione di finestre nei thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebcde45ca37696b6dbc90e639f630a689498b04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311990"
---
# <a name="creating-windows-in-threads"></a>Creazione di finestre nei thread

Qualsiasi thread può creare una finestra. Il thread che crea la finestra è proprietario della finestra e della coda di messaggi associata. Pertanto, il thread deve fornire un ciclo di messaggi per elaborare i messaggi nella coda di messaggi. Inoltre, è necessario utilizzare [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) o [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) in tale thread, anziché le altre funzioni di [attesa](/windows/desktop/Sync/wait-functions), in modo che sia in grado di elaborare i messaggi. In caso contrario, il sistema può diventare un deadlock quando il thread riceve un messaggio mentre è in attesa.

La funzione [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) può essere usata per consentire a un set di thread di condividere lo stesso stato di input. Condividendo lo stato di input, i thread condividono il concetto della finestra attiva. In questo, un thread può sempre attivare la finestra di un altro thread. Questa funzione è utile anche per condividere lo stato attivo, lo stato di acquisizione del mouse, lo stato della tastiera e lo stato dell'ordine Z della finestra tra le finestre create da thread diversi il cui stato di input è condiviso.

Per informazioni sulla creazione di Windows, vedere [classi di Windows](../winmsg/window-classes.md).

 

 
