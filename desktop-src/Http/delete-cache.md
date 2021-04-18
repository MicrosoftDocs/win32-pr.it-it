---
title: delete cache
description: Scarica l'intera cache URL o Elimina le voci in base all'URL specificato.
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- Elimina HTTP cache
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f963d12812140d11923460235ef780a621ba3db5
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "106299274"
---
# <a name="delete-cache"></a><span data-ttu-id="b30a3-104">delete cache</span><span class="sxs-lookup"><span data-stu-id="b30a3-104">delete cache</span></span>

<span data-ttu-id="b30a3-105">Scarica l'intera cache URL o Elimina le voci in base all'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="b30a3-105">Flushes the entire URL cache or deletes entries according to the specified URL.</span></span>

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a><span data-ttu-id="b30a3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b30a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b30a3-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[URL = \] \* \* \* stringa*</span><span class="sxs-lookup"><span data-stu-id="b30a3-107"><span id="_url__string"></span><span id="_URL__STRING"></span>\**\[url=\]\*\*\*string*</span></span>
</dt> <dd>

<span data-ttu-id="b30a3-108">Obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b30a3-108">Required.</span></span> <span data-ttu-id="b30a3-109">Specifica l'URL completo.</span><span class="sxs-lookup"><span data-stu-id="b30a3-109">Specifies the fully qualified URL.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="b30a3-110"><span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[ricorsivo = \] {Yes \| No}**</span><span class="sxs-lookup"><span data-stu-id="b30a3-110"><span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursive=\]{yes\|no}**</span></span>
</dt> <dd>

<span data-ttu-id="b30a3-111">In caso affermativo, rimuove tutte le voci nell'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="b30a3-111">If yes, removes all entries under the specified URL.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b30a3-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="b30a3-112">Examples</span></span>

<span data-ttu-id="b30a3-113">**Elimina URL cache = https://www.contoso.com:80/myresource/ ricorsivo = Sì**</span><span class="sxs-lookup"><span data-stu-id="b30a3-113">**delete cache url=https://www.contoso.com:80/myresource/ recursive=yes**</span></span>

 

 




