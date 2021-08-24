---
description: L'azione ProcessComponents registra e annulla la registrazione dei componenti, dei relativi percorsi chiave e dei client dei componenti.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: Azione ProcessComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e866c6003052922dfc0e1fca5bd4ff8ea63d207eeb03c5ada22cf5f2d3e7b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259281"
---
# <a name="processcomponents-action"></a>Azione ProcessComponents

L'azione ProcessComponents registra e annulla la registrazione dei componenti, dei relativi percorsi chiave e dei client dei componenti. L'azione ProcessComponents esegue una query sulla colonna KeyPath della [tabella Component per](component-table.md) determinare i percorsi chiave. Questa registrazione viene usata da [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) per restituire il percorso di un componente per un client del prodotto.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

L'azione ProcessComponents deve essere eseguita dopo [l'azione InstallInitialize.](installinitialize-action.md)

## <a name="actiondata-messages"></a>Messaggi ActionData

Per ogni componente registrato.



| Campo | Descrizione dei dati dell'azione      |
|-------|---------------------------------|
| \[1\] | ProductId                       |
| \[2\] | Componentid                     |
| \[3\] | Percorso della chiave per il componente. |



 

Per ogni componente di cui viene annullata la registrazione.



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | ProductId                  |
| \[2\] | Componentid                |



 

 

 



