---
description: Il compilatore MOF accetta un valore a virgola mobile specificato per una proprietà a virgola mobile. Il valore viene arrotondato per eccesso e archiviato come numero a virgola mobile. Questa situazione può causare risultati imprevisti.
ms.assetid: 5cf7d8e1-c29d-4b9f-8557-e656c5e83370
ms.tgt_platform: multiple
title: Compilazione di codice MOF con valori Floating-Point
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734639e1038b8e9739fead694740dbf5ab5f9cc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232633"
---
# <a name="compiling-mof-code-with-floating-point-values"></a>Compilazione di codice MOF con valori Floating-Point

Il compilatore MOF accetta un valore a virgola mobile specificato per una proprietà a virgola mobile. Il valore viene arrotondato per eccesso e archiviato come numero a virgola mobile. Questa situazione può causare risultati imprevisti.

Nell'esempio di codice MOF seguente viene definita una classe denominata **ABC** in uno spazio dei nomi denominato "test". Questo codice MOF viene compilato senza errori, ma non è possibile eseguire una query per il valore a virgola mobile definito per la proprietà **exampleUint16** nell'istanza creata dal codice.

``` syntax
#pragma namespace ("\\\\.\\Root")

instance of __Namespace
{
    Name = "Test";
};

#pragma namespace ("\\\\.\\Root\\test")

Class abc
{
        [KEY] String testID ;
        Uint16 exampleUint16;
        Real64 exampleReal64;
};

Instance of abc
{ 
        TestID ="exampleID";
        exampleUint16 = 1000.4;
};
```

Se si esegue la query seguente, viene ricevuto un codice di errore che indica una query non valida.


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000.4
```



Tuttavia, la query seguente consente di trovare l'istanza indicata.


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Compilazione di file MOF](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Comandi del preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 



