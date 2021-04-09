---
title: Conversione in VBScript da JScript
description: Conversione in VBScript da JScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f5ac608e94f883edc3b319fd04625e9a08d18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044404"
---
# <a name="translating-to-vbscript-from-jscript"></a>Conversione in VBScript da JScript

In VBScript, **per**... **Ogni** ciclo enumera i membri di una raccolta. in JScript, **per**... **in** loop enumera i membri di un oggetto o di una matrice JScript. Per enumerare una raccolta in JScript, utilizzare un oggetto enumeratore.

JScript fornisce l'oggetto Error, che può essere usato per intercettare e gestire gli errori. L'oggetto Error è analogo all'oggetto Err di VBScript.

In JScript sono disponibili diversi tipi di dati, ad esempio numeri, stringhe, valori booleani, oggetti e l'attributo null. VBScript utilizza un solo tipo di dati, **Variant**, che può essere sottotipo per rappresentare stringhe, numeri, valori booleani e così via.

In JScript, le matrici possono essere espanse in modo dinamico impostando un nuovo valore per la proprietà lunghezza della matrice. In VBScript non è possibile ingrandire le matrici; è necessario ridimensionarli usando l'istruzione **ReDim** .

Entrambe le funzioni di supporto VBScript e JScript. VBScript, tuttavia, supporta anche subroutine. Le subroutine sono simili alle funzioni, ma non restituiscono un valore.

JScript distingue tra maiuscole e minuscole. VBScript non è.

JScript è supportato da un'ampia gamma di Web browser, tra cui Internet Explorer e Netscape Navigator. Netscape Navigator non supporta VBScript.

Le matrici JScript non sono matrici della variabile di tipo **SafeArray VARIANT**. Uno script JScript deve usare un oggetto VBArray per accedere alla variabile **SafeArray VARIANT**. Gli script VBScript possono accedere direttamente alle variabili **SafeArray VARIANT**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




