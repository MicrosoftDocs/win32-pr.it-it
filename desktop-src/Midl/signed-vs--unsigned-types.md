---
title: Tipi signed e unsigned (MIDL)
description: I compilatori che utilizzano valori predefiniti diversi per i tipi firmati e non firmati possono causare errori software nell'applicazione distribuita.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- tipi di dati MIDL, signed e unsigned
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e38fbe1dc27eebae7c7933db1d699600370d960
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400070"
---
# <a name="signed-and-unsigned-types-midl"></a><span data-ttu-id="43d83-104">Tipi signed e unsigned (MIDL)</span><span class="sxs-lookup"><span data-stu-id="43d83-104">Signed and Unsigned Types (MIDL)</span></span>

<span data-ttu-id="43d83-105">I compilatori che utilizzano valori predefiniti diversi per i tipi firmati e non firmati possono causare errori software nell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="43d83-105">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="43d83-106">È possibile evitare questi problemi dichiarando in modo esplicito i tipi di carattere come con segno o senza segno.</span><span class="sxs-lookup"><span data-stu-id="43d83-106">You can avoid these problems by explicitly declaring your character types as signed or unsigned.</span></span> <span data-ttu-id="43d83-107">Si noti che i compilatori IDL DCE non riconoscono la parola chiave [**signed**](signed.md).</span><span class="sxs-lookup"><span data-stu-id="43d83-107">Note that DCE IDL compilers do not recognize the keyword [**signed**](signed.md).</span></span> <span data-ttu-id="43d83-108">Questa funzionalità non è pertanto disponibile quando si usa l'opzione del compilatore MIDL/**OSF** .</span><span class="sxs-lookup"><span data-stu-id="43d83-108">Therefore, this feature is not available when you use the MIDL compiler /**osf** switch.</span></span>

<span data-ttu-id="43d83-109">MIDL definisce il tipo [**piccolo**](small.md) per assumere lo stesso segno predefinito del tipo [**char**](char-idl.md) nel compilatore C di destinazione.</span><span class="sxs-lookup"><span data-stu-id="43d83-109">MIDL defines the [**small**](small.md) type to take the same default sign as the [**char**](char-idl.md) type in the target C compiler.</span></span> <span data-ttu-id="43d83-110">Se il compilatore presuppone che **char** sia senza segno, anche **small** verrà definito come senza segno.</span><span class="sxs-lookup"><span data-stu-id="43d83-110">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="43d83-111">Molti compilatori C consentono di modificare l'impostazione predefinita come opzione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="43d83-111">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="43d83-112">Nell'ambiente di sviluppo Microsoft Visual C++, ad esempio, l'opzione della riga di comando **/J** modifica il segno predefinito di **char** da signed a unsigned.</span><span class="sxs-lookup"><span data-stu-id="43d83-112">For example, in the Microsoft Visual C++ development environment, the **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="43d83-113">È anche possibile controllare il segno di variabili di tipo [**char**](char-idl.md) e [**small**](small.md) con l'opzione della riga di comando del compilatore MIDL [**/char**](-char.md).</span><span class="sxs-lookup"><span data-stu-id="43d83-113">You can also control the sign of variables of type [**char**](char-idl.md) and [**small**](small.md) with the MIDL compiler command-line switch [**/char**](-char.md).</span></span> <span data-ttu-id="43d83-114">Questa opzione consente di specificare il segno predefinito usato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="43d83-114">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="43d83-115">Il compilatore MIDL dichiara in modo esplicito il segno di tutti i tipi **char** che non corrispondono al tipo predefinito del compilatore C nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="43d83-115">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 




