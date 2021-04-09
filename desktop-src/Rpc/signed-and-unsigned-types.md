---
title: Tipi firmati e non firmati (RPC)
description: I compilatori che utilizzano valori predefiniti diversi per i tipi firmati e non firmati possono causare errori software nell'applicazione distribuita.
ms.assetid: 0464d465-84b7-49fc-968e-5efe037966c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453d45d0a4c29a2e30449fb645e6f40338eac546
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873225"
---
# <a name="signed-and-unsigned-types-rpc"></a><span data-ttu-id="1767a-103">Tipi firmati e non firmati (RPC)</span><span class="sxs-lookup"><span data-stu-id="1767a-103">Signed and Unsigned Types (RPC)</span></span>

<span data-ttu-id="1767a-104">I compilatori che utilizzano valori predefiniti diversi per i tipi firmati e non firmati possono causare errori software nell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="1767a-104">Compilers that use different defaults for signed and unsigned types can cause software errors in your distributed application.</span></span> <span data-ttu-id="1767a-105">È possibile evitare questi problemi dichiarando in modo esplicito i tipi di **carattere come con segno o** **senza segno**.</span><span class="sxs-lookup"><span data-stu-id="1767a-105">You can avoid these problems by explicitly declaring your character types as **signed** or **unsigned**.</span></span>

<span data-ttu-id="1767a-106">MIDL definisce il tipo [**piccolo**](/windows/desktop/Midl/small) per assumere lo stesso segno predefinito del tipo **char** nel compilatore C di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1767a-106">MIDL defines the [**small**](/windows/desktop/Midl/small) type to take the same default sign as the **char** type in the target C compiler.</span></span> <span data-ttu-id="1767a-107">Se il compilatore presuppone che **char** sia senza segno, anche **small** verrà definito come senza segno.</span><span class="sxs-lookup"><span data-stu-id="1767a-107">If the compiler assumes that **char** is unsigned, **small** will also be defined as unsigned.</span></span> <span data-ttu-id="1767a-108">Molti compilatori C consentono di modificare l'impostazione predefinita come opzione della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="1767a-108">Many C compilers let you change the default as a command-line option.</span></span> <span data-ttu-id="1767a-109">Ad esempio, l'opzione della riga di comando **/J** del compilatore C Microsoft modifica il segno predefinito di **char** da signed a unsigned.</span><span class="sxs-lookup"><span data-stu-id="1767a-109">For example, the Microsoft C compiler **/J** command-line option changes the default sign of **char** from signed to unsigned.</span></span>

<span data-ttu-id="1767a-110">È anche possibile controllare il segno di variabili di tipo **char** e **small** con l'opzione della riga di comando del compilatore MIDL [**/char**](/windows/desktop/Midl/-char).</span><span class="sxs-lookup"><span data-stu-id="1767a-110">You can also control the sign of variables of type **char** and **small** with the MIDL compiler command-line switch [**/char**](/windows/desktop/Midl/-char).</span></span> <span data-ttu-id="1767a-111">Questa opzione consente di specificare il segno predefinito usato dal compilatore.</span><span class="sxs-lookup"><span data-stu-id="1767a-111">This switch allows you to specify the default sign used by your compiler.</span></span> <span data-ttu-id="1767a-112">Il compilatore MIDL dichiara in modo esplicito il segno di tutti i tipi **char** che non corrispondono al tipo predefinito del compilatore C nel file di intestazione generato.</span><span class="sxs-lookup"><span data-stu-id="1767a-112">The MIDL compiler explicitly declares the sign of all **char** types that do not match your C-compiler default type in the generated header file.</span></span>

 

 
