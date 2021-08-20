---
title: Gestore predefinito e gestori personalizzati
description: Gestore predefinito e gestori personalizzati
ms.assetid: b64617e8-3a71-449d-8948-fd997c1550b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d7c0cbcff81ed8c0aa1e23d4b6713b33943e6ef925a0a22cb06f7102877eda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118103749"
---
# <a name="the-default-handler-and-custom-handlers"></a>Gestore predefinito e gestori personalizzati

Il gestore predefinito, un'implementazione fornita da OLE, viene usato dalla maggior parte delle applicazioni come gestore. Un'applicazione implementa un gestore personalizzato quando le funzionalità del gestore predefinito non sono sufficienti. Un gestore personalizzato può sostituire completamente il gestore predefinito o usare parti della funzionalità fornita laddove appropriato. Nel secondo caso, il gestore dell'applicazione viene implementato come oggetto aggregato costituito da un nuovo oggetto controllo e dal gestore predefinito. I gestori di applicazioni/predefiniti di combinazioni sono noti anche *come gestori in-process.* Il *gestore remoto viene* usato per gli oggetti a cui non è assegnato un CLSID nel Registro di sistema o che non hanno un gestore specificato. Tutto ciò che è necessario da un gestore per questi tipi di oggetti è che passano informazioni attraverso il limite del processo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestori di oggetti](object-handlers.md)
</dt> </dl>

 

 




