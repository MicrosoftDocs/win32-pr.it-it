---
title: Conversione in VBScript da JavaScript
description: Conversione in VBScript da JavaScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eda8169a665dc93133f7ac933de12ecc612f3e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297973"
---
# <a name="translating-to-vbscript-from-javascript"></a>Conversione in VBScript da JavaScript

In JavaScript sono disponibili diversi tipi di dati, ad esempio numeri, stringhe, valori booleani, oggetti e l'attributo null. VBScript utilizza un solo tipo di dati, **Variant**, che può essere sottotipo per rappresentare stringhe, numeri, valori booleani e così via.

In JavaScript, le matrici possono essere espanse dinamicamente impostando un nuovo valore per la proprietà lunghezza della matrice. In VBScript non è possibile ingrandire le matrici; è necessario ridimensionarli usando l'istruzione **ReDim** .

Funzioni di supporto sia per VBScript che per JavaScript. VBScript, tuttavia, supporta anche subroutine. Le subroutine sono simili alle funzioni, ad eccezione del fatto che non restituiscono un valore.

JavaScript fa distinzione tra maiuscole e minuscole. VBScript non è.

JavaScript è supportato da un'ampia gamma di Web browser, tra cui Internet Explorer e Netscape Navigator. Netscape Navigator non supporta VBScript.

VBScript supporta la gestione degli errori tramite il relativo oggetto Err. JavaScript attualmente non fornisce un mezzo per intercettare e gestire gli errori.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in VBScript](translating-to-vbscript.md)
</dt> </dl>

 

 




