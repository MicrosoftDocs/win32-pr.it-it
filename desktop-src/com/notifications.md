---
title: Notifiche (COM)
description: Notifiche
ms.assetid: 060c012c-5f74-4a4c-bec3-e9072f920442
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4668322428a9580fd4c9c9ea5edfb395081cc50
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474932"
---
# <a name="notifications-com"></a>Notifiche (COM)

Le notifiche sono callback generate da un oggetto quando viene rilevata una modifica nel nome, nello stato, nei dati o nella presentazione. Per i contenitori e gli altri client è necessario che le notifiche rispondano in modo appropriato a tali modifiche. Un contenitore viene registrato per ricevere le notifiche impostando una connessione consultiva a un oggetto di interesse. Altri client interessati possono eseguire la stessa operazione. Il contenitore crea anche un sink consultivo per ricevere le notifiche. Utilizzando la connessione stabilita dal contenitore, un oggetto che subisce una modifica notifica il sink consultivo. Al momento della ricezione di una notifica, il contenitore acquisisce qualsiasi azione definita per il tipo di modifica che si è verificato.

Per altre informazioni, vedere i seguenti argomenti:

-   [Tipi di notifiche](types-of-notifications.md)
-   [Come funzionano le notifiche](how-notifications-work.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> </dl>

 

 




