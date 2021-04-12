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
# <a name="translating-to-javascript-from-jscript"></a><span data-ttu-id="c4a32-103">Conversione in JavaScript da JScript</span><span class="sxs-lookup"><span data-stu-id="c4a32-103">Translating to JavaScript from JScript</span></span>

<span data-ttu-id="c4a32-104">JScript è ampiamente compatibile con JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c4a32-104">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="c4a32-105">Tuttavia, JScript include alcuni oggetti attualmente non supportati da JavaScript, ad esempio ActiveXObject, Enumerator, Error, Global e VBArray.</span><span class="sxs-lookup"><span data-stu-id="c4a32-105">However, JScript includes some objects not currently supported by JavaScript, such as ActiveXObject, Enumerator, Error, Global, and VBArray.</span></span>

<span data-ttu-id="c4a32-106">La versione 5,0 di JScript supporta la gestione delle eccezioni tramite **try**... istruzioni **catch** .</span><span class="sxs-lookup"><span data-stu-id="c4a32-106">JScript version 5.0 supports exception handling through **try**...**catch** statements.</span></span> <span data-ttu-id="c4a32-107">JavaScript attualmente non fornisce un meccanismo di gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="c4a32-107">JavaScript does not currently provide an error-handing mechanism.</span></span>

<span data-ttu-id="c4a32-108">Quando si utilizza JScript o JavaScript, esistono alcune sottili differenze tra le implementazioni del modello a oggetti supportate da vari Web browser.</span><span class="sxs-lookup"><span data-stu-id="c4a32-108">When working with either JScript or JavaScript, there are some subtle differences between the object model implementations supported by various Web browsers.</span></span> <span data-ttu-id="c4a32-109">Per scrivere script eseguiti in Internet Explorer e Netscape Navigator, limitare le funzionalità usate dagli script a quelle specificate nello standard World Wide Web Consortium (W3C) [per la versione HTML 3,2](https://www.w3.org/tr/rec-html32.html).</span><span class="sxs-lookup"><span data-stu-id="c4a32-109">To write script that runs on both Internet Explorer and Netscape Navigator, limit the features used by your scripts to those specified in the World Wide Web Consortium (W3C) [standard for HTML version 3.2](https://www.w3.org/tr/rec-html32.html).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4a32-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4a32-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4a32-111">Conversione in JavaScript</span><span class="sxs-lookup"><span data-stu-id="c4a32-111">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> </dl>

 

 




