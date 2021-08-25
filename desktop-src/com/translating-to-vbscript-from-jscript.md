---
title: Conversione in VBScript da JScript
description: Conversione in VBScript da JScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3900ba82b258e6ee19cf06edb2f97247033778da5fcabaffe4a854e66a5fef73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992251"
---
# <a name="translating-to-vbscript-from-jscript"></a>Conversione in VBScript da JScript

In VBScript, **for**... **Ogni** ciclo enumera i membri di una raccolta. in JScript, **per**... **il** ciclo in enumera i membri di un JScript o di una matrice. Per enumerare una raccolta in JScript, usare un oggetto Enumerator.

JScript fornisce l'oggetto Error, che può essere usato per intercettare e gestire gli errori. L'oggetto Error è analogo all'oggetto VBScript Err.

In JScript sono disponibili diversi tipi di dati, ad esempio numeri, stringhe, valori booleani, oggetti e l'attributo Null. VBScript usa un solo tipo di dati, **Variant,** che può essere sottotipato per rappresentare stringhe, numeri, valori booleani e così via.

In JScript, le matrici possono essere espanse dinamicamente impostando un nuovo valore per la proprietà length della matrice. In VBScript le matrici non possono essere ingrandite. Devono essere ridimensionati usando **l'istruzione redim.**

Sia VBScript che JScript supportano le funzioni . VBScript, tuttavia, supporta anche subroutine. Le subroutine sono simili alle funzioni, ma non restituiscono un valore.

JScript fa distinzione tra maiuscole e minuscole. VBScript non lo è.

JScript è supportato da un'ampia gamma di Web browser, tra cui Internet Explorer e Netscape Navigator. Netscape Navigator non supporta VBScript.

JScript matrici non sono matrici del tipo di variabile **VARIANT SAFEARRAY**. Uno JScript script deve usare un oggetto VBArray per accedere alla **variabile VARIANT SAFEARRAY.** Gli script VBScript possono accedere **direttamente alle variabili VARIANT SAFEARRAY.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




