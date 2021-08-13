---
description: L'azione AllocateRegistrySpace garantisce che la quantità di spazio disponibile nel Registro di sistema specificata dalla proprietà AVAILABLEFREEREG esista nel Registro di sistema.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: Azione AllocateRegistrySpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e47a0a0ebc3edec4605cbfac45443e4d30ee25df82ad3eaeb9da9ec9d3a94b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639578"
---
# <a name="allocateregistryspace-action"></a>Azione AllocateRegistrySpace

L'azione AllocateRegistrySpace garantisce che la quantità di spazio disponibile nel Registro di sistema specificata dalla proprietà [**AVAILABLEFREEREG**](availablefreereg.md) esista nel Registro di sistema.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

L'azione AllocateRegistrySpace deve essere chiamata dopo [InstallInitialize.](installinitialize-action.md) È consigliabile pianificare AllocateRegistrySpace prima di tutte le altre azioni per assicurarsi che lo spazio del Registro di sistema disponibile sia sufficiente per continuare.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione     |
|-------|--------------------------------|
| \[1\] | Spazio del Registro di sistema necessario in KB. |



 

 

 



