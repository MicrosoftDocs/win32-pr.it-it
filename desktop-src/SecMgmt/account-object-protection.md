---
description: Viene illustrato il modo in cui gli oggetti account sono protetti.
ms.assetid: a07ef46e-f4b6-4e21-bdd7-72d03e1c88b3
title: Protezione oggetti account
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f495a3dc943ef73eef5074e0edc73247ceb02d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315364"
---
# <a name="account-object-protection"></a><span data-ttu-id="424f1-103">Protezione oggetti account</span><span class="sxs-lookup"><span data-stu-id="424f1-103">Account Object Protection</span></span>

<span data-ttu-id="424f1-104">Gli oggetti [**account**](account-object.md) sono protetti nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="424f1-104">[**Account**](account-object.md) objects are protected in the following fashion:</span></span>

-   <span data-ttu-id="424f1-105">Il **mondo** del gruppo ha un'esecuzione generica \_ .</span><span class="sxs-lookup"><span data-stu-id="424f1-105">The group **WORLD** has GENERIC\_EXECUTE.</span></span>
-   <span data-ttu-id="424f1-106">L' **\_ amministratore locale** del gruppo dispone dell'accesso DELETE, GENERIC \_ Read, Generic \_ WRITE, Generic \_ Execute e Write \_ DACL.</span><span class="sxs-lookup"><span data-stu-id="424f1-106">The group **LOCAL\_ADMIN** has DELETE, GENERIC\_READ, GENERIC\_WRITE, GENERIC\_EXECUTE, and WRITE\_DACL access.</span></span>
-   <span data-ttu-id="424f1-107">L' **\_ amministratore locale** del gruppo viene assegnato come proprietario e gruppo primario di oggetti account.</span><span class="sxs-lookup"><span data-stu-id="424f1-107">The group **LOCAL\_ADMIN** is assigned as owner and primary group of Account objects.</span></span>

 

 



