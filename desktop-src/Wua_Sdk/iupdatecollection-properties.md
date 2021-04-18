---
description: L'interfaccia IUpdateCollection definisce le proprietà seguenti.
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: Proprietà di IUpdateCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aae347885deccb52ac44513bd1138aa18995c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307629"
---
# <a name="iupdatecollection-properties"></a>Proprietà di IUpdateCollection

L'interfaccia [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) definisce le proprietà seguenti.



| Proprietà                                        | Descrizione                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | Ottiene un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) che può essere utilizzata per enumerare la raccolta. |
| [**Conteggio**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | Ottiene il numero di elementi nella raccolta.                                                                           |
| [**Elemento**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | Ottiene o imposta un'interfaccia [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) in una raccolta.                                                    |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | Ottiene un valore booleano che indica se la raccolta di aggiornamenti è di sola lettura.                                          |



 

 

 
