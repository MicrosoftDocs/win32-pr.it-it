---
title: Traduzione in JavaScript da JScript
description: Traduzione in JavaScript da JScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c4adb5827952cc9bab0dac268997b5b73a52ecd1403e5431cdb3939b08c7e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129583"
---
# <a name="translating-to-javascript-from-jscript"></a>Traduzione in JavaScript da JScript

JScript è in gran parte compatibile con JavaScript. Tuttavia, JScript alcuni oggetti non attualmente supportati da JavaScript, ad esempio ActiveXObject, Enumerator, Error, Global e VBArray.

JScript versione 5.0 supporta la gestione delle eccezioni tramite **try**... **Istruzioni catch.** JavaScript attualmente non fornisce un meccanismo di gestione degli errori.

Quando si lavora con JScript o JavaScript, esistono alcune piccole differenze tra le implementazioni del modello a oggetti supportate da diversi Web browser. Per scrivere script in esecuzione in Internet Explorer e Netscape Navigator, limitare le funzionalità usate dagli script a quelle specificate nello standard World Wide Web Consortium (W3C) per [HTML versione 3.2.](https://www.w3.org/tr/rec-html32.html)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in JavaScript](translating-to-javascript.md)
</dt> </dl>

 

 




