---
description: L'azione UnregisterComPlus rimuove le applicazioni COM+ dal Registro di sistema.
ms.assetid: bcedc436-a048-487e-9a84-e766da57a0b3
title: Annulla registrazioneComPlus Action
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc3ed5e8e4afd853294e7f5832662e9aaf1eb122d3573e7c384115c86d994588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499851"
---
# <a name="unregistercomplus-action"></a>Annulla registrazioneComPlus Action

L'azione UnregisterComPlus rimuove le applicazioni COM+ dal Registro di sistema.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

[L'azione RegisterComPlus](registercomplus-action.md) deve seguire [l'azione InstallFiles](installfiles-action.md) e l'azione UnregisterComPlus.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                                    |
|-------|---------------------------------------------------------------|
| \[1\] | Identificatore dell'applicazione COM+ da rimuovere. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Azione RegisterComPlus](registercomplus-action.md)
</dt> <dt>

[Tabella Complus](complus-table.md)
</dt> <dt>

[Installazione di un'applicazione COM+ con il Windows di installazione](installing-a-com--application-with-the-windows-installer.md)
</dt> </dl>

 

 



