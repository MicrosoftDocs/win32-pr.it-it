---
description: "Quando un'applicazione esegue un'operazione IPropertyStorage:: WriteMultiple su qualsiasi proprietà WIA (Windows Image Acquisition) scrivibile, il driver WIA esegue una convalida sul nuovo valore della proprietà."
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: Convalida della proprietà WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60d9e64122e19249c19bc47564631162d783920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226134"
---
# <a name="wia-property-validation"></a>Convalida della proprietà WIA

Quando un'applicazione esegue un'operazione [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) su qualsiasi proprietà WIA (Windows Image Acquisition) scrivibile, il driver WIA esegue una convalida sul nuovo valore della proprietà. La scrittura di una proprietà può avere effetti collaterali che modificano altri valori di proprietà. È necessario che l'applicazione legga tutti i valori delle proprietà dopo un'operazione di scrittura per determinare che tutte le proprietà sono impostate sui valori desiderati dall'applicazione.

È possibile scrivere più proprietà contemporaneamente usando l'operazione [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) . In alcuni casi è possibile che alcune assegnazioni di proprietà siano in conflitto. In questi casi, la priorità usata per risolvere i conflitti è la seguente:

1.  \_finalità del cur degli indirizzi IP WIA \_ \_
2.  tipo di dati \_ IPA WIA \_
3.  \_profondità IPA \_ WIA
4.  \_indirizzi IP WIA \_ XRES
5.  \_indirizzi IP WIA \_ YRES
6.  \_indirizzi IP WIA \_ XPos
7.  \_indirizzi IP WIA \_ YPos
8.  \_indirizzi IP WIA \_ stampa
9.  \_indirizzi IP WIA \_ YEXTENT

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
