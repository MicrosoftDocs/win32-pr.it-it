---
title: Gestore predefinito e gestori personalizzati
description: Gestore predefinito e gestori personalizzati
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dfd152a9f7b20b8ba1553db4efc9b57bffef60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955293"
---
# <a name="the-default-handler-and-custom-handlers"></a>Gestore predefinito e gestori personalizzati

Il gestore predefinito, un'implementazione fornita da OLE, viene usato dalla maggior parte delle applicazioni come gestore. Un'applicazione implementa un gestore personalizzato quando le funzionalità del gestore predefinite non sono sufficienti. Un gestore personalizzato può sostituire completamente il gestore predefinito o usare parti della funzionalità che fornisce laddove appropriato. Nel secondo caso, il gestore dell'applicazione viene implementato come un oggetto aggregato costituito da un nuovo oggetto controllo e dal gestore predefinito. I gestori di applicazione/predefiniti combinati sono noti anche come *gestori in-process*. Il *gestore di comunicazione remota* viene usato per gli oggetti a cui non è assegnato un CLSID nel registro di sistema o che non hanno alcun gestore specificato. Tutto ciò che è necessario da un gestore per questi tipi di oggetti è che passano informazioni attraverso il limite del processo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestori di oggetti](object-handlers.md)
</dt> </dl>

 

 




