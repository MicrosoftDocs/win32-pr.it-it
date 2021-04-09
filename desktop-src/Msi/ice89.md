---
description: ICE89 verifica che il valore nella \_ colonna padre ProgID della tabella ProgId sia una chiave esterna valida nella colonna ProgID della tabella ProgID. Ogni elemento padre ProgId deve avere un record nella tabella ProgId.
ms.assetid: 3f5c1720-d90f-4af7-9162-520b846efbb6
title: ICE89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d14ec5b17a20b9046625feb464865bd0c08419e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968233"
---
# <a name="ice89"></a><span data-ttu-id="e5a49-104">ICE89</span><span class="sxs-lookup"><span data-stu-id="e5a49-104">ICE89</span></span>

<span data-ttu-id="e5a49-105">ICE89 verifica che il valore nella \_ colonna padre ProgID della [tabella ProgId](progid-table.md) sia una chiave esterna valida nella colonna ProgId della tabella ProgID.</span><span class="sxs-lookup"><span data-stu-id="e5a49-105">ICE89 validates that the value in the Progid\_Parent column in [ProgId table](progid-table.md) is a valid foreign key into the ProgId column in ProgId table.</span></span> <span data-ttu-id="e5a49-106">Ogni elemento padre ProgId deve avere un record nella tabella ProgId.</span><span class="sxs-lookup"><span data-stu-id="e5a49-106">Every ProgId parent should have a record in the ProgId table.</span></span>

## <a name="result"></a><span data-ttu-id="e5a49-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="e5a49-107">Result</span></span>

<span data-ttu-id="e5a49-108">ICE89 invia i seguenti errori.</span><span class="sxs-lookup"><span data-stu-id="e5a49-108">ICE89 posts the following errors.</span></span>



| <span data-ttu-id="e5a49-109">Errore ICE89</span><span class="sxs-lookup"><span data-stu-id="e5a49-109">ICE89 error</span></span>                                                           | <span data-ttu-id="e5a49-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e5a49-110">Description</span></span>                                                                |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="e5a49-111">Il valore \_ padre ProgID ' \[ 1 \] ' nella tabella ProgId non è un ProgID valido.</span><span class="sxs-lookup"><span data-stu-id="e5a49-111">The ProgId\_Parent '\[1\]' in the ProgId table is not a valid ProgId.</span></span> | <span data-ttu-id="e5a49-112">È stato specificato un elemento padre ProgId che non è elencato nella tabella ProgId.</span><span class="sxs-lookup"><span data-stu-id="e5a49-112">There is a ProgId parent specified that is not listed in the ProgId table.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e5a49-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5a49-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5a49-114">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="e5a49-114">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



