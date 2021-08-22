---
title: Delega di QueryInterface
description: Delega di QueryInterface
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c63a9eb336bcf049877957bd55523ee70de489263bd19e0ebece8b65fbdd0ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501211"
---
# <a name="delegation-of-queryinterface"></a>Delega di QueryInterface

I gestori che richiedono l'accesso ad alcune interfacce interne nella gestione proxy devono passare attraverso [**l'interfaccia IInternalUnknown.**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) In questo modo si impedisce ai gestori di delegare ed esporre le interfacce interne dell'aggregazione all'esterno dell'aggregazione. Queste interfacce includono [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e [**IMultiQI.**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi) Se il gestore vuole esporre **IClientSecurity** o **IMultiQI,** deve implementarli.

Nel caso di [**IClientSecurity,**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)se il client tenta di impostare la sicurezza su un'interfaccia esposta dal gestore, il gestore deve impostare la sicurezza sul proxy dell'interfaccia di rete sottostante.

Nel caso di [**IMultiQI,**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi)il gestore deve compilare le interfacce di cui è a conoscenza e quindi inoltrare la chiamata al gestore proxy per ottenere il resto delle interfacce compilate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestore Client-Side lightweight](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 