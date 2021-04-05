---
description: Nel frammento di codice seguente viene illustrata la pubblicazione di un oggetto utente in un server ILS. Dopo la pubblicazione di un oggetto utente, le entità remote possono utilizzare l'oggetto utente per effettuare chiamate all'utente specificato.
ms.assetid: 8b68886c-0df5-4005-bcd5-1a18336f5192
title: Aggiunta di un oggetto utente a un server ILS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85b15dcdbca47187cf4155dfbf7535d06718c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750783"
---
# <a name="adding-a-user-object-to-an-ils-server"></a>Aggiunta di un oggetto utente a un server ILS

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Nel frammento di codice seguente viene illustrata la pubblicazione di un oggetto utente in un server ILS. Dopo la pubblicazione di un oggetto utente, le entità remote possono utilizzare l'oggetto utente per effettuare chiamate all'utente specificato.

Questo frammento presuppone che la [connessione a un server ILS](connecting-to-an-ils-server.md) sia già stata eseguita.


```C++
hr = pDirectory->AddDirectoryObject(pDirectoryObject);
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)
</dt> <dt>

[**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)
</dt> <dt>

[**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)
</dt> </dl>

 

 



