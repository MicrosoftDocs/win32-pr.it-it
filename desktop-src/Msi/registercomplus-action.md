---
description: L'azione RegisterComPlus registra le applicazioni COM+.
ms.assetid: e42bb993-7079-4d5b-bb2e-c958e99e705e
title: Azione RegisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb824d67e776a99f8cd05c56f73f171f436c71d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131618"
---
# <a name="registercomplus-action"></a>Azione RegisterComPlus

L'azione RegisterComPlus registra le applicazioni COM+.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione RegisterComPlus deve seguire l'azione [InstallFiles](installfiles-action.md) e l'azione [UnregisterComPlus](unregistercomplus-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione              |
|-------|-----------------------------------------|
| \[1\] | ID applicazione dell'applicazione COM+. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella ComPlus](complus-table.md)
</dt> <dt>

[Azione UnregisterComPlus](unregistercomplus-action.md)
</dt> <dt>

[Installazione di un'applicazione COM+ con la Windows Installer](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



