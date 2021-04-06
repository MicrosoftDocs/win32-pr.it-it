---
description: Per creare un'interfaccia utente semplice, gli sviluppatori di pacchetti di installazione possono utilizzare una progettazione dell'interfaccia utente che rispetta il comportamento della procedura guidata di interfaccia.
ms.assetid: c69ba452-3c2e-47d7-8ea0-8f8f9e6b58c8
title: Comportamento della procedura guidata dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045aa59fe510ff10f428d0a7c74549ce4d817157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760139"
---
# <a name="user-interface-wizard-behavior"></a>Comportamento della procedura guidata dell'interfaccia utente

Per creare un'interfaccia utente semplice, gli sviluppatori di pacchetti di installazione possono utilizzare una progettazione dell'interfaccia utente che rispetta il comportamento della procedura guidata di interfaccia.

Il termine comportamento della procedura guidata dell'interfaccia utente indica che ogni finestra di dialogo in una sequenza contiene un pulsante **>>successivo** , che l'utente fa clic per passare alla successiva finestra di dialogo dopo aver immesso i dati o aver configurato le informazioni nella finestra di dialogo corrente. Se l'utente decide di tornare indietro e di modificare le informazioni immesse in una finestra di dialogo precedente, ogni finestra di dialogo contiene un pulsante **<<precedente** su cui l'utente fa clic per tornare indietro. Alla fine della sequenza della procedura guidata, l'utente fa clic su un pulsante **fine** per avviare il processo di installazione.

L'interfaccia utente descritta nell'esempio dell'interfaccia utente rispetta il comportamento della procedura guidata dell'interfaccia utente. Vedere [un esempio di installazione](an-installation-example.md).

 

 



