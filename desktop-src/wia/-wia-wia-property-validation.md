---
description: Quando un'applicazione esegue un'operazione IPropertyStorage::WriteMultiple su qualsiasi proprietà WIA (Windows Image Acquisition) scrivibile, il driver WIA esegue una convalida sul nuovo valore della proprietà.
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: Convalida delle proprietà WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1aca5879dbcb789b7e94a780c8fc99e53b703f6aea74498ae455e8e2ec6b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813051"
---
# <a name="wia-property-validation"></a>Convalida delle proprietà WIA

Quando un'applicazione esegue [un'operazione IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) su qualsiasi proprietà WIA (Windows Image Acquisition) scrivibile, il driver WIA esegue una convalida sul nuovo valore della proprietà. La scrittura di una proprietà può avere effetti collaterali che modificano altri valori di proprietà. L'applicazione deve leggere tutti i valori delle proprietà dopo un'operazione di scrittura per determinare che tutte le proprietà sono impostate su valori desiderati dall'applicazione.

È possibile scrivere più proprietà contemporaneamente usando [l'operazione IPropertyStorage::WriteMultiple.](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) In alcuni casi alcune assegnazioni di proprietà sono in conflitto. In questi casi, la priorità usata per risolvere i conflitti è la seguente:

1.  FINALITÀ CUR DI WIA \_ IPS \_ \_
2.  TIPO \_ DI DATI IPA DI WIA \_
3.  PROFONDITÀ \_ IPA DI WIA \_
4.  WIA \_ IPS \_ XRES
5.  WIA \_ IPS \_ YRES
6.  WIA \_ IPS \_ XPOS
7.  WIA \_ IPS \_ YPOS
8.  WIA \_ IPS \_ XEXTENT
9.  WIA \_ IPS \_ YEXTENT

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
