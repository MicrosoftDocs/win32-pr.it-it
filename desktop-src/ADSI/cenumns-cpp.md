---
title: CENUMNS. CPP
description: Nel componente provider di esempio l'enumerazione di un oggetto spazio dei nomi usa i metodi di cenumns.cpp elencati nella tabella seguente.
ms.assetid: 52e23977-8df6-44a4-9a5e-a7896471c17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b86298b27fa097af6ca9607ff2c92dfcdb101a435f9fbd67c60f23467c9e71d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017918"
---
# <a name="cenumnscpp"></a>CENUMNS. CPP

Nel componente provider di esempio l'enumerazione di un oggetto spazio dei nomi usa i metodi di cenumns.cpp elencati nella tabella seguente.



| Metodo                                              | Descrizione                                                                                                                                               |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSNamespaceEnum::Create**                  | Creare un oggetto per consentire l'enumerazione di un oggetto spazio dei nomi ADS.                                                                                         |
| **CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**  | Costruttore standard.                                                                                                                                     |
| **CSampleDSNamespaceEnum::~CSampleDSNamespaceEnum** | Distruttore standard.                                                                                                                                      |
| **CSampleDSNamespaceEnum::Next**                    | Recuperare il numero specificato di elementi dall'oggetto spazio dei nomi indicato.                                                                            |
| **CSampleDSNamespaceEnum::EnumObjects**             | Gestire il recupero dei puntatori a interfaccia agli oggetti .                                                                                                  |
| **CSampleDSNamespaceEnum::FetchObjects**            | Recuperare il set di [**puntatori IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch)                                                                          |
| **CSampleDSNamespaceEnum::FetchNextObject**         | Recuperare l'oggetto successivo. Se viene trovato, creare un oggetto Active Directory generico e recuperarne il [**puntatore IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) |



 

 

 