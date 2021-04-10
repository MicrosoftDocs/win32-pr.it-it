---
description: L'attributo cutpoint specifica quando una transizione passa da un'origine all'altra, se viene eseguito il rendering della transizione come taglia. Il valore è relativo all'inizio della transizione.
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: Attributo cutpoint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd516bd67577906a0a06d8da692ffbd7563ce32f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124596"
---
# <a name="cutpoint-attribute"></a>Attributo cutpoint

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `cutpoint` attributo specifica quando una transizione passa da un'origine all'altra, se viene eseguito il rendering della transizione come taglia. Il valore è relativo all'inizio della transizione.

## <a name="possible-values"></a>Valori possibili

Deve essere una stringa con formato *hh: mm: SS. FF* , dove *HH* = hours, *mm* = minutes, *SS* = seconds e *FF* = frazioni di secondi. Esempio: 1:04:30.512. È possibile omettere le unità iniziali. Ad esempio, 3:00 (tre minuti) e 45 (45 secondi) sono entrambi validi.

## <a name="applies-to"></a>Si applica a

[**transizione**](transition-element.md)

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Attributi XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 



