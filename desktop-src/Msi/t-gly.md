---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ms.assetid: 06fd0284-5af9-409a-8748-c0b40e0fa317
title: T (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fada27e903c465f9b5e0342fca481e5161b699c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314770"
---
# <a name="t-windows-installer"></a><span data-ttu-id="53e47-103">T (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="53e47-103">T (Windows Installer)</span></span>

<span data-ttu-id="53e47-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [i](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="53e47-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="53e47-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**elaborazione delle transazioni**</span><span class="sxs-lookup"><span data-stu-id="53e47-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**transaction processing**</span></span>
</dt> <dd>

<span data-ttu-id="53e47-106">Una o più operazioni elaborate insieme come un unico intero indivisibile denominato transazione.</span><span class="sxs-lookup"><span data-stu-id="53e47-106">One or more operations processed together as a single indivisible whole called a transaction.</span></span> <span data-ttu-id="53e47-107">Per avere esito positivo, è necessario che tutte le operazioni costituenti abbiano esito positivo. in caso contrario, viene eseguito il rollback di tutte le operazioni allo stato originale.</span><span class="sxs-lookup"><span data-stu-id="53e47-107">All the constituent operations must succeed for the transaction to succeed, otherwise all the operations are rolled back to the original state.</span></span>

</dd> <dt>

<span data-ttu-id="53e47-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**trasformazione**</span><span class="sxs-lookup"><span data-stu-id="53e47-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="53e47-109">Modello delle differenze tra due [*database del programma di installazione*](i-gly.md) che possono essere applicati per produrre modifiche simili in altri database.</span><span class="sxs-lookup"><span data-stu-id="53e47-109">Template of the differences between two [*installer databases*](i-gly.md) that can be applied to produce similar changes in other databases.</span></span> <span data-ttu-id="53e47-110">È ad esempio possibile utilizzare una trasformazione di localizzazione per modificare la lingua di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="53e47-110">For example, a localization transform can be used to change the language of an application.</span></span> <span data-ttu-id="53e47-111">Per altre informazioni, vedere [unioni e trasformazioni](merges-and-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="53e47-111">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

</dd> <dt>

<span data-ttu-id="53e47-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**flag di condizione di errore di trasformazione**</span><span class="sxs-lookup"><span data-stu-id="53e47-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**transform error condition flags**</span></span>
</dt> <dd>

<span data-ttu-id="53e47-113">Set di proprietà utilizzate per contrassegnare le condizioni di errore di una [*trasformazione*](/windows).</span><span class="sxs-lookup"><span data-stu-id="53e47-113">Set of properties used to flag the error conditions of a [*transform*](/windows).</span></span> <span data-ttu-id="53e47-114">Per ulteriori informazioni, vedere [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="53e47-114">For more information, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> <dt>

<span data-ttu-id="53e47-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**trasforma flag di convalida**</span><span class="sxs-lookup"><span data-stu-id="53e47-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**transform validation flags**</span></span>
</dt> <dd>

<span data-ttu-id="53e47-116">Set di proprietà utilizzate per verificare che la [*trasformazione*](/windows) possa essere applicata al database.</span><span class="sxs-lookup"><span data-stu-id="53e47-116">Set of properties used to verify that the [*transform*](/windows) can be applied to the database.</span></span> <span data-ttu-id="53e47-117">Per un elenco di queste proprietà, vedere [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span><span class="sxs-lookup"><span data-stu-id="53e47-117">For a list of these properties, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> </dl>

 

 
