---
description: Al termine di una classe o di un'istanza di, è possibile eliminare la classe o l'istanza da WMI.
ms.assetid: 8d4bf548-a332-4058-92d0-d613bbeaa408
ms.tgt_platform: multiple
title: Eliminazione di una classe o di un'istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a46a52400623e31df3e051a0b587f49326733b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226950"
---
# <a name="deleting-a-class-or-instance"></a>Eliminazione di una classe o di un'istanza

Al termine di una classe o di un'istanza di, è possibile eliminare la classe o l'istanza da WMI. Analogamente ad altre tecnologie orientate agli oggetti, è possibile eliminare oggetti di classe o istanza per pulire lo spazio dei nomi WMI e restituire le risorse di sistema. Tuttavia, molte classi e istanze in WMI sono persistenti e vengono usate da un'ampia gamma di applicazioni in qualsiasi momento, pertanto è necessario prestare attenzione quando si elimina una classe o un'istanza WMI: l'applicazione o un'altra applicazione richiederà probabilmente la classe o l'istanza in un secondo momento.

L'eliminazione di una classe o di un'istanza è una procedura semplice. Tuttavia, a causa della natura permanente di una classe, probabilmente non sarà necessario eliminare spesso una classe. È possibile, ad esempio, eliminare la classe [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) , perché è improbabile che non si disponga di un'unità disco in un punto qualsiasi dell'azienda. In alternativa, sarà più probabile eliminare un'istanza di una classe. Per ulteriori informazioni, vedere [eliminazione di un'istanza](deleting-an-instance.md).

Sebbene non comune, è possibile che si verifichi un periodo di tempo in cui si desidera aggiornare una classe creata. Ad esempio, è possibile creare una classe per rappresentare un'applicazione di terze parti. Se il software di terze parti è stato aggiornato nella misura in cui la classe non rappresenta più correttamente il software, potrebbe essere necessario eliminare la classe originale. Per ulteriori informazioni, vedere [eliminazione di una classe](deleting-a-class.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione di classi Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
