---
title: Conversione in JScript da VBScript
description: Conversione in JScript da VBScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18c2ccb11ffa4f5f000d8cfc73f7db6f857cf6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708032"
---
# <a name="translating-to-jscript-from-vbscript"></a>Conversione in JScript da VBScript

In VBScript, **per**... **Ogni** ciclo enumera i membri di una raccolta. in JScript, **per**... **in** loop enumera i membri di un oggetto o di una matrice JScript. Per enumerare una raccolta in JScript, utilizzare un oggetto enumeratore.

In JScript sono disponibili diversi tipi di dati, ad esempio numeri, stringhe, valori booleani, oggetti e l'attributo null. VBScript utilizza un solo tipo di dati, **Variant**, che può essere sottotipo per rappresentare stringhe, numeri, valori booleani e così via.

In JScript, le matrici possono essere espanse in modo dinamico impostando un nuovo valore per la proprietà lunghezza della matrice. In VBScript non è possibile ingrandire le matrici; è necessario ridimensionarli usando l'istruzione **ReDim** .

Entrambe le funzioni di supporto VBScript e JScript. VBScript, tuttavia, supporta anche subroutine. Le subroutine sono simili alle funzioni, ma non restituiscono un valore.

JScript distingue tra maiuscole e minuscole. VBScript non è.

JScript è supportato sia da Internet Explorer che dal navigatore Netscape. Netscape Navigator non supporta VBScript.

JScript fornisce l'oggetto Error, che può essere usato per intercettare e gestire gli errori. L'oggetto Error è analogo all'oggetto Err di VBScript.

Le matrici JScript non sono matrici della variabile di tipo **SafeArray VARIANT**. Se lo script riceve una variabile **SafeArray VARIANT** da un oggetto com o da uno script VBScript, deve usare un oggetto VBArray per accedere alla variabile **SafeArray VARIANT** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in JScript](translating-to-jscript.md)
</dt> </dl>

 

 




