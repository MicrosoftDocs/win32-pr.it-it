---
description: Per le query sui dati dello schema viene utilizzata l'istruzione SELECT con una sintassi simile a quella per le query di dati.
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: Istruzione SELECT per le query dello schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f9f3f9ae8cc11a94d4d868e36af56ee7dffd2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233458"
---
# <a name="select-statement-for-schema-queries"></a><span data-ttu-id="f3b6e-103">Istruzione SELECT per le query dello schema</span><span class="sxs-lookup"><span data-stu-id="f3b6e-103">SELECT Statement for Schema Queries</span></span>

<span data-ttu-id="f3b6e-104">Per le query sui dati dello schema viene utilizzata l'istruzione SELECT con una sintassi simile a quella per le [query di dati](select-statement-for-data-queries.md).</span><span class="sxs-lookup"><span data-stu-id="f3b6e-104">Schema data queries use the SELECT statement with a syntax similar to that for [data queries](select-statement-for-data-queries.md).</span></span> <span data-ttu-id="f3b6e-105">La differenza consiste nell'utilizzo di una classe speciale denominata "meta \_ Class", che identifica la query come query dello schema.</span><span class="sxs-lookup"><span data-stu-id="f3b6e-105">The difference is the use of a special class called "meta\_class", which identifies the query as a schema query.</span></span>

<span data-ttu-id="f3b6e-106">Nell'esempio seguente vengono richieste tutte le definizioni di classe nello spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="f3b6e-106">The following example requests all class definitions that are within the current namespace.</span></span>


```sql
SELECT * FROM meta_class
```



<span data-ttu-id="f3b6e-107">Le query di schema supportano solo " \* ".</span><span class="sxs-lookup"><span data-stu-id="f3b6e-107">Schema queries only support "\*".</span></span> <span data-ttu-id="f3b6e-108">Per restringere l'ambito delle definizioni restituite, un provider può aggiungere una clausola WHERE che specifica una determinata classe.</span><span class="sxs-lookup"><span data-stu-id="f3b6e-108">To narrow the scope of the definitions returned, a provider can add a WHERE clause that specifies a particular class.</span></span>

<span data-ttu-id="f3b6e-109">Nell'esempio seguente viene illustrato come aggiungere una clausola WHERE per specificare una classe specifica.</span><span class="sxs-lookup"><span data-stu-id="f3b6e-109">The following example shows how to add a WHERE clause to specify a particular class.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



<span data-ttu-id="f3b6e-110">La speciale **\_ \_ proprietà denominata identifica la classe** di destinazione per una query di schema.</span><span class="sxs-lookup"><span data-stu-id="f3b6e-110">The special property called **\_\_this** identifies the target class for a schema query.</span></span> <span data-ttu-id="f3b6e-111">Si noti che è necessario usare l'operatore ISA con **\_ \_ questa** proprietà per richiedere definizioni per le sottoclassi della classe di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f3b6e-111">Note that the ISA operator must be used with the **\_\_this** property to request definitions for the subclasses of the target class.</span></span> <span data-ttu-id="f3b6e-112">La query precedente restituisce la definizione per la classe [**Win32 \_ disco logico**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) e le definizioni per tutte le relative sottoclassi.</span><span class="sxs-lookup"><span data-stu-id="f3b6e-112">The preceding query returns the definition for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and definitions for all of its subclasses.</span></span>

<span data-ttu-id="f3b6e-113">Nell'esempio seguente viene illustrato come richiedere una definizione di classe per una singola classe utilizzando la proprietà di sistema della **\_ \_ classe** .</span><span class="sxs-lookup"><span data-stu-id="f3b6e-113">The following example shows how to request a class definition for a single class by using the **\_\_Class** system property.</span></span>


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



<span data-ttu-id="f3b6e-114">Questa query equivale a chiamare il metodo [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) con il parametro del percorso dell'oggetto impostato su "Win32 \_ disco logico".</span><span class="sxs-lookup"><span data-stu-id="f3b6e-114">This query is equivalent to calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or the [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) method with the object path parameter set to "Win32\_LogicalDisk".</span></span>

<span data-ttu-id="f3b6e-115">Nell'esempio di codice VBScript seguente vengono recuperate tutte le classi figlio di una classe WMI di primo livello.</span><span class="sxs-lookup"><span data-stu-id="f3b6e-115">The following VBScript code sample retrieves all child classes of a top level WMI class.</span></span> <span data-ttu-id="f3b6e-116">La \_ \_ proprietà di sistema WMI Dynasty include il nome della classe di primo livello da cui viene derivata una classe, che è possibile usare per recuperare tutte le classi in uno spazio dei nomi derivato da una classe di primo livello, inclusa quella classe.</span><span class="sxs-lookup"><span data-stu-id="f3b6e-116">The \_\_Dynasty WMI system property holds the name of the top-level class from which a class is derived, which you can use to retrieve all classes in a namespace derived from a top level class, including that class.</span></span>


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Dynasty = 'Win32_CurrentTime'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



<span data-ttu-id="f3b6e-117">Il codice VBScript seguente recupera le classi figlio immediate per una classe WMI.</span><span class="sxs-lookup"><span data-stu-id="f3b6e-117">The following VBScript retrieves an immediate child classes for a WMI class.</span></span>


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Superclass = 'Cim_DataFile'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



<span data-ttu-id="f3b6e-118">Il codice VBScript seguente recupera le classi di primo livello.</span><span class="sxs-lookup"><span data-stu-id="f3b6e-118">The following VBScript retrieves top level classes.</span></span> <span data-ttu-id="f3b6e-119">Per tutte le classi di primo livello in uno spazio dei nomi WMI, la \_ \_ proprietà di sistema superclass è null.</span><span class="sxs-lookup"><span data-stu-id="f3b6e-119">For all the top level classes in a WMI namespace, the \_\_Superclass system property is Null.</span></span> <span data-ttu-id="f3b6e-120">Pertanto, è possibile recuperare le classi di primo livello cercando una superclasse null.</span><span class="sxs-lookup"><span data-stu-id="f3b6e-120">Therefore, it is possible to retrieve the top level classes by searching for a Null superclass.</span></span>


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
