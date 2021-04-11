---
description: Le query di associazione dello schema utilizzano le stesse istruzioni utilizzate nelle query di associazione dati, ovvero gli ASSOCIATOri di e i riferimenti di.
ms.assetid: b5fc2d86-702a-42cd-82e6-f15c905ba6aa
ms.tgt_platform: multiple
title: Associazioni schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0c3b753bf4657c66a635319bab7dbe435a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233459"
---
# <a name="schema-associations"></a><span data-ttu-id="a27b3-103">Associazioni schema</span><span class="sxs-lookup"><span data-stu-id="a27b3-103">Schema Associations</span></span>

<span data-ttu-id="a27b3-104">Le query di associazione dello schema utilizzano le stesse istruzioni utilizzate nelle query di associazione dati, ovvero gli ASSOCIATOri di e i riferimenti di.</span><span class="sxs-lookup"><span data-stu-id="a27b3-104">Schema association queries use the same statements as are used in data association queries: ASSOCIATORS OF and REFERENCES OF.</span></span> <span data-ttu-id="a27b3-105">Tuttavia, con le query di associazione dati, vengono restituite le istanze della classe e con le query di associazione dello schema, vengono restituiti i nomi delle classi che possono partecipare alle relazioni di associazione.</span><span class="sxs-lookup"><span data-stu-id="a27b3-105">However, with data association queries, class instances are returned, and with schema association queries, names of classes that can participate in association relationships are returned.</span></span> <span data-ttu-id="a27b3-106">Utilizzare, ad esempio, una query di schema per individuare tutte le classi di associazione definite nello schema che fanno riferimento a una classe di origine.</span><span class="sxs-lookup"><span data-stu-id="a27b3-106">For example, use a schema query to find all of the association classes defined in the schema that reference a source class.</span></span>

<span data-ttu-id="a27b3-107">La sintassi per gli ASSOCIATOri di e i riferimenti di istruzioni è la stessa per le query di associazione dello schema, così come per le query di associazione dati, con le eccezioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a27b3-107">The syntax for the ASSOCIATORS OF and REFERENCES OF statements is the same for schema association queries as it is for data association queries with the following exceptions:</span></span>

-   <span data-ttu-id="a27b3-108">L'oggetto di origine è una classe anziché un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="a27b3-108">The source object is a class rather than an instance.</span></span>
-   <span data-ttu-id="a27b3-109">Esiste una parola chiave aggiuntiva, **SchemaOnly**, che identifica la query come applicabile a uno schema anziché ai dati.</span><span class="sxs-lookup"><span data-stu-id="a27b3-109">There is an additional keyword, **SchemaOnly**, which identifies the query as applying to a schema rather than to data.</span></span>
-   <span data-ttu-id="a27b3-110">La parola chiave **ClassDefsOnly** non è valida.</span><span class="sxs-lookup"><span data-stu-id="a27b3-110">The **ClassDefsOnly** keyword is not valid.</span></span>

<span data-ttu-id="a27b3-111">Nell'esempio seguente viene illustrata la sintassi completa degli ASSOCIATOri di statement per una query di schema.</span><span class="sxs-lookup"><span data-stu-id="a27b3-111">The following example shows the complete syntax of the ASSOCIATORS OF statement for a schema query.</span></span> <span data-ttu-id="a27b3-112">Per informazioni dettagliate sulla sintassi, vedere [associrs of Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="a27b3-112">For detailed syntax, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>


```sql
ASSOCIATORS OF {SourceClass} WHERE 
    AssocClass = AssocClassName
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
    SchemaOnly
```



<span data-ttu-id="a27b3-113">Nell'esempio seguente viene illustrata una query che restituisce le classi del **protocollo** e del **driver** , le due classi che fanno riferimento alla classe di origine.</span><span class="sxs-lookup"><span data-stu-id="a27b3-113">The following example shows a query that returns the **Protocol** and **Driver** classes, the two classes that refer to the source class.</span></span>


```sql
ASSOCIATORS OF {Adapter} WHERE SchemaOnly
```



<span data-ttu-id="a27b3-114">La query seguente restituisce solo la classe **driver** a causa della restrizione inserita dalla parola chiave **AssocClass** .</span><span class="sxs-lookup"><span data-stu-id="a27b3-114">The following query returns only the **Driver** class because of the restriction placed by the **AssocClass** keyword.</span></span>


```sql
ASSOCIATORS OF {Adapter} WHERE AssocClass = AdapterDriver SchemaOnly
```



<span data-ttu-id="a27b3-115">Di seguito è riportata la sintassi completa dei riferimenti dell'istruzione per una query di schema.</span><span class="sxs-lookup"><span data-stu-id="a27b3-115">The complete syntax of the REFERENCES OF statement for a schema query is as follows.</span></span> <span data-ttu-id="a27b3-116">Per la sintassi dettagliata, vedere [References of Statement](references-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="a27b3-116">For detailed syntax, see [REFERENCES OF Statement](references-of-statement.md).</span></span>


```sql
REFERENCES OF {SourceClass} WHERE
    ResultClass = ClassName
    Role = PropertyName
    RequiredQualifier = QualifierName
    SchemaOnly
```



> [!Note]  
> <span data-ttu-id="a27b3-117">Le query di associazione dello schema possono restituire oggetti duplicati.</span><span class="sxs-lookup"><span data-stu-id="a27b3-117">Schema association queries may return duplicate objects.</span></span>

 

<span data-ttu-id="a27b3-118">Ad esempio, la query seguente restituirà la classe [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) più volte durante l'enumerazione delle classi nello spazio dei nomi **\\ CIMV2 radice** .</span><span class="sxs-lookup"><span data-stu-id="a27b3-118">For example, the following query will return the class [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) several times when enumerating classes in the **root\\cimv2** namespace.</span></span>


```sql
ASSOCIATORS OF {Win32_ComputerSystem} WHERE SchemaOnly
```



 

 
