---
description: L'azione AllocateRegistrySpace garantisce che nel registro di sistema esista la quantità di spazio disponibile nel registro di sistema specificato dalla proprietà AVAILABLEFREEREG.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: Azione AllocateRegistrySpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6f986561595c73bf3bb1188d899af3d3d7d528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311064"
---
# <a name="allocateregistryspace-action"></a>Azione AllocateRegistrySpace

L'azione AllocateRegistrySpace garantisce che nel registro di sistema esista la quantità di spazio disponibile nel registro di sistema specificato dalla proprietà [**AVAILABLEFREEREG**](availablefreereg.md) .

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione AllocateRegistrySpace deve essere chiamata dopo [InstallInitialize](installinitialize-action.md). È consigliabile pianificare il AllocateRegistrySpace prima di tutte le altre azioni per assicurarsi che lo spazio disponibile nel registro di sistema sia sufficiente per continuare.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione     |
|-------|--------------------------------|
| \[1\] | Spazio del registro di sistema obbligatorio in KB. |



 

 

 



