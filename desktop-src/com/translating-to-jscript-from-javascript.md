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
# <a name="translating-to-jscript-from-javascript"></a><span data-ttu-id="e44b5-103">Conversione in JScript da JavaScript</span><span class="sxs-lookup"><span data-stu-id="e44b5-103">Translating to JScript from JavaScript</span></span>

<span data-ttu-id="e44b5-104">JScript è ampiamente compatibile con JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e44b5-104">JScript is largely compatible with JavaScript.</span></span> <span data-ttu-id="e44b5-105">Tuttavia, la versione 5,0 di JScript include alcuni oggetti attualmente non supportati da JavaScript, ad esempio ActiveXObject, Enumerator, Error, Global e VBArray.</span><span class="sxs-lookup"><span data-stu-id="e44b5-105">However, JScript version 5.0 includes some objects not currently supported by JavaScript, such as ActiveXObject, Enumerator, Error, Global, and VBArray.</span></span>

<span data-ttu-id="e44b5-106">JScript 5,0 supporta la gestione delle eccezioni tramite **try**... istruzioni **catch** .</span><span class="sxs-lookup"><span data-stu-id="e44b5-106">JScript 5.0 supports exception handling through **try**...**catch** statements.</span></span> <span data-ttu-id="e44b5-107">JavaScript attualmente non fornisce un meccanismo di gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="e44b5-107">JavaScript does not currently provide an error-handing mechanism.</span></span>

<span data-ttu-id="e44b5-108">Quando si utilizza JScript o JavaScript, esistono alcune sottili differenze tra le implementazioni del modello a oggetti supportate da vari Web browser.</span><span class="sxs-lookup"><span data-stu-id="e44b5-108">When working with either JScript or JavaScript, there are some subtle differences between the object model implementations supported by various Web browsers.</span></span> <span data-ttu-id="e44b5-109">Per scrivere script eseguiti in Internet Explorer e Netscape Navigator, limitare le funzionalità usate dagli script a quelle specificate nello standard World Wide Web Consortium (W3C) per la versione HTML 3,2.</span><span class="sxs-lookup"><span data-stu-id="e44b5-109">To write script that runs on both Internet Explorer and Netscape Navigator, limit the features used by your scripts to those specified in the World Wide Web Consortium (W3C) standard for HTML version 3.2.</span></span> <span data-ttu-id="e44b5-110">Per ulteriori informazioni su questo standard, vedere la [specifica di riferimento HTML 3,2](https://www.w3.org/TR/REC-html32.html).</span><span class="sxs-lookup"><span data-stu-id="e44b5-110">For more information about this standard, see [HTML 3.2 Reference Specification](https://www.w3.org/TR/REC-html32.html).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e44b5-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e44b5-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e44b5-112">Conversione in JScript</span><span class="sxs-lookup"><span data-stu-id="e44b5-112">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




