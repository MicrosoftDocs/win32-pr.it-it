---
description: ICE73 verifica che il pacchetto non riutilizzi i codici dei pacchetti, i codici di aggiornamento o i codici prodotto degli esempi di Windows Installer SDK. I pacchetti non devono mai riutilizzare i codici di pacchetto, aggiornamento o prodotto di un altro prodotto.
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ac0e192f7c2ab7fb6f6236e45e0e4da70157e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308325"
---
# <a name="ice73"></a><span data-ttu-id="0cf25-104">ICE73</span><span class="sxs-lookup"><span data-stu-id="0cf25-104">ICE73</span></span>

<span data-ttu-id="0cf25-105">ICE73 verifica che il pacchetto non riutilizzi i codici dei pacchetti, i codici di aggiornamento o i codici prodotto degli esempi di Windows Installer SDK.</span><span class="sxs-lookup"><span data-stu-id="0cf25-105">ICE73 verifies that your package does not reuse package codes, upgrade codes, or product codes of the Windows Installer SDK samples.</span></span> <span data-ttu-id="0cf25-106">I pacchetti non devono mai riutilizzare i codici di pacchetto, aggiornamento o prodotto di un altro prodotto.</span><span class="sxs-lookup"><span data-stu-id="0cf25-106">Packages should never reuse the package, upgrade, or product codes of another product.</span></span>

## <a name="result"></a><span data-ttu-id="0cf25-107">Risultato</span><span class="sxs-lookup"><span data-stu-id="0cf25-107">Result</span></span>

<span data-ttu-id="0cf25-108">ICE73 genera un avviso se il pacchetto del prodotto riutilizza un pacchetto o un codice prodotto di un esempio SDK Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="0cf25-108">ICE73 outputs a warning if your product's package reuses a package or product code of a Windows Installer SDK sample.</span></span>

## <a name="example"></a><span data-ttu-id="0cf25-109">Esempio</span><span class="sxs-lookup"><span data-stu-id="0cf25-109">Example</span></span>

<span data-ttu-id="0cf25-110">ICE73 segnala gli errori seguenti per l'esempio illustrato:</span><span class="sxs-lookup"><span data-stu-id="0cf25-110">ICE73 reports the following errors for the example shown:</span></span>

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> <span data-ttu-id="0cf25-111">Gli asterischi ( \* \* \* \* ) nel GUID rappresentano l'intervallo di GUID riservati per i pacchetti Windows Installer SDK successivi.</span><span class="sxs-lookup"><span data-stu-id="0cf25-111">The asterisks (\*\*\*\*) in the GUID represent the range of GUIDs reserved for subsequent Windows Installer SDK packages.</span></span>

 

<span data-ttu-id="0cf25-112">Per correggere gli errori, generare un nuovo GUID univoco per i codici del prodotto e del pacchetto del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0cf25-112">To fix the errors, generate a new unique GUID for your package's product and package codes.</span></span> <span data-ttu-id="0cf25-113">Sarà inoltre necessario un nuovo GUID univoco per il codice di aggiornamento del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="0cf25-113">You will also need a new unique GUID for your package's upgrade code.</span></span>

<span data-ttu-id="0cf25-114">[Flusso di informazioni di riepilogo](summary-information-stream.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="0cf25-114">[Summary Information Stream](summary-information-stream.md) (partial)</span></span>



| <span data-ttu-id="0cf25-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0cf25-115">Property</span></span>       | <span data-ttu-id="0cf25-116">Valore</span><span class="sxs-lookup"><span data-stu-id="0cf25-116">Value</span></span>                                  |
|----------------|----------------------------------------|
| <span data-ttu-id="0cf25-117">\_REVNUMBER PID</span><span class="sxs-lookup"><span data-stu-id="0cf25-117">PID\_REVNUMBER</span></span> | <span data-ttu-id="0cf25-118">{000C1101-0000-0000-C000-000000000047}</span><span class="sxs-lookup"><span data-stu-id="0cf25-118">{000C1101-0000-0000-C000-000000000047}</span></span> |



 

<span data-ttu-id="0cf25-119">[Tabella delle proprietà](property-table.md) (parziale)</span><span class="sxs-lookup"><span data-stu-id="0cf25-119">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="0cf25-120">Proprietà</span><span class="sxs-lookup"><span data-stu-id="0cf25-120">Property</span></span>                           | <span data-ttu-id="0cf25-121">Valore</span><span class="sxs-lookup"><span data-stu-id="0cf25-121">Value</span></span>                                  |
|------------------------------------|----------------------------------------|
| [<span data-ttu-id="0cf25-122">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="0cf25-122">**ProductCode**</span></span>](productcode.md) | <span data-ttu-id="0cf25-123">{80F7E030-A751-11D2-A7D4-006097C99860}</span><span class="sxs-lookup"><span data-stu-id="0cf25-123">{80F7E030-A751-11D2-A7D4-006097C99860}</span></span> |
| [<span data-ttu-id="0cf25-124">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="0cf25-124">**UpgradeCode**</span></span>](upgradecode.md) | <span data-ttu-id="0cf25-125">{8FC70000-88A0-4b41-82B8-8905D4AA904C}</span><span class="sxs-lookup"><span data-stu-id="0cf25-125">{8FC70000-88A0-4b41-82B8-8905D4AA904C}</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0cf25-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0cf25-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cf25-127">Codici del pacchetto</span><span class="sxs-lookup"><span data-stu-id="0cf25-127">Package Codes</span></span>](package-codes.md)
</dt> <dt>

[<span data-ttu-id="0cf25-128">Codici prodotto</span><span class="sxs-lookup"><span data-stu-id="0cf25-128">Product Codes</span></span>](product-codes.md)
</dt> <dt>

[<span data-ttu-id="0cf25-129">**Proprietà riepilogo Numero revisione**</span><span class="sxs-lookup"><span data-stu-id="0cf25-129">**Revision Number Summary Property**</span></span>](revision-number-summary.md)
</dt> <dt>

[<span data-ttu-id="0cf25-130">**Proprietà UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="0cf25-130">**UpgradeCode Property**</span></span>](upgradecode.md)
</dt> <dt>

[<span data-ttu-id="0cf25-131">**Proprietà ProductCode**</span><span class="sxs-lookup"><span data-stu-id="0cf25-131">**ProductCode Property**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="0cf25-132">Riferimento ghiaccio</span><span class="sxs-lookup"><span data-stu-id="0cf25-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



