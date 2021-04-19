---
description: L'azione ProcessComponents registra e Annulla la registrazione dei componenti, dei percorsi chiave e dei client dei componenti.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: Azione ProcessComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aef1f71e9a50b714a12848fc9f923d1866c2e40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316254"
---
# <a name="processcomponents-action"></a>Azione ProcessComponents

L'azione ProcessComponents registra e Annulla la registrazione dei componenti, dei percorsi chiave e dei client dei componenti. L'azione ProcessComponents esegue una query sulla colonna di percorso della [tabella dei componenti](component-table.md) per determinare i percorsi della colonna. Questa registrazione viene utilizzata da [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) per restituire il percorso di un componente per un client del prodotto.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione ProcessComponents deve essere successiva all'azione [InstallInitialize](installinitialize-action.md) .

## <a name="actiondata-messages"></a>Messaggi ActionData

Per ogni componente registrato.



| Campo | Descrizione dei dati dell'azione      |
|-------|---------------------------------|
| \[1\] | ProductId                       |
| \[2\] | ComponentId                     |
| \[3\] | Percorso della chiave per il componente. |



 

Per ogni componente di cui viene annullata la registrazione.



| Campo | Descrizione dei dati dell'azione |
|-------|----------------------------|
| \[1\] | ProductId                  |
| \[2\] | ComponentId                |



 

 

 



