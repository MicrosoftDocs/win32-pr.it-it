---
description: In questo argomento viene descritto come controllare la visibilità del verbo.
title: Come escludere e controllare la visibilità del verbo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f689d8b93ce9facb62b654f3f8be62f665e001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227432"
---
# <a name="how-to-suppress-and-control-verb-visibility"></a>Come escludere e controllare la visibilità del verbo

In questo argomento viene descritto come controllare la visibilità del verbo.

## <a name="instructions"></a>Istruzioni


È possibile utilizzare le impostazioni dei criteri di Windows per controllare la visibilità dei verbi. I verbi possono essere eliminati tramite le impostazioni dei criteri aggiungendo una sottochiave **SuppressionPolicy** o un valore GUID **SuppressionPolicyEx** alla sottochiave del registro di sistema del verbo. Impostare il valore della sottochiave **SuppressionPolicy** sull'ID criterio. Se il criterio è attivato, il verbo e la voce del menu di scelta rapida associato vengono eliminati. Per i possibili valori ID dei criteri, vedere l'enumerazione [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .

 

 



