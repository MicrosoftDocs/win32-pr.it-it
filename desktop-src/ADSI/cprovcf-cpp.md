---
title: CPROVCF. CPP
description: Nel componente provider di esempio, un esempio di codice dell'oggetto provider ADs class factory codice si trova in cprovcf. cpp.
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d086cd79086f40bab6d898b844ed52fc0161bc7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470814"
---
# <a name="cprovcfcpp"></a>CPROVCF. CPP

Nel componente provider di esempio, un esempio di codice dell'oggetto provider ADs class factory codice si trova in cprovcf. cpp. Il componente provider non crea mai direttamente un'istanza di questo oggetto in un momento diverso da quello in cui l'oggetto viene creato automaticamente durante le operazioni di associazione in [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) o nella funzione interna del Visual Basic metodo **GetObject**. Il metodo supportato è elencato nella tabella seguente.



| Metodo                                  | Descrizione                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| **CSampleDSProviderCF:: CreateInstance** | Crea un'istanza della class factory per l'oggetto provider ADS. |



 

 

 




