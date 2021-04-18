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
# <a name="translating-to-vbscript-from-javascript"></a><span data-ttu-id="880a9-103">Conversione in VBScript da JavaScript</span><span class="sxs-lookup"><span data-stu-id="880a9-103">Translating to VBScript from JavaScript</span></span>

<span data-ttu-id="880a9-104">In JavaScript sono disponibili diversi tipi di dati, ad esempio numeri, stringhe, valori booleani, oggetti e l'attributo null.</span><span class="sxs-lookup"><span data-stu-id="880a9-104">In JavaScript, there are several data types, such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="880a9-105">VBScript utilizza un solo tipo di dati, **Variant**, che può essere sottotipo per rappresentare stringhe, numeri, valori booleani e così via.</span><span class="sxs-lookup"><span data-stu-id="880a9-105">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="880a9-106">In JavaScript, le matrici possono essere espanse dinamicamente impostando un nuovo valore per la proprietà lunghezza della matrice.</span><span class="sxs-lookup"><span data-stu-id="880a9-106">In JavaScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="880a9-107">In VBScript non è possibile ingrandire le matrici; è necessario ridimensionarli usando l'istruzione **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="880a9-107">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="880a9-108">Funzioni di supporto sia per VBScript che per JavaScript.</span><span class="sxs-lookup"><span data-stu-id="880a9-108">Both VBScript and JavaScript support functions.</span></span> <span data-ttu-id="880a9-109">VBScript, tuttavia, supporta anche subroutine.</span><span class="sxs-lookup"><span data-stu-id="880a9-109">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="880a9-110">Le subroutine sono simili alle funzioni, ad eccezione del fatto che non restituiscono un valore.</span><span class="sxs-lookup"><span data-stu-id="880a9-110">Subroutines are similar to functions, except they do not return a value.</span></span>

<span data-ttu-id="880a9-111">JavaScript fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="880a9-111">JavaScript is case-sensitive.</span></span> <span data-ttu-id="880a9-112">VBScript non è.</span><span class="sxs-lookup"><span data-stu-id="880a9-112">VBScript is not.</span></span>

<span data-ttu-id="880a9-113">JavaScript è supportato da un'ampia gamma di Web browser, tra cui Internet Explorer e Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="880a9-113">JavaScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="880a9-114">Netscape Navigator non supporta VBScript.</span><span class="sxs-lookup"><span data-stu-id="880a9-114">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="880a9-115">VBScript supporta la gestione degli errori tramite il relativo oggetto Err.</span><span class="sxs-lookup"><span data-stu-id="880a9-115">VBScript supports error handling through its Err object.</span></span> <span data-ttu-id="880a9-116">JavaScript attualmente non fornisce un mezzo per intercettare e gestire gli errori.</span><span class="sxs-lookup"><span data-stu-id="880a9-116">JavaScript does not currently provide a means of trapping and handling errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="880a9-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="880a9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="880a9-118">Conversione in VBScript</span><span class="sxs-lookup"><span data-stu-id="880a9-118">Translating to VBScript</span></span>](translating-to-vbscript.md)
</dt> </dl>

 

 




