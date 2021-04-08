---
description: Il metodo Connect dell'oggetto merge può essere utilizzato per connettere un modulo a una funzionalità aggiuntiva che è stata unita nel database o che verrà unita nel database. La funzionalità deve esistere prima di chiamare questo metodo.
ms.assetid: 8b59de42-bc3f-468b-a410-8f935ff73345
title: Connessione di un modulo merge a più funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d57b49f1ee27b4c8d3aa5d0b3ac1b0d7b8b8e11c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883689"
---
# <a name="connecting-a-merge-module-to-multiple-features"></a>Connessione di un modulo merge a più funzionalità

Il metodo [**Connect**](merge-connect.md) dell' [oggetto merge](merge-object.md) può essere utilizzato per connettere un modulo a una funzionalità aggiuntiva che è stata unita nel database o che verrà unita nel database. La funzionalità deve esistere prima di chiamare questo metodo.

Un modulo merge non deve mai recapitare un componente contenente file di sistema alla funzionalità principale di un'applicazione, perché ciò può causare la convalida e il ripristino dell'applicazione ogni volta che viene usato il file di sistema. È necessario creare un file con estensione MSI progettato per accettare i componenti di un modulo merge in modo che tutti i componenti che contengono file di sistema appartengano solo a funzionalità distinte dalla funzionalità principale dell'applicazione.

Se il pacchetto usa un modulo merge contenente file di sistema che collegano tutti i componenti del modulo merge alla funzionalità principale dell'applicazione, un tentativo di usare il file di sistema potrebbe attivare il programma di installazione per provare a riparare la funzionalità principale dell'applicazione. Se non è possibile ripristinare la funzionalità principale, l'installazione potrebbe non riuscire.

 

 



