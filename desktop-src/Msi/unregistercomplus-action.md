---
description: L'azione UnregisterComPlus rimuove le applicazioni COM+ dal registro di sistema.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Azione UnregisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e32d39255229151757f7d6be0ada871f555f77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968670"
---
# <a name="unregistercomplus-action"></a>Azione UnregisterComPlus

L'azione UnregisterComPlus rimuove le applicazioni COM+ dal registro di sistema.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione [RegisterComPlus](registercomplus-action.md) deve seguire l'azione [InstallFiles](installfiles-action.md) e l'azione UnregisterComPlus.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Identificatore dell'applicazione COM+ da rimuovere. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azione RegisterComPlus](registercomplus-action.md)
</dt> <dt>

[Tabella ComPlus](complus-table.md)
</dt> <dt>

[Installazione di un'applicazione COM+ con la Windows Installer](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



