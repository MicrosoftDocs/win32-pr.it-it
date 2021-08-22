---
title: Struttura VARIANT
description: La maggior parte Microsoft Active Accessibility funzioni e metodi IAccessible accettano una struttura VARIANT come parametro. Essenzialmente, la struttura VARIANT è un contenitore per un'unione di grandi dimensioni che contiene molti tipi di dati.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 063d1e17d998f3cb7d70a0a271e55f02628e7864164e00becb5a708af371e12c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563549"
---
# <a name="variant-structure"></a>Struttura VARIANT

La maggior parte Microsoft Active Accessibility funzioni e [**metodi IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) accettano una [**struttura VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) come parametro. Essenzialmente, la **struttura VARIANT** è un contenitore per un'unione di grandi dimensioni che contiene molti tipi di dati.

Il valore nel primo membro della struttura , **vt**, descrive quale dei membri dell'unione è valido. Anche se [**la struttura VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) supporta molti tipi di dati diversi, Microsoft Active Accessibility solo i tipi seguenti.



| Valore vt     | Nome del membro valore corrispondente |
|--------------|---------------------------------|
| VT \_ I4       | **lVal**                        |
| VT \_ DISPATCH | **pdispVal**                    |
| VT \_ BSTR     | **bstrVal**                     |
| VT \_ EMPTY    | Nessuno                            |



 

Quando si ricevono informazioni in una [**struttura VARIANT,**](/windows/win32/api/oaidl/ns-oaidl-variant) controllare il membro **vt** per scoprire quale membro contiene dati validi. Analogamente, quando si inviano informazioni usando una **struttura VARIANT,** impostare sempre **vt** in modo che rifletta il membro di unione che contiene le informazioni.

Prima di usare la struttura , inizializzarla chiamando la funzione [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model (COM). Al termine della struttura , cancellarla prima che la memoria che contiene [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) venga liberata chiamando [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).

 

 