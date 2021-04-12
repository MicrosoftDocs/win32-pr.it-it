---
title: Conversione in JavaScript da JScript
description: Conversione in JavaScript da JScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b18972f407cf008626245798b3f7740d98058e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398678"
---
# <a name="translating-to-javascript-from-jscript"></a>Conversione in JavaScript da JScript

JScript è ampiamente compatibile con JavaScript. Tuttavia, JScript include alcuni oggetti attualmente non supportati da JavaScript, ad esempio ActiveXObject, Enumerator, Error, Global e VBArray.

La versione 5,0 di JScript supporta la gestione delle eccezioni tramite **try**... istruzioni **catch** . JavaScript attualmente non fornisce un meccanismo di gestione degli errori.

Quando si utilizza JScript o JavaScript, esistono alcune sottili differenze tra le implementazioni del modello a oggetti supportate da vari Web browser. Per scrivere script eseguiti in Internet Explorer e Netscape Navigator, limitare le funzionalità usate dagli script a quelle specificate nello standard World Wide Web Consortium (W3C) [per la versione HTML 3,2](https://www.w3.org/tr/rec-html32.html).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in JavaScript](translating-to-javascript.md)
</dt> </dl>

 

 




