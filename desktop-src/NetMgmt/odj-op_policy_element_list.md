---
title: OP_POLICY_ELEMENT_LIST
description: Definizione di OP_POLICY_ELEMENT_LIST IDL
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3c46e7208e6c142b9f58a7704be9bd3461c845b2
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "103734698"
---
# <a name="op_policy_element_list-structure"></a><span data-ttu-id="7b44c-103">Struttura OP_POLICY_ELEMENT_LIST</span><span class="sxs-lookup"><span data-stu-id="7b44c-103">OP_POLICY_ELEMENT_LIST structure</span></span>

<span data-ttu-id="7b44c-104">Definisce una chiave del registro di sistema radice e una matrice di elementi chiave del registro di sistema da configurare con tale chiave.</span><span class="sxs-lookup"><span data-stu-id="7b44c-104">Defines  a root registry key and an array of registry key elements to be configured under that key.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b44c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b44c-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_ELEMENT_LIST
{
    [string] wchar_t                            *pSource;
    ULONG                                       ulRootKeyId;
    ULONG                                       cElements;
    [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
} OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;
```

## <a name="members"></a><span data-ttu-id="7b44c-106">Members</span><span class="sxs-lookup"><span data-stu-id="7b44c-106">Members</span></span>

### <a name="psource"></a><span data-ttu-id="7b44c-107">pSource</span><span class="sxs-lookup"><span data-stu-id="7b44c-107">pSource</span></span>

<span data-ttu-id="7b44c-108">Contiene il percorso del file Criteri di gruppo dal quale sono stati originati gli elementi contenuti.</span><span class="sxs-lookup"><span data-stu-id="7b44c-108">Contains the path of the Group Policy file that the contained elements were sourced from.</span></span>

### <a name="ulrootkeyid"></a><span data-ttu-id="7b44c-109">ulRootKeyId</span><span class="sxs-lookup"><span data-stu-id="7b44c-109">ulRootKeyId</span></span>

<span data-ttu-id="7b44c-110">Contiene l'identificatore della chiave del registro di sistema radice. attualmente deve essere impostato su HKEY_LOCAL_MACHINE.</span><span class="sxs-lookup"><span data-stu-id="7b44c-110">Contains the identifier of the root registry key; currently must be set to HKEY_LOCAL_MACHINE.</span></span>

### <a name="celements"></a><span data-ttu-id="7b44c-111">cElements</span><span class="sxs-lookup"><span data-stu-id="7b44c-111">cElements</span></span>

<span data-ttu-id="7b44c-112">Contiene il numero di elementi in pEles.</span><span class="sxs-lookup"><span data-stu-id="7b44c-112">Contains the number of elements in pElements.</span></span>

### <a name="pelements"></a><span data-ttu-id="7b44c-113">pEle</span><span class="sxs-lookup"><span data-stu-id="7b44c-113">pElements</span></span>

<span data-ttu-id="7b44c-114">Contiene una matrice di elementi OP_POLICY_ELEMENT.</span><span class="sxs-lookup"><span data-stu-id="7b44c-114">Contains an array of OP_POLICY_ELEMENT elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b44c-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b44c-115">See also</span></span>

[<span data-ttu-id="7b44c-116">**Definizioni IDL di aggiunta al dominio offline**</span><span class="sxs-lookup"><span data-stu-id="7b44c-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="7b44c-117">**\_elemento dei criteri op \_**</span><span class="sxs-lookup"><span data-stu-id="7b44c-117">**OP\_POLICY\_ELEMENT**</span></span>](odj-op_policy_element.md)
