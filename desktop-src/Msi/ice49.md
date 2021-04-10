---
description: ICE49 verifica la presenza di voci del registro di sistema predefinite che non sono di \_ tipo reg SZ.
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edc5ba319380e92fe7d1b7410673c1c688eb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883938"
---
# <a name="ice49"></a><span data-ttu-id="e2413-103">ICE49</span><span class="sxs-lookup"><span data-stu-id="e2413-103">ICE49</span></span>

<span data-ttu-id="e2413-104">ICE49 verifica la presenza di voci del registro di sistema predefinite che non sono di tipo **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="e2413-104">ICE49 checks for default registry entries that are not a **REG\_SZ** type.</span></span>

## <a name="result"></a><span data-ttu-id="e2413-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="e2413-105">Result</span></span>

<span data-ttu-id="e2413-106">ICE49 pubblica un avviso se è presente una voce del registro di sistema predefinita che non è un tipo **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="e2413-106">ICE49 posts an warning if there is a default registry entry that is not a **REG\_SZ** type.</span></span>

## <a name="example"></a><span data-ttu-id="e2413-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="e2413-107">Example</span></span>

<span data-ttu-id="e2413-108">ICE49 segnala l'avviso seguente per l'esempio illustrato.</span><span class="sxs-lookup"><span data-stu-id="e2413-108">ICE49 reports the following warning for the example shown.</span></span>

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

<span data-ttu-id="e2413-109">Il valore " \# 123" è un valore **DWORD** del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e2413-109">The value '\#123' is a **DWORD** registry value.</span></span>

<span data-ttu-id="e2413-110">[Tabella del registro di sistema](registry-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="e2413-110">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="e2413-111">Registro</span><span class="sxs-lookup"><span data-stu-id="e2413-111">Registry</span></span> | <span data-ttu-id="e2413-112">Nome</span><span class="sxs-lookup"><span data-stu-id="e2413-112">Name</span></span> | <span data-ttu-id="e2413-113">Valore</span><span class="sxs-lookup"><span data-stu-id="e2413-113">Value</span></span> |
|----------|------|-------|
| <span data-ttu-id="e2413-114">Reg1</span><span class="sxs-lookup"><span data-stu-id="e2413-114">Reg1</span></span>     |      | <span data-ttu-id="e2413-115">\#123</span><span class="sxs-lookup"><span data-stu-id="e2413-115">\#123</span></span> |



 

<span data-ttu-id="e2413-116">Per correggere il problema, modificare il valore di tipo **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="e2413-116">To fix this warning, change the value to type **REG\_SZ**.</span></span>

<span data-ttu-id="e2413-117">I componenti con non **reg \_ SZ** sono validi.</span><span class="sxs-lookup"><span data-stu-id="e2413-117">Components with non-**REG\_SZ** are valid.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2413-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e2413-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2413-119">Sintassi dell'istruzione condizionale</span><span class="sxs-lookup"><span data-stu-id="e2413-119">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> <dt>

[<span data-ttu-id="e2413-120">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="e2413-120">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



