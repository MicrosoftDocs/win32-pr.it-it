---
title: Conversione in JScript da JavaScript
description: Conversione in JScript da JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45535807a5ef2baf59c2e068007a5a8df8bf4863
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104516642"
---
# <a name="translating-to-jscript-from-javascript"></a>Conversione in JScript da JavaScript

JScript è ampiamente compatibile con JavaScript. Tuttavia, la versione 5,0 di JScript include alcuni oggetti attualmente non supportati da JavaScript, ad esempio ActiveXObject, Enumerator, Error, Global e VBArray.

JScript 5,0 supporta la gestione delle eccezioni tramite **try**... istruzioni **catch** . JavaScript attualmente non fornisce un meccanismo di gestione degli errori.

Quando si utilizza JScript o JavaScript, esistono alcune sottili differenze tra le implementazioni del modello a oggetti supportate da vari Web browser. Per scrivere script eseguiti in Internet Explorer e Netscape Navigator, limitare le funzionalità usate dagli script a quelle specificate nello standard World Wide Web Consortium (W3C) per la versione HTML 3,2. Per ulteriori informazioni su questo standard, vedere la [specifica di riferimento HTML 3,2](https://www.w3.org/TR/REC-html32.html).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione in JScript](translating-to-jscript.md)
</dt> </dl>

 

 




