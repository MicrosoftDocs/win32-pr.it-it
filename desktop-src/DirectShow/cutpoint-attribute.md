---
description: L'attributo cutpoint specifica quando una transizione viene tagliata da un'origine a quella successiva, se viene eseguito il rendering della transizione come taglio. Il valore è relativo all'inizio della transizione.
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: Attributo cutpoint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7332d3ef1b608b192b18e0d32bc99bce547058754950847e0a9767eb500a1553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654592"
---
# <a name="cutpoint-attribute"></a>Attributo cutpoint

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

`cutpoint`L'attributo specifica quando una transizione viene tagliata da un'origine a quella successiva, se viene eseguito il rendering della transizione come taglio. Il valore è relativo all'inizio della transizione.

## <a name="possible-values"></a>Valori possibili

Deve essere una stringa nel formato *hh:mm:ss.ff,* dove *hh* = ore, mm = *minuti,* *ss* = secondi e *ff* = frazioni di secondi. Esempio: 1:04:30.512. Le unità iniziali possono essere omesse. Ad esempio, 3:00 (tre minuti) e 45 (45 secondi) sono entrambi validi.

## <a name="applies-to"></a>Si applica a

[**Transizione**](transition-element.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 



