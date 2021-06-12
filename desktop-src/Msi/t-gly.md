---
description: Informazioni su Windows Installer concetti che iniziano con la lettera T, ad esempio l'elaborazione e la trasformazione delle transazioni.
ms.assetid: 06fd0284-5af9-409a-8748-c0b40e0fa317
title: T (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9489455f880ba558e5a9f8584be19718823035
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011264"
---
# <a name="t-windows-installer"></a><span data-ttu-id="4b1f6-103">T (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="4b1f6-103">T (Windows Installer)</span></span>

<span data-ttu-id="4b1f6-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span><span class="sxs-lookup"><span data-stu-id="4b1f6-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="4b1f6-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**elaborazione delle transazioni**</span><span class="sxs-lookup"><span data-stu-id="4b1f6-105"><span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**transaction processing**</span></span>
</dt> <dd>

<span data-ttu-id="4b1f6-106">Una o più operazioni elaborate insieme come singolo intero indivisibile denominato transazione.</span><span class="sxs-lookup"><span data-stu-id="4b1f6-106">One or more operations processed together as a single indivisible whole called a transaction.</span></span> <span data-ttu-id="4b1f6-107">Tutte le operazioni costituenti devono avere esito positivo perché la transazione riesca; in caso contrario, viene eseguito il rollback di tutte le operazioni allo stato originale.</span><span class="sxs-lookup"><span data-stu-id="4b1f6-107">All the constituent operations must succeed for the transaction to succeed, otherwise all the operations are rolled back to the original state.</span></span>

</dd> <dt>

<span data-ttu-id="4b1f6-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**Trasformare**</span><span class="sxs-lookup"><span data-stu-id="4b1f6-108"><span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**transform**</span></span>
</dt> <dd>

<span data-ttu-id="4b1f6-109">Modello delle differenze tra due database [*del programma di installazione*](i-gly.md) che possono essere applicati per produrre modifiche simili in altri database.</span><span class="sxs-lookup"><span data-stu-id="4b1f6-109">Template of the differences between two [*installer databases*](i-gly.md) that can be applied to produce similar changes in other databases.</span></span> <span data-ttu-id="4b1f6-110">È ad esempio possibile usare una trasformazione di localizzazione per modificare la lingua di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4b1f6-110">For example, a localization transform can be used to change the language of an application.</span></span> <span data-ttu-id="4b1f6-111">Per altre informazioni, vedere [Unioni e trasformazioni.](merges-and-transforms.md)</span><span class="sxs-lookup"><span data-stu-id="4b1f6-111">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

</dd> <dt>

<span data-ttu-id="4b1f6-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**flag di condizione di errore di trasformazione**</span><span class="sxs-lookup"><span data-stu-id="4b1f6-112"><span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**transform error condition flags**</span></span>
</dt> <dd>

<span data-ttu-id="4b1f6-113">Set di proprietà utilizzate per contrassegnare le condizioni di errore di una [*trasformazione.*](/windows)</span><span class="sxs-lookup"><span data-stu-id="4b1f6-113">Set of properties used to flag the error conditions of a [*transform*](/windows).</span></span> <span data-ttu-id="4b1f6-114">Per altre informazioni, vedere [**MsiCreateTransformSummaryInfo.**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)</span><span class="sxs-lookup"><span data-stu-id="4b1f6-114">For more information, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> <dt>

<span data-ttu-id="4b1f6-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**flag di convalida delle trasformazioni**</span><span class="sxs-lookup"><span data-stu-id="4b1f6-115"><span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**transform validation flags**</span></span>
</dt> <dd>

<span data-ttu-id="4b1f6-116">Set di proprietà utilizzate per verificare che [*la trasformazione*](/windows) possa essere applicata al database.</span><span class="sxs-lookup"><span data-stu-id="4b1f6-116">Set of properties used to verify that the [*transform*](/windows) can be applied to the database.</span></span> <span data-ttu-id="4b1f6-117">Per un elenco di queste proprietà, vedere [**MsiCreateTransformSummaryInfo.**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)</span><span class="sxs-lookup"><span data-stu-id="4b1f6-117">For a list of these properties, see [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa).</span></span>

</dd> </dl>

 

 
