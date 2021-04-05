---
description: ICE99 verifica che nessun nome di proprietà immesso nella tabella di directory duplica un nome riservato per l'utilizzo pubblico o privato del Windows Installer.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d70aeaf6480e45db5b47f76434f93e49adf317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757040"
---
# <a name="ice99"></a><span data-ttu-id="f657d-103">ICE99</span><span class="sxs-lookup"><span data-stu-id="f657d-103">ICE99</span></span>

<span data-ttu-id="f657d-104">ICE99 verifica che nessun nome di proprietà immesso nella tabella di [directory](directory-table.md) duplica un nome riservato per l'utilizzo pubblico o privato del Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f657d-104">ICE99 verifies that no property name entered in the [Directory](directory-table.md) table duplicates a name reserved for the public or private use of the Windows Installer.</span></span>

## <a name="result"></a><span data-ttu-id="f657d-105">Risultato</span><span class="sxs-lookup"><span data-stu-id="f657d-105">Result</span></span>

<span data-ttu-id="f657d-106">ICE99 invia il seguente errore.</span><span class="sxs-lookup"><span data-stu-id="f657d-106">ICE99 posts the following error.</span></span>



| <span data-ttu-id="f657d-107">Errore ICE99</span><span class="sxs-lookup"><span data-stu-id="f657d-107">ICE99 error</span></span>                                                                                                      | <span data-ttu-id="f657d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f657d-108">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f657d-109">Il nome della directory: \[ 1 \] corrisponde a una delle proprietà pubbliche MSI e può causare effetti collaterali imprevisti.</span><span class="sxs-lookup"><span data-stu-id="f657d-109">The directory name: \[1\] is the same as one of the MSI Public Properties and can cause unforeseen side effects.</span></span> | <span data-ttu-id="f657d-110">Il valore nella colonna directory della tabella [directory](directory-table.md) Duplica il nome di una proprietà riservata dal Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f657d-110">The value in the Directory column of the [Directory](directory-table.md) table duplicates a property name reserved by the Windows Installer.</span></span> |



 

## <a name="example"></a><span data-ttu-id="f657d-111">Esempio</span><span class="sxs-lookup"><span data-stu-id="f657d-111">Example</span></span>

<span data-ttu-id="f657d-112">ICE99 segnala l'errore seguente per l'esempio:</span><span class="sxs-lookup"><span data-stu-id="f657d-112">ICE99 reports the following error for the example:</span></span>

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

<span data-ttu-id="f657d-113">[Directory](directory-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="f657d-113">[Directory](directory-table.md) (partial)</span></span>



| <span data-ttu-id="f657d-114">Directory</span><span class="sxs-lookup"><span data-stu-id="f657d-114">Directory</span></span>        | <span data-ttu-id="f657d-115">\_Padre directory</span><span class="sxs-lookup"><span data-stu-id="f657d-115">Directory\_Parent</span></span> | <span data-ttu-id="f657d-116">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="f657d-116">DefaultDir</span></span> |
|------------------|-------------------|------------|
| <span data-ttu-id="f657d-117">CustomActionData</span><span class="sxs-lookup"><span data-stu-id="f657d-117">CustomActionData</span></span> |                   |            |



 

<span data-ttu-id="f657d-118">Per correggere il problema, è necessario modificare il nome di CustomActionData.</span><span class="sxs-lookup"><span data-stu-id="f657d-118">To correct this warning you should change the name of CustomActionData.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f657d-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f657d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f657d-120">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="f657d-120">ICE Reference</span></span>](ice-reference.md)
</dt> <dt>

[<span data-ttu-id="f657d-121">Tabella directory</span><span class="sxs-lookup"><span data-stu-id="f657d-121">Directory Table</span></span>](directory-table.md)
</dt> <dt>

[<span data-ttu-id="f657d-122">Non supportato in Windows Installer 3,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="f657d-122">Not Supported in Windows Installer 3.0 and earlier</span></span>](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



