---
title: Conversione in JScript da VBScript
description: Conversione in JScript da VBScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18c2ccb11ffa4f5f000d8cfc73f7db6f857cf6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708032"
---
# <a name="translating-to-jscript-from-vbscript"></a><span data-ttu-id="e82c0-103">Conversione in JScript da VBScript</span><span class="sxs-lookup"><span data-stu-id="e82c0-103">Translating to JScript from VBScript</span></span>

<span data-ttu-id="e82c0-104">In VBScript, **per**... **Ogni** ciclo enumera i membri di una raccolta. in JScript, **per**... **in** loop enumera i membri di un oggetto o di una matrice JScript.</span><span class="sxs-lookup"><span data-stu-id="e82c0-104">In VBScript, the **For**...**Each** loop enumerates the members of a collection; in JScript, the **for**...**in** loop enumerates the members of a JScript object or array.</span></span> <span data-ttu-id="e82c0-105">Per enumerare una raccolta in JScript, utilizzare un oggetto enumeratore.</span><span class="sxs-lookup"><span data-stu-id="e82c0-105">To enumerate a collection in JScript, use an Enumerator object.</span></span>

<span data-ttu-id="e82c0-106">In JScript sono disponibili diversi tipi di dati, ad esempio numeri, stringhe, valori booleani, oggetti e l'attributo null.</span><span class="sxs-lookup"><span data-stu-id="e82c0-106">In JScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="e82c0-107">VBScript utilizza un solo tipo di dati, **Variant**, che può essere sottotipo per rappresentare stringhe, numeri, valori booleani e così via.</span><span class="sxs-lookup"><span data-stu-id="e82c0-107">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="e82c0-108">In JScript, le matrici possono essere espanse in modo dinamico impostando un nuovo valore per la proprietà lunghezza della matrice.</span><span class="sxs-lookup"><span data-stu-id="e82c0-108">In JScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="e82c0-109">In VBScript non è possibile ingrandire le matrici; è necessario ridimensionarli usando l'istruzione **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="e82c0-109">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="e82c0-110">Entrambe le funzioni di supporto VBScript e JScript.</span><span class="sxs-lookup"><span data-stu-id="e82c0-110">Both VBScript and JScript support functions.</span></span> <span data-ttu-id="e82c0-111">VBScript, tuttavia, supporta anche subroutine.</span><span class="sxs-lookup"><span data-stu-id="e82c0-111">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="e82c0-112">Le subroutine sono simili alle funzioni, ma non restituiscono un valore.</span><span class="sxs-lookup"><span data-stu-id="e82c0-112">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="e82c0-113">JScript distingue tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e82c0-113">JScript is case-sensitive.</span></span> <span data-ttu-id="e82c0-114">VBScript non è.</span><span class="sxs-lookup"><span data-stu-id="e82c0-114">VBScript is not.</span></span>

<span data-ttu-id="e82c0-115">JScript è supportato sia da Internet Explorer che dal navigatore Netscape.</span><span class="sxs-lookup"><span data-stu-id="e82c0-115">JScript is supported by both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="e82c0-116">Netscape Navigator non supporta VBScript.</span><span class="sxs-lookup"><span data-stu-id="e82c0-116">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="e82c0-117">JScript fornisce l'oggetto Error, che può essere usato per intercettare e gestire gli errori.</span><span class="sxs-lookup"><span data-stu-id="e82c0-117">JScript provides the Error object, which can be used to trap and handle errors.</span></span> <span data-ttu-id="e82c0-118">L'oggetto Error è analogo all'oggetto Err di VBScript.</span><span class="sxs-lookup"><span data-stu-id="e82c0-118">The Error object is analogous to the VBScript Err object.</span></span>

<span data-ttu-id="e82c0-119">Le matrici JScript non sono matrici della variabile di tipo **SafeArray VARIANT**.</span><span class="sxs-lookup"><span data-stu-id="e82c0-119">JScript arrays are not arrays of the variable type **VARIANT SAFEARRAY**.</span></span> <span data-ttu-id="e82c0-120">Se lo script riceve una variabile **SafeArray VARIANT** da un oggetto com o da uno script VBScript, deve usare un oggetto VBArray per accedere alla variabile **SafeArray VARIANT** .</span><span class="sxs-lookup"><span data-stu-id="e82c0-120">If your script receives a **VARIANT SAFEARRAY** variable from a COM object or VBScript script, it must use a VBArray object to access the **VARIANT SAFEARRAY** variable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e82c0-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e82c0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e82c0-122">Conversione in JScript</span><span class="sxs-lookup"><span data-stu-id="e82c0-122">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




