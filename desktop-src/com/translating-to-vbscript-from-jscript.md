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
# <a name="translating-to-vbscript-from-jscript"></a><span data-ttu-id="78440-103">Conversione in VBScript da JScript</span><span class="sxs-lookup"><span data-stu-id="78440-103">Translating to VBScript from JScript</span></span>

<span data-ttu-id="78440-104">In VBScript, **per**... **Ogni** ciclo enumera i membri di una raccolta. in JScript, **per**... **in** loop enumera i membri di un oggetto o di una matrice JScript.</span><span class="sxs-lookup"><span data-stu-id="78440-104">In VBScript, the **For**...**Each** loop enumerates the members of a collection; in JScript, the **for**...**in** loop enumerates the members of a JScript object or array.</span></span> <span data-ttu-id="78440-105">Per enumerare una raccolta in JScript, utilizzare un oggetto enumeratore.</span><span class="sxs-lookup"><span data-stu-id="78440-105">To enumerate a collection in JScript, use an Enumerator object.</span></span>

<span data-ttu-id="78440-106">JScript fornisce l'oggetto Error, che può essere usato per intercettare e gestire gli errori.</span><span class="sxs-lookup"><span data-stu-id="78440-106">JScript provides the Error object, which can be used to trap and handle errors.</span></span> <span data-ttu-id="78440-107">L'oggetto Error è analogo all'oggetto Err di VBScript.</span><span class="sxs-lookup"><span data-stu-id="78440-107">The Error object is analogous to the VBScript Err object.</span></span>

<span data-ttu-id="78440-108">In JScript sono disponibili diversi tipi di dati, ad esempio numeri, stringhe, valori booleani, oggetti e l'attributo null.</span><span class="sxs-lookup"><span data-stu-id="78440-108">In JScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="78440-109">VBScript utilizza un solo tipo di dati, **Variant**, che può essere sottotipo per rappresentare stringhe, numeri, valori booleani e così via.</span><span class="sxs-lookup"><span data-stu-id="78440-109">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="78440-110">In JScript, le matrici possono essere espanse in modo dinamico impostando un nuovo valore per la proprietà lunghezza della matrice.</span><span class="sxs-lookup"><span data-stu-id="78440-110">In JScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="78440-111">In VBScript non è possibile ingrandire le matrici; è necessario ridimensionarli usando l'istruzione **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="78440-111">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="78440-112">Entrambe le funzioni di supporto VBScript e JScript.</span><span class="sxs-lookup"><span data-stu-id="78440-112">Both VBScript and JScript support functions.</span></span> <span data-ttu-id="78440-113">VBScript, tuttavia, supporta anche subroutine.</span><span class="sxs-lookup"><span data-stu-id="78440-113">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="78440-114">Le subroutine sono simili alle funzioni, ma non restituiscono un valore.</span><span class="sxs-lookup"><span data-stu-id="78440-114">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="78440-115">JScript distingue tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="78440-115">JScript is case-sensitive.</span></span> <span data-ttu-id="78440-116">VBScript non è.</span><span class="sxs-lookup"><span data-stu-id="78440-116">VBScript is not.</span></span>

<span data-ttu-id="78440-117">JScript è supportato da un'ampia gamma di Web browser, tra cui Internet Explorer e Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="78440-117">JScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="78440-118">Netscape Navigator non supporta VBScript.</span><span class="sxs-lookup"><span data-stu-id="78440-118">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="78440-119">Le matrici JScript non sono matrici della variabile di tipo **SafeArray VARIANT**.</span><span class="sxs-lookup"><span data-stu-id="78440-119">JScript arrays are not arrays of the variable type **VARIANT SAFEARRAY**.</span></span> <span data-ttu-id="78440-120">Uno script JScript deve usare un oggetto VBArray per accedere alla variabile **SafeArray VARIANT**.</span><span class="sxs-lookup"><span data-stu-id="78440-120">A JScript script must use a VBArray object to access the **VARIANT SAFEARRAY** variable.</span></span> <span data-ttu-id="78440-121">Gli script VBScript possono accedere direttamente alle variabili **SafeArray VARIANT**.</span><span class="sxs-lookup"><span data-stu-id="78440-121">VBScript scripts can access **VARIANT SAFEARRAY** variables directly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78440-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="78440-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78440-123">Conversione in VBScript</span><span class="sxs-lookup"><span data-stu-id="78440-123">Translating to VBScript</span></span>](translating-to-vbscript.md)
</dt> </dl>

 

 




