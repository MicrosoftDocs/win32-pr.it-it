---
title: Informazioni di base
description: Il Microsoft Active Accessibility, oleacc.dll, crea oggetti proxy che implementano IAccessible per conto dei controlli Windows standard.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d154beb5d824bc722e713346129258c2d294d678a92c1b66d12035ce390f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052959"
---
# <a name="background-information"></a>Informazioni di base

Il Microsoft Active Accessibility, oleacc.dll, crea oggetti proxy che implementano [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per conto dei controlli Windows standard. Poiché questi proxy usano messaggi Windows standard e API specifiche del controllo per raccogliere informazioni su ogni controllo, non esiste alcun meccanismo diretto per personalizzare le informazioni esporli tramite **IAccessible.**

Attualmente, è possibile personalizzare un'implementazione [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) esistente usando le tecniche di sottoclassazione e wrapping. Tuttavia, queste tecniche sono noiose e erre. In realtà, la maggior parte del codice scritto per eseguire l'override di una o due proprietà riguarda l'implementazione di sottoclassi e wrapping; solo una piccola frazione esegue l'attività reale di override delle informazioni. L'annotazione dinamica migliora la situazione fornendo funzionalità simili senza richiedere la scrittura di sottoclassi o il wrapping del codice. È invece possibile concentrarsi sulla fornitura di codice che fornisce le informazioni corrette. L'annotazione dinamica consente agli sviluppatori di passare hint e altre informazioni utili a OLEACC per personalizzare le informazioni esporle. Questa sola funzionalità ridurrà il costo del supporto Microsoft Active Accessibility e consentirà agli sviluppatori di migliorare notevolmente l'accessibilità delle interfacce utente.

 

 




