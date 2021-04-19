---
description: Gli assembly Common Language Runtime installati nel Global Assembly Cache devono disporre di file identici in tutte le occorrenze dell'assembly.
ms.assetid: 02b4ad60-d28d-44b8-955f-b367197e69c3
title: Modalità di reinstallazione degli assembly Common Language Runtime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8512e4c6e888c7d67b2ca252184fa4f748445fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311699"
---
# <a name="reinstallation-modes-of-common-language-runtime-assemblies"></a>Modalità di reinstallazione degli assembly Common Language Runtime

Gli assembly Common Language Runtime installati nel Global Assembly Cache devono disporre di file identici in tutte le occorrenze dell'assembly. Ciò significa che le modalità di reinstallazione utilizzate da [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) e [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) devono avere significati diversi per i componenti regolari e gli assembly Common Language Runtime. Le seguenti definizioni di modalità di reinstallazione si applicano agli assembly Common Language Runtime.



| Modalità di reinstallazione                  | Significato per i componenti di Microsoft .NET                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| REINSTALLMODE \_ FILEmissing      | Installare o reinstallare il componente Common Language Runtime se è mancante o incompleto.                                         |
| \_FILEOLDERVERSION REINSTALLMODE | Installare o reinstallare il componente Common Language Runtime se è mancante o incompleto.                                         |
| \_FILEEQUALVERSION REINSTALLMODE | Installare o reinstallare il componente Common Language Runtime se è mancante o incompleto.                                         |
| fileexact REINSTALLMODE \_        | Installare o reinstallare il componente Common Language Runtime se è mancante o incompleto.                                         |
| REINSTALLMODE \_ FILEverify       | Installare o reinstallare il componente Common Language Runtime se è mancante o se il componente esistente è incompleto o danneggiato. |
| REINSTALLMODE \_ FILEreplace      | Installare o reinstallare sempre il componente Common Language Runtime.                                                                 |



 

 

 



