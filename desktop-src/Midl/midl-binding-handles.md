---
title: Handle di binding MIDL
description: Gli handle di associazione sono oggetti dati che rappresentano l'associazione tra il client e il server.
ms.assetid: 178f4838-3deb-43d4-804f-ad6404b377bd
keywords:
- tipi di dati MIDL, handle di associazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59faea2137cb037cab1e5969e53fff2c146ad31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046576"
---
# <a name="midl-binding-handles"></a><span data-ttu-id="bafc6-104">Handle di binding MIDL</span><span class="sxs-lookup"><span data-stu-id="bafc6-104">MIDL Binding Handles</span></span>

<span data-ttu-id="bafc6-105">Gli handle di associazione sono oggetti dati che rappresentano l'associazione tra il client e il server.</span><span class="sxs-lookup"><span data-stu-id="bafc6-105">Binding handles are data objects that represent the binding between the client and the server.</span></span>

<span data-ttu-id="bafc6-106">MIDL supporta il tipo di base [**handle \_ t**](handle-t.md).</span><span class="sxs-lookup"><span data-stu-id="bafc6-106">MIDL supports the base type [**handle\_t**](handle-t.md).</span></span> <span data-ttu-id="bafc6-107">Gli handle di questo tipo sono noti come "handle primitivi".</span><span class="sxs-lookup"><span data-stu-id="bafc6-107">Handles of this type are known as "primitive handles."</span></span>

<span data-ttu-id="bafc6-108">È possibile definire tipi di handle personalizzati usando l'attributo **\[ handle \]** .</span><span class="sxs-lookup"><span data-stu-id="bafc6-108">You can define your own handle types using the **\[handle\]** attribute.</span></span> <span data-ttu-id="bafc6-109">Gli handle definiti in questo modo sono noti come handle "definiti dall'utente" o "personalizzati" o "generici".</span><span class="sxs-lookup"><span data-stu-id="bafc6-109">Handles defined in this way are known as "user-defined" or "customized" or "generic" handles.</span></span>

<span data-ttu-id="bafc6-110">È anche possibile definire un handle che mantiene le informazioni sullo stato usando l'attributo dell' **\[** [**\_ handle di contesto**](context-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="bafc6-110">You can also define a handle that maintains state information using the **\[**[**context\_handle**](context-handle.md)**\]** attribute.</span></span> <span data-ttu-id="bafc6-111">Gli handle definiti in questo modo sono noti come handle "context".</span><span class="sxs-lookup"><span data-stu-id="bafc6-111">Handles defined in this way are known as "context" handles.</span></span>

<span data-ttu-id="bafc6-112">Se non sono necessarie informazioni sullo stato e non si sceglie di chiamare le librerie di runtime RPC per gestire l'handle, è possibile richiedere che le librerie di runtime forniscano l'associazione automatica.</span><span class="sxs-lookup"><span data-stu-id="bafc6-112">If no state information is needed and you do not choose to call the RPC run-time libraries to manage the handle, you can request that the run-time libraries provide automatic binding.</span></span> <span data-ttu-id="bafc6-113">Questa operazione viene eseguita tramite la parola chiave ACF **\[** [**auto \_ handle**](auto-handle.md) **\]** .</span><span class="sxs-lookup"><span data-stu-id="bafc6-113">This is done by using the ACF keyword **\[**[**auto\_handle**](auto-handle.md)**\]**.</span></span>

<span data-ttu-id="bafc6-114">È possibile specificare una variabile globale come handle di associazione usando l' **\[** [**\_ handle implicito**](implicit-handle.md)della parola chiave ACF **\]** .</span><span class="sxs-lookup"><span data-stu-id="bafc6-114">You can specify a global variable as the binding handle by using the ACF keyword **\[**[**implicit\_handle**](implicit-handle.md)**\]**.</span></span> <span data-ttu-id="bafc6-115">La parola chiave **\[ \_ handle \] esplicita** viene usata per indicare che ogni funzione remota dispone di un handle specificato in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="bafc6-115">The **\[explicit\_handle\]** keyword is used to state that each remote function has an explicitly specified handle.</span></span>

<span data-ttu-id="bafc6-116">Per ulteriori informazioni, vedere [Binding e handle](/windows/desktop/Rpc/binding-and-handles).</span><span class="sxs-lookup"><span data-stu-id="bafc6-116">For more information, see [Binding and Handles](/windows/desktop/Rpc/binding-and-handles).</span></span>

 

 