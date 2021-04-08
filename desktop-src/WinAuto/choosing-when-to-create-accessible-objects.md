---
title: Scelta di quando creare oggetti accessibili
description: Gli sviluppatori di server possono creare tutti gli oggetti accessibili all'interno di un contenitore quando viene creato il contenitore oppure possono creare oggetti accessibili in modo dinamico.
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987b40527c178c40101288b0192c38d9a9b06040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045006"
---
# <a name="choosing-when-to-create-accessible-objects"></a>Scelta di quando creare oggetti accessibili

Gli sviluppatori di server possono creare tutti gli oggetti accessibili all'interno di un contenitore quando viene creato il contenitore oppure possono creare oggetti accessibili in modo dinamico.

Si supponga, ad esempio, di disporre di una finestra di dialogo con diversi controlli personalizzati. Un server crea oggetti accessibili per tutti i controlli personalizzati quando viene visualizzata la finestra di dialogo. Tuttavia, se uno dei controlli è una casella combinata personalizzata, il server attende fino a quando un utente lo seleziona per creare oggetti accessibili per gli elementi contenuti nella casella combinata.

Se l'elemento padre crea oggetti accessibili in modo dinamico, le applicazioni utilizzano una quantità inferiore di memoria rispetto a quando tutti i possibili oggetti accessibili sono stati creati in anticipo.

 

 




