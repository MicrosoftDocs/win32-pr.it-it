---
title: Conversione in VBScript da JavaScript
description: Conversione in VBScript da JavaScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6138a6d13710e87ae2b80c979b208d0360e28501ce5d763546a1605c49f0802a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047739"
---
# <a name="translating-to-vbscript-from-javascript"></a>Conversione in VBScript da JavaScript

In JavaScript sono disponibili diversi tipi di dati, ad esempio numeri, stringhe, valori booleani, oggetti e l'attributo Null. VBScript usa un solo tipo di **dati, Variant**, che può essere sottotipato per rappresentare stringhe, numeri, valori booleani e così via.

In JavaScript le matrici possono essere espanse dinamicamente impostando un nuovo valore per la proprietà length della matrice. In VBScript le matrici non possono essere ingrandite. devono essere ridimensionati usando **l'istruzione redim.**

Sia VBScript che JavaScript supportano le funzioni. VBScript, tuttavia, supporta anche le subroutine. Le subroutine sono simili alle funzioni, ma non restituiscono un valore.

JavaScript fa distinzione tra maiuscole e minuscole. VBScript non lo è.

JavaScript è supportato da un'ampia gamma di Web browser, tra cui Internet Explorer e Netscape Navigator. Netscape Navigator non supporta VBScript.

VBScript supporta la gestione degli errori tramite il relativo oggetto Err. JavaScript attualmente non offre un modo per trapping e gestione degli errori.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




