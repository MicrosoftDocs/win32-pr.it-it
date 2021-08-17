---
title: Conversione in JScript da JavaScript
description: Conversione in JScript da JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c25276d569c5b461693a666d1bf8cf706b6896c0995972e1d2af0071c5760b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129563"
---
# <a name="translating-to-jscript-from-javascript"></a>Conversione in JScript da JavaScript

JScript è in gran parte compatibile con JavaScript. Tuttavia, JScript versione 5.0 include alcuni oggetti non attualmente supportati da JavaScript, ad esempio ActiveXObject, Enumerator, Error, Global e VBArray.

JScript 5.0 supporta la gestione delle eccezioni tramite **try**... **Istruzioni catch.** JavaScript attualmente non fornisce un meccanismo di gestione degli errori.

Quando si lavora con JScript o JavaScript, esistono alcune piccole differenze tra le implementazioni del modello a oggetti supportate da diversi Web browser. Per scrivere script che vengono eseguiti in Internet Explorer e Netscape Navigator, limitare le funzionalità usate dagli script a quelle specificate nello standard World Wide Web Consortium (W3C) per HTML versione 3.2. Per altre informazioni su questo standard, vedere [HTML 3.2 Reference Specification](https://www.w3.org/TR/REC-html32.html).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Traduzione in JScript](translating-to-jscript.md)
</dt> </dl>

 

 




