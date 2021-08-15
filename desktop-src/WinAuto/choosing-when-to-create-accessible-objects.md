---
title: Scelta del momento in cui creare oggetti accessibili
description: Gli sviluppatori di server possono creare tutti gli oggetti accessibili all'interno di un contenitore quando viene creato il contenitore oppure possono creare gli oggetti accessibili in modo dinamico.
ms.assetid: 26c8bb4b-19ec-4fd5-b758-30cb6a513818
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a53ee02cb7de574242b3ba9986cdf0ce6068e8495e1ebaf638eed08e9c04b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118325980"
---
# <a name="choosing-when-to-create-accessible-objects"></a>Scelta del momento in cui creare oggetti accessibili

Gli sviluppatori di server possono creare tutti gli oggetti accessibili all'interno di un contenitore quando viene creato il contenitore oppure possono creare gli oggetti accessibili in modo dinamico.

Si immagini, ad esempio, una finestra di dialogo con diversi controlli personalizzati. Un server crea oggetti accessibili per tutti i controlli personalizzati quando viene visualizzata la finestra di dialogo. Tuttavia, se uno dei controlli è una casella combinata personalizzata, il server attende fino a quando un utente non la seleziona per creare oggetti accessibili per gli elementi contenuti nella casella combinata.

Facendo in modo che l'elemento padre crei oggetti accessibili in modo dinamico, le applicazioni usano meno memoria rispetto a quando tutti i possibili oggetti accessibili sono stati creati in anticipo.

 

 




