---
title: Versione formato
description: Il formato del valore della versione è un tipo di dati WORD utilizzato per indicare la versione del formato del flusso.
ms.assetid: 38362a45-4f49-4a85-aabe-452ff32c2812
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503019a3bfe3224e4137ac3bfd43fadbe1e15a3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104516893"
---
# <a name="format-version"></a>Versione formato

Il formato del valore della versione è un tipo di dati **Word** utilizzato per indicare la versione del formato del flusso. Può essere zero o uno. Quando si legge il set di proprietà, è necessario controllare l'indicatore di versione del formato. Se non è zero o uno, il flusso è stato scritto in una specifica diversa e non può essere letto dal codice sviluppato in base a questa specifica.

I set di proprietà con formato versione 1 sono equivalenti alla versione 0, con le aggiunte seguenti:

-   **Nomi proprietà con distinzione tra maiuscole** e minuscole. I nomi delle proprietà vengono archiviati nella proprietà Dictionary riservata, [ID proprietà 0](/windows/desktop/Stg/reserved-property-identifiers). Nei set di proprietà della versione 1, questi nomi possono fare distinzione tra maiuscole e minuscole. La distinzione tra maiuscole e minuscole è determinata dalla proprietà del comportamento riservato, [ID proprietà 0x80000003](/windows/desktop/Stg/reserved-property-identifiers).
-   **Nomi di proprietà Long**. I set di proprietà della versione 1, a differenza dei set di proprietà della versione 0, non sono limitati nella lunghezza dei nomi di proprietà. Per ulteriori informazioni sui nomi delle proprietà, vedere [ID proprietà 0](/windows/desktop/Stg/reserved-property-identifiers) .
-   **Tipi di proprietà**. I set di proprietà della versione 1 possono contenere tutti i tipi di proprietà che possono essere conservati in un set di proprietà della versione 0, oltre ad alcuni tipi aggiuntivi. Per ulteriori informazioni su questi tipi, vedere la struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

 

 