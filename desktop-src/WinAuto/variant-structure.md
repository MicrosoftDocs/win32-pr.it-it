---
title: Struttura VARIANT
description: La maggior parte delle funzioni di Microsoft Active Accessibility e delle proprietà e dei metodi IAccessible accetta una struttura VARIANT come parametro. In pratica, la struttura VARIANT è un contenitore per un'Unione di grandi dimensioni che contiene molti tipi di dati.
ms.assetid: 774dfac8-e258-4266-b81e-072eb3961fb1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cafc63388de27ae01b3e1ca478add6802ac6b85c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117979"
---
# <a name="variant-structure"></a>Struttura VARIANT

La maggior parte delle funzioni di Microsoft Active Accessibility e delle proprietà e dei metodi [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) accetta una struttura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) come parametro. In pratica, la struttura **Variant** è un contenitore per un'Unione di grandi dimensioni che contiene molti tipi di dati.

Il valore nel primo membro della struttura, **VT**, descrive quale dei membri di Unione è valido. Sebbene la struttura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) supporti molti tipi di dati diversi, Microsoft Active Accessibility utilizza solo i tipi seguenti.



| Valore VT     | Nome del membro del valore corrispondente |
|--------------|---------------------------------|
| VT \_ I4       | **lVal**                        |
| \_invio VT | **pdispVal**                    |
| \_BSTR VT     | **bstrVal**                     |
| VT \_ vuoto    | Nessuno                            |



 

Quando si ricevono informazioni in una struttura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , controllare il membro **VT** per individuare il membro che contiene dati validi. Analogamente, quando si inviano informazioni utilizzando una struttura **Variant** , impostare sempre **VT** per riflettere il membro dell'Unione che contiene le informazioni.

Prima di utilizzare la struttura, inizializzarla chiamando la funzione [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) Component Object Model (com). Al termine della struttura, cancellarlo prima che la memoria che contiene la [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) venga liberata chiamando [**VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear).

 

 