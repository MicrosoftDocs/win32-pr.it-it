---
description: L'identificatore noto CLASS fa riferimento a una pseudo-proprietà in ogni oggetto WMI che indica \_ \_ la classe dell'oggetto corrente.
ms.assetid: a1d0e934-c5b5-4554-9d6e-3881064419ca
ms.tgt_platform: multiple
title: __CLASS identificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f40d95d0476bf139aebd3cc6eefe8a34782a48bec311f2a40e1f861ec27c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110745"
---
# <a name="__class-identifier"></a>\_\_Identificatore CLASS

L'identificatore noto CLASS fa riferimento a una pseudo-proprietà in ogni oggetto WMI che indica \_ \_ la classe dell'oggetto corrente.

Usare \_ \_ CLASS in una [clausola WHERE](where-clause.md) per filtrare tutti gli oggetti delle classi derivate dal set di risultati. Ad esempio, il set di risultati della query seguente contiene non solo oggetti la cui classe è [**\_ LogicalDisk Win32,**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)ma anche oggetti la cui classe è derivata da **\_ LogicalDisk Win32.**


```sql
SELECT * FROM Win32_LogicalDisk
```



Nell'esempio seguente l'uso di CLASS nella clausola WHERE filtra tutti gli oggetti delle classi derivate da \_ \_ [**\_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)  perché la relativa classe non è **\_ LogicalDisk Win32.**


```sql
SELECT * FROM Win32_LogicalDisk   WHERE __CLASS = "Win32_LogicalDisk"
```



Usare \_ \_ CLASS nei provider a cui viene richiesto di fornire istanze di una classe specifica, indipendentemente dalle sottoclassi.

 

 
