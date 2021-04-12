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
# <a name="compiling-mof-code-with-floating-point-values"></a><span data-ttu-id="d1d51-105">Compilazione di codice MOF con valori Floating-Point</span><span class="sxs-lookup"><span data-stu-id="d1d51-105">Compiling MOF Code with Floating-Point Values</span></span>

<span data-ttu-id="d1d51-106">Il compilatore MOF accetta un valore a virgola mobile specificato per una proprietà a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="d1d51-106">The MOF compiler accepts a floating-point value specified for a nonfloating-point property.</span></span> <span data-ttu-id="d1d51-107">Il valore viene arrotondato per eccesso e archiviato come numero a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="d1d51-107">The value is rounded up or down and stored as a nonfloating-point number.</span></span> <span data-ttu-id="d1d51-108">Questa situazione può causare risultati imprevisti.</span><span class="sxs-lookup"><span data-stu-id="d1d51-108">This situation can cause some unexpected results.</span></span>

<span data-ttu-id="d1d51-109">Nell'esempio di codice MOF seguente viene definita una classe denominata **ABC** in uno spazio dei nomi denominato "test".</span><span class="sxs-lookup"><span data-stu-id="d1d51-109">The following MOF code example defines a class called **abc** in a namespace called "Test".</span></span> <span data-ttu-id="d1d51-110">Questo codice MOF viene compilato senza errori, ma non è possibile eseguire una query per il valore a virgola mobile definito per la proprietà **exampleUint16** nell'istanza creata dal codice.</span><span class="sxs-lookup"><span data-stu-id="d1d51-110">This MOF code compiles without errors, but you cannot query for the floating-point value defined for the property **exampleUint16** in the instance this code creates.</span></span>

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

<span data-ttu-id="d1d51-111">Se si esegue la query seguente, viene ricevuto un codice di errore che indica una query non valida.</span><span class="sxs-lookup"><span data-stu-id="d1d51-111">If you issue the following query, you get an error code that indicates an invalid query.</span></span>


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000.4
```



<span data-ttu-id="d1d51-112">Tuttavia, la query seguente consente di trovare l'istanza indicata.</span><span class="sxs-lookup"><span data-stu-id="d1d51-112">However, the following query finds the indicated instance.</span></span>


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000
```



## <a name="related-topics"></a><span data-ttu-id="d1d51-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d1d51-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1d51-114">Compilazione di file MOF</span><span class="sxs-lookup"><span data-stu-id="d1d51-114">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="d1d51-115">**mofcomp**</span><span class="sxs-lookup"><span data-stu-id="d1d51-115">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="d1d51-116">Comandi del preprocessore</span><span class="sxs-lookup"><span data-stu-id="d1d51-116">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



