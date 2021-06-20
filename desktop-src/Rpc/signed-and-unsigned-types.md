---
title: Tipi con e senza segno (RPC)
description: Informazioni sui tipi firmati e non firmati in RPC. I compilatori che usano tipi predefiniti diversi possono causare errori software nell'applicazione distribuita.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c03010262c8492b6738d1e817e165e5ca8f839
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406544"
---
# <a name="signed-and-unsigned-types-rpc"></a><span data-ttu-id="ee5fe-104">Tipi con e senza segno (RPC)</span><span class="sxs-lookup"><span data-stu-id="ee5fe-104">Signed and Unsigned Types (RPC)</span></span>

<span data-ttu-id="ee5fe-105">I compilatori che usano valori predefiniti diversi per i tipi firmati e non firmati possono causare errori software nell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="ee5fe-105">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="ee5fe-106">È possibile evitare questi problemi dichiarando in modo esplicito i tipi di carattere **come signed** o **unsigned**.</span><span class="sxs-lookup"><span data-stu-id="ee5fe-106">You can avoid these problems by explicitly declaring your character types as **signed** or **unsigned**.</span></span>

<span data-ttu-id="ee5fe-107">MIDL definisce il [**tipo piccolo**](/windows/desktop/Midl/small) per assumere lo stesso segno predefinito del tipo **char** nel compilatore C di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ee5fe-107">MIDL defines the [**small**](/windows/desktop/Midl/small) type to take the same default sign as the **char** type in the target C compiler.</span></span> <span data-ttu-id="ee5fe-108">Se il compilatore presuppone che **char** sia senza segno, **anche small** verrà definito come unsigned.</span><span class="sxs-lookup"><span data-stu-id="ee5fe-108">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="ee5fe-109">Molti compilatori C consentono di modificare il valore predefinito come opzione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="ee5fe-109">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="ee5fe-110">Ad esempio, l'opzione della riga di comando **/J** del compilatore Microsoft C modifica il segno predefinito di **char** da signed a unsigned.</span><span class="sxs-lookup"><span data-stu-id="ee5fe-110">For example, the Microsoft C compiler **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="ee5fe-111">È anche possibile controllare il segno delle variabili di tipo **char** e **small** con l'opzione della riga di comando del compilatore MIDL [**/char**](/windows/desktop/Midl/-char).</span><span class="sxs-lookup"><span data-stu-id="ee5fe-111">You can also control the sign of variables of type **char** and **small** with the MIDL compiler command-line switch [**/char**](/windows/desktop/Midl/-char).</span></span> <span data-ttu-id="ee5fe-112">Questa opzione consente di specificare il segno predefinito usato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="ee5fe-112">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="ee5fe-113">Il compilatore MIDL dichiara in modo esplicito il segno di tutti i tipi **char** che non corrispondono al tipo predefinito del compilatore C nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="ee5fe-113">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 
