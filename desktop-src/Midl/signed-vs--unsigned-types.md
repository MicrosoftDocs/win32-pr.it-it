---
title: Tipi con e senza segno (MIDL)
description: Informazioni sui tipi con e senza segno in MIDL. I compilatori che usano tipi predefiniti diversi possono causare errori software nell'applicazione distribuita.
ms.assetid: a4c2d811-6cf4-4c0b-af12-bf8247152984
keywords:
- tipi di dati MIDL, con segno e senza segno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a3ed3c9f7022123f162fe0240ae190cdb4c8f8
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407384"
---
# <a name="signed-and-unsigned-types-midl"></a><span data-ttu-id="71a6b-105">Tipi con e senza segno (MIDL)</span><span class="sxs-lookup"><span data-stu-id="71a6b-105">Signed and Unsigned Types (MIDL)</span></span>

<span data-ttu-id="71a6b-106">I compilatori che usano valori predefiniti diversi per i tipi con e senza segno possono causare errori software nell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="71a6b-106">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="71a6b-107">È possibile evitare questi problemi dichiarando in modo esplicito i tipi di carattere come con o senza segno.</span><span class="sxs-lookup"><span data-stu-id="71a6b-107">You can avoid these problems by explicitly declaring your character types as signed or unsigned.</span></span> <span data-ttu-id="71a6b-108">Si noti che i compilatori IDL DCE non riconoscono la parola chiave [**firmata**](signed.md).</span><span class="sxs-lookup"><span data-stu-id="71a6b-108">Note that DCE IDL compilers do not recognize the keyword [**signed**](signed.md).</span></span> <span data-ttu-id="71a6b-109">Pertanto, questa funzionalità non è disponibile quando si usa l'opzione del compilatore **MIDL/osf.**</span><span class="sxs-lookup"><span data-stu-id="71a6b-109">Therefore, this feature is not available when you use the MIDL compiler /**osf** switch.</span></span>

<span data-ttu-id="71a6b-110">MIDL definisce il [**tipo small**](small.md) in modo che accetta lo stesso segno predefinito del [**tipo char**](char-idl.md) nel compilatore C di destinazione.</span><span class="sxs-lookup"><span data-stu-id="71a6b-110">MIDL defines the [**small**](small.md) type to take the same default sign as the [**char**](char-idl.md) type in the target C compiler.</span></span> <span data-ttu-id="71a6b-111">Se il compilatore presuppone che **char** sia senza segno, **anche small** verrà definito come senza segno.</span><span class="sxs-lookup"><span data-stu-id="71a6b-111">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="71a6b-112">Molti compilatori C consentono di modificare il valore predefinito come opzione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="71a6b-112">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="71a6b-113">Nell'ambiente di sviluppo Microsoft Visual C++, ad esempio, l'opzione della riga di comando **/J** modifica il segno predefinito di **char** da signed a unsigned.</span><span class="sxs-lookup"><span data-stu-id="71a6b-113">For example, in the Microsoft Visual C++ development environment, the **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="71a6b-114">È anche possibile controllare il segno delle variabili di tipo [**char**](char-idl.md) e [**small**](small.md) con l'opzione della riga di comando del compilatore MIDL [**/char**](-char.md).</span><span class="sxs-lookup"><span data-stu-id="71a6b-114">You can also control the sign of variables of type [**char**](char-idl.md) and [**small**](small.md) with the MIDL compiler command-line switch [**/char**](-char.md).</span></span> <span data-ttu-id="71a6b-115">Questa opzione consente di specificare il segno predefinito usato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="71a6b-115">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="71a6b-116">Il compilatore MIDL dichiara in modo esplicito il segno di tutti i tipi **char** che non corrispondono al tipo predefinito del compilatore C nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="71a6b-116">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 




