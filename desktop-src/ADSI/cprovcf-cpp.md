---
title: CPROVCF. CPP
description: Nel componente provider di esempio un esempio di codice dell'oggetto provider ADs class factory codice è in cprovcf.cpp.
ms.assetid: 53a4da74-3f36-4e6d-ae93-8d595680bcf3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3b77ea7fe1b1d6fe946b9a8b509be33c11f2a075ee658ee305f0f7ba2d2c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023669"
---
# <a name="cprovcfcpp"></a>CPROVCF. CPP

Nel componente provider di esempio un esempio di codice dell'oggetto provider ADs class factory codice è in cprovcf.cpp. Il componente provider non crea mai direttamente un'istanza di questo oggetto in qualsiasi momento diverso da quando l'oggetto viene creato automaticamente durante le operazioni di associazione in [**ADsGetObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject) o la funzione interna nel metodo **getObject** Visual Basic . Il metodo supportato è elencato nella tabella seguente.



| Metodo                                  | Descrizione                                                           |
|-----------------------------------------|-----------------------------------------------------------------------|
| **CSampleDSProviderCF::CreateInstance** | Crea un'istanza del class factory per l'oggetto provider ADS. |



 

 

 




