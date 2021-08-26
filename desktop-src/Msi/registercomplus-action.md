---
description: L'azione RegisterComPlus registra le applicazioni COM+.
ms.assetid: e42bb993-7079-4d5b-bb2e-c958e99e705e
title: Azione RegisterComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046d1f40293888d3a1be48a3c55fd5082b6073828c8d5cc7d34c464556986d4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082641"
---
# <a name="registercomplus-action"></a>Azione RegisterComPlus

L'azione RegisterComPlus registra le applicazioni COM+.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione RegisterComPlus deve seguire [l'azione InstallFiles](installfiles-action.md) e [l'azione UnregisterComPlus](unregistercomplus-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione              |
|-------|-----------------------------------------|
| \[1\] | ID applicazione dell'applicazione COM+. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tabella Complus](complus-table.md)
</dt> <dt>

[Azione Annulla registrazioneComPlus](unregistercomplus-action.md)
</dt> <dt>

[Installazione di un'applicazione COM+ con il Windows di installazione](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



