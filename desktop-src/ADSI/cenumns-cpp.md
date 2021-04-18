---
title: CENUMNS. CPP
description: Nel componente provider di esempio, l'enumerazione di un oggetto spazio dei nomi utilizza i metodi, da cenumns. cpp, elencati nella tabella seguente.
ms.assetid: 52e23977-8df6-44a4-9a5e-a7896471c17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a8bc745535014a346e8042c577d14222302679
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300418"
---
# <a name="cenumnscpp"></a>CENUMNS. CPP

Nel componente provider di esempio, l'enumerazione di un oggetto spazio dei nomi utilizza i metodi, da cenumns. cpp, elencati nella tabella seguente.



| Metodo                                              | Descrizione                                                                                                                                               |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSNamespaceEnum:: create**                  | Creare un oggetto per consentire l'enumerazione di un oggetto spazio dei nomi ADS.                                                                                         |
| **CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**  | Costruttore standard.                                                                                                                                     |
| **CSampleDSNamespaceEnum:: ~ CSampleDSNamespaceEnum** | Distruttore standard.                                                                                                                                      |
| **CSampleDSNamespaceEnum:: Next**                    | Recupera il numero specificato di elementi dall'oggetto spazio dei nomi indicato.                                                                            |
| **CSampleDSNamespaceEnum:: EnumObjects**             | Gestire il recupero dei puntatori di interfaccia agli oggetti.                                                                                                  |
| **CSampleDSNamespaceEnum::FetchObjects**            | Recupera il set di puntatori [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .                                                                          |
| **CSampleDSNamespaceEnum::FetchNextObject**         | Recuperare l'oggetto successivo. Se trovato, creare un oggetto Active Directory generico e recuperare il puntatore [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . |



 

 

 