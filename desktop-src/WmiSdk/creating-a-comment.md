---
description: Il Managed Object Format (MOF) supporta due stili di commento usando due diversi stili di delimitatori di commento.
ms.assetid: 5ab71b45-7ed1-44c4-8710-6b833b0afb80
ms.tgt_platform: multiple
title: Creazione di un commento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 870833f1dbb86f53c7114c4e376af2b4882906ffe1b8cc10f5876bd2c80492e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097341"
---
# <a name="creating-a-comment"></a>Creazione di un commento

Il Managed Object Format (MOF) supporta due stili di commento usando due diversi stili di delimitatori di commento.

Nella tabella seguente sono elencati i delimitatori usati per i commenti e l'effetto dei delimitatori nel codice.



| Delimitatore   | Marks                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | Inizio di un commento che termina alla fine della riga.                                    |
| /\* E \*/ | Inizio e fine di un commento che può estendersi su più righe o solo su una parte di una riga. |



 

Come nei linguaggi di programmazione C e C++, è necessario usare il delimitatore // solo con commenti a riga singola, ma usare i delimitatori / e / con commenti a riga singola o a \* \* più righe.

Nell'esempio di codice seguente vengono descritti i due stili delimitatori.

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Progettazione di Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



