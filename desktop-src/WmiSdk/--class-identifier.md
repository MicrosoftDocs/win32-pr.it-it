---
description: La classe identificatore noto \_ \_ fa riferimento a una pseudo-proprietà su ogni oggetto WMI che indica la classe dell'oggetto corrente.
ms.assetid: a1d0e934-c5b5-4554-9d6e-3881064419ca
ms.tgt_platform: multiple
title: Identificatore __CLASS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b4db6cacb6943619cf6468cf7f03d4a4c08278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131775"
---
# <a name="__class-identifier"></a>\_\_Identificatore di classe

La classe identificatore noto \_ \_ fa riferimento a una pseudo-proprietà su ogni oggetto WMI che indica la classe dell'oggetto corrente.

Utilizzare la \_ \_ classe in una clausola [where](where-clause.md) per filtrare gli oggetti delle classi derivate dal set di risultati. Il set di risultati della query seguente, ad esempio, contiene non solo gli oggetti la cui classe è [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), ma anche gli oggetti la cui classe è derivata da **Win32 \_ disco logico**.


```sql
SELECT * FROM Win32_LogicalDisk
```



Nell'esempio seguente, l'uso della \_ \_ classe nella clausola **where** filtra tutti gli oggetti delle classi derivate da [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) perché la relativa classe non è **Win32 \_ disco logico**.


```sql
SELECT * FROM Win32_LogicalDisk   WHERE __CLASS = "Win32_LogicalDisk"
```



Utilizzare la \_ \_ classe nei provider a cui viene richiesto di fornire istanze di una classe specifica, indipendentemente dalle sottoclassi.

 

 
