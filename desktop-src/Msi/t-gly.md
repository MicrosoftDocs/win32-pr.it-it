---
description: Informazioni sui Windows installer che iniziano con la lettera T, ad esempio l'elaborazione e la trasformazione delle transazioni.
ms.assetid: 06fd0284-5af9-409a-8748-c0b40e0fa317
title: T (programma Windows di installazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7148ff7ca92a55698baa8f21e28ee6c4a54d69fd498adaea29c924bc23bc9fda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626711"
---
# <a name="t-windows-installer"></a>T (programma Windows di installazione)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**elaborazione delle transazioni**
</dt> <dd>

Una o più operazioni elaborate insieme come singolo intero indivisibile denominato transazione. Tutte le operazioni costituenti devono avere esito positivo perché la transazione riesca; in caso contrario, viene eseguito il rollback di tutte le operazioni allo stato originale.

</dd> <dt>

<span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**Trasformare**
</dt> <dd>

Modello delle differenze tra due database [*del programma di installazione*](i-gly.md) che possono essere applicati per produrre modifiche simili in altri database. È ad esempio possibile usare una trasformazione di localizzazione per modificare la lingua di un'applicazione. Per altre informazioni, vedere [Unioni e trasformazioni.](merges-and-transforms.md)

</dd> <dt>

<span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**flag di condizione di errore di trasformazione**
</dt> <dd>

Set di proprietà utilizzate per contrassegnare le condizioni di errore di una [*trasformazione.*](/windows) Per altre informazioni, vedere [**MsiCreateTransformSummaryInfo.**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

</dd> <dt>

<span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**flag di convalida delle trasformazioni**
</dt> <dd>

Set di proprietà utilizzato per verificare che [*la trasformazione*](/windows) possa essere applicata al database. Per un elenco di queste proprietà, vedere [**MsiCreateTransformSummaryInfo.**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

</dd> </dl>

 

 
