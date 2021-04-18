---
title: Conversioni dei tipi di dati
description: Conversioni dei tipi di dati
ms.assetid: 54688ee9-2dd7-466b-b278-13d6f9d1e6ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8135a3fb86fda9ac9ab9666ec42991a8d04d9e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300511"
---
# <a name="data-type-conversions"></a>Conversioni dei tipi di dati

Ogni linguaggio di programmazione definisce determinati tipi e contenitori per i dati. La maggior parte di questi tipi di dati, in particolare le primitive, viene mappata facilmente ad altri linguaggi di programmazione. Alcuni tipi di dati, tuttavia, non hanno alcun equivalente in un altro linguaggio e non possono essere convertiti.

Per informazioni specifiche sui tipi di dati non riconosciuti dal linguaggio di programmazione, vedere gli argomenti seguenti:

-   [Conversione in C++](translating-to-c--.md)
-   [Conversione in Visual Basic](translating-to-visual-basic.md)
-   [Conversione in Java](translating-to-java.md)

Nella tabella seguente sono elencate le conversioni tra linguaggi di programmazione per i tipi di dati comuni.



| C++                                     | Visual Basic             | Java                               | Contiene                                                                                       |
|-----------------------------------------|--------------------------|------------------------------------|------------------------------------------------------------------------------------------------|
| **signed char**<br/>              | Non supportato<br/> | **byte**<br/>                | intero con segno a 1 byte <br/> (VT \_ I1, \[ T \] )<br/>                                   |
| **unsigned char**<br/>            | **Byte**<br/>      | Non supportato<br/>           | Unsigned Integer a 1 byte <br/> (VT \_ UI1, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                 |
| **unsigned char**<br/>            | **Carattere**<br/> | **char**<br/>                | carattere Unicode a 2 byte <br/> (VT \_ UI2, \[ T \] \[ P \] )<br/>                          |
| **short**<br/>                    | **Integer**<br/>   | **short**<br/>               | intero con segno a 2 byte <br/> (VT \_ I2, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                    |
| **unsigned short**<br/>           | Non supportato<br/> | Non supportato<br/>           | Unsigned Integer a 2 byte <br/> (VT \_ UI2, \[ T \] \[ P \] )<br/>                           |
| **int**<br/>                      | **Long**<br/>      | **int**<br/>                 | intero con segno a 4 byte <br/> (VT \_ I4, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                    |
| **int senza segno**<br/>             | Non supportato<br/> | Non supportato<br/>           | Unsigned Integer a 4 byte <br/> (VT \_ UI4, \[ T \] \[ P \] )<br/>                           |
| **\_\_Int64**<br/>                | Non supportato<br/> | **long**<br/>                | intero con segno a 8 byte <br/> (VT \_ I8, \[ T \] \[ P \] )<br/>                              |
| **Int64 senza segno \_ \_**<br/>       | Non supportato<br/> | Non supportato<br/>           | Unsigned Integer a 8 byte <br/> (VT \_ UI8, \[ T \] \[ P \] )<br/>                           |
| **float**<br/>                    | **Singolo**<br/>    | **float**<br/>               | numero a virgola mobile a 4 byte <br/> (VT \_ R4, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>             |
| **double**<br/>                   | **Double**<br/>    | **double**<br/>              | numero a virgola mobile a 8 byte <br/> (VT \_ R8, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>             |
| **BSTR**<br/>                     | **Stringa**<br/>    | **Java. lang. String**<br/>    | Stringa di automazione <br/> (VT \_ BSTR, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                      |
| **BOOL**<br/>                     | **Boolean**<br/>   | **boolean**<br/>             | Boolean <br/> (VT \_ BOOL, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                                |
| **VARIANTE**<br/>                  | **Variante**<br/>   | **com. ms. com. Variant**<br/>  | VARIANT LONTANO\* <br/> (VT \_ VARIANT, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                       |
| [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)<br/> | **object**<br/>    | **com. ms. com. IUnknown**<br/> | Puntatore all'interfaccia IDispatch <br/> (VT \_ DISPATCH, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>        |
| **DATE**<br/>                     | **Data**<br/>      | **com. ms. com. Variant**<br/>  | Data <br/> (VT \_ Data, \[ V \] \[ T \] \[ P \] \[ S \] )<br/>                                   |
| **CURRENCY**<br/>                 | **Valuta**<br/>  | **com. ms. com. Variant**<br/>  | Valuta <br/> (VT \_ CY, \[ v \] \[ t \] \[ P \] \[ S \] o VT \_ Decimal, \[ v \] \[ t \] \[ S \] )<br/> |



 

Per informazioni sui valori VARTYPE e su come usarli, vedere l'argomento [tipi di dati e strutture di IDispatch](/previous-versions/ms221600(v=vs.100)).

Le conversioni dei tipi di dati tra i linguaggi di scripting sono più semplici rispetto a quelle per i linguaggi di programmazione. JScript e JavaScript supportano entrambi gli stessi tipi di dati e VBScript supporta solo un singolo tipo di dati, **Variant**. Pertanto, tutti i tipi di dati JScript e JavaScript diventano tipi **Variant** quando vengono convertiti in VBScript. Quando si converte VBScript in JScript o JavaScript, i tipi **Variant** diventano numeri, stringhe, valori booleani e così via.

 

