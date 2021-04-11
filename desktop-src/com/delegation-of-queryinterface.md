---
title: Delega di QueryInterface
description: Delega di QueryInterface
ms.assetid: c5c1b584-9ca3-4dc4-a769-0142e5d8790a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e062f3d063d4f23c941182d80170cec0a680c6f3
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118510"
---
# <a name="delegation-of-queryinterface"></a>Delega di QueryInterface

I gestori che richiedono l'accesso ad alcune interfacce interne di gestione proxy devono passare attraverso l'interfaccia [**IInternalUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-iinternalunknown) . Ciò impedisce ai gestori di delegare in modo cieco ed esporre le interfacce interne dell'aggregazione al di fuori dell'aggregazione. Queste interfacce includono [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi). Se il gestore vuole esporre **IClientSecurity** o **IMultiQI**, deve implementarli.

Nel caso di [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity), se il client tenta di impostare la sicurezza su un'interfaccia esposta dal gestore, il gestore deve impostare la sicurezza sul proxy dell'interfaccia di rete sottostante.

Nel caso di [**IMultiQI**](/windows/win32/api/objidlbase/nn-objidlbase-imultiqi), il gestore deve compilare le interfacce che conosce e quindi inviare la chiamata a gestione proxy per ottenere il resto delle interfacce compilate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestore di Client-Side Lightweight](the-lightweight-client-side-handler.md)
</dt> </dl>

 

 