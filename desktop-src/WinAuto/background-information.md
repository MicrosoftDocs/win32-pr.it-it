---
title: Informazioni di base
description: Il componente Microsoft Active Accessibility, oleacc.dll, crea oggetti proxy che implementano IAccessible per conto dei controlli Windows standard.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a9b044f8035a474f02b8457dc99ec39aca73c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116765"
---
# <a name="background-information"></a>Informazioni di base

Il componente Microsoft Active Accessibility, oleacc.dll, crea oggetti proxy che implementano [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per conto dei controlli Windows standard. Poiché questi proxy usano i messaggi Windows standard e le API specifiche del controllo per raccogliere informazioni su ogni controllo, non esiste alcun meccanismo diretto per la personalizzazione delle informazioni che questi proxy espongono tramite **IAccessible**.

Attualmente, è possibile personalizzare un'implementazione di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) esistente mediante tecniche di creazione di sottoclassi e wrapping. Tuttavia, queste tecniche sono noiose e soggette a errori. Infatti, la maggior parte del codice scritto per eseguire l'override di una o due proprietà riguarda l'implementazione della sottoclasse e del wrapping; solo una piccola frazione esegue la vera attività di override delle informazioni. L'annotazione dinamica migliora la situazione fornendo funzionalità simili senza richiedere la scrittura di codice per la creazione di sottoclassi o il ritorno a capo. È invece possibile concentrarsi sulla fornitura di codice che fornisca le informazioni corrette. L'annotazione dinamica consente agli sviluppatori di passare hint e altre informazioni utili a OLEACC per personalizzare le informazioni che espone. Questa funzionalità consente di ridurre il costo del supporto di Microsoft Active Accessibility e di consentire agli sviluppatori di migliorare notevolmente l'accessibilità delle interfacce utente.

 

 




