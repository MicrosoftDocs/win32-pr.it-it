---
description: L'azione ResolveSource determina il percorso dell'origine e imposta la proprietà SourceDir se l'origine non è stata ancora risolta.
ms.assetid: 6d6205a0-a870-4df2-922b-befea7e28a1a
title: Azione ResolveSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713598cd4daa90764cde2155e43b61e151432d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316742"
---
# <a name="resolvesource-action"></a>Azione ResolveSource

L'azione ResolveSource determina il percorso dell'origine e imposta la proprietà [**SourceDir**](sourcedir.md) se l'origine non è stata ancora risolta.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione ResolveSource deve essere successiva all' [azione CostInitialize](costinitialize-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData

Nessun messaggio ActionData.

## <a name="remarks"></a>Commenti

Prima di usare la proprietà [**SourceDir**](sourcedir.md) in qualsiasi espressione, è necessario chiamare l'azione ResolveSource. Deve anche essere chiamato prima di tentare di recuperare il valore della proprietà **SourceDir** usando [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya). L'azione ResolveSource non deve essere eseguita se l'origine non è disponibile, come potrebbe essere quando si disinstalla l'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Resilienza di origine](source-resiliency.md)
</dt> </dl>

 

 



