---
description: Un altro modo per creare uno spazio dei nomi consiste nell'usare il codice Managed Object Format (MOF) per creare uno spazio dei nomi di pari livello. Uno spazio dei nomi di pari livello è uno spazio dei nomi che non esiste come elemento figlio dello spazio dei nomi corrente.
ms.assetid: 1a3f8569-e725-4158-9a2b-b440b9247925
ms.tgt_platform: multiple
title: Creazione di uno spazio dei nomi di pari livello con codice MOF
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4fcbf6e16ad51ab9a0df63e3497735b07cd6afc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317565"
---
# <a name="creating-a-sibling-namespace-with-mof-code"></a><span data-ttu-id="1a401-104">Creazione di uno spazio dei nomi di pari livello con codice MOF</span><span class="sxs-lookup"><span data-stu-id="1a401-104">Creating a Sibling Namespace with MOF Code</span></span>

<span data-ttu-id="1a401-105">Un altro modo per creare uno spazio dei nomi consiste nell'usare il codice Managed Object Format (MOF) per creare uno spazio dei nomi di pari livello.</span><span class="sxs-lookup"><span data-stu-id="1a401-105">Another way of creating a namespace is to use Managed Object Format (MOF) code to create a sibling namespace.</span></span> <span data-ttu-id="1a401-106">Uno spazio dei nomi di pari livello è uno spazio dei nomi che non esiste come elemento figlio dello spazio dei nomi corrente.</span><span class="sxs-lookup"><span data-stu-id="1a401-106">A sibling namespace is a namespace that does not exist as a child of the current namespace.</span></span>

<span data-ttu-id="1a401-107">Nella procedura seguente viene descritto come creare uno spazio dei nomi di pari livello con codice MOF.</span><span class="sxs-lookup"><span data-stu-id="1a401-107">The following procedure describes how to create a sibling namespace with MOF code.</span></span>

<span data-ttu-id="1a401-108">**Per creare uno spazio dei nomi di pari livello con codice MOF**</span><span class="sxs-lookup"><span data-stu-id="1a401-108">**To create a sibling namespace with MOF code**</span></span>

1.  <span data-ttu-id="1a401-109">Inserire il comando [**\# pragma namespace**](pragma-namespace.md) nel codice MOF prima della dichiarazione dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="1a401-109">Insert the [**\#pragma namespace**](pragma-namespace.md) command into your MOF code prior to the namespace declaration.</span></span>

    <span data-ttu-id="1a401-110">Il comando [**\# pragma namespace**](pragma-namespace.md) indica a WMI dove creare le istanze dopo la direttiva.</span><span class="sxs-lookup"><span data-stu-id="1a401-110">The [**\#pragma namespace**](pragma-namespace.md) command instructs WMI where to create the instances following the directive.</span></span>

2.  <span data-ttu-id="1a401-111">Creare un'istanza della classe dello [**\_ \_ spazio dei nomi**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="1a401-111">Create an instance of the [**\_\_Namespace**](--namespace.md) class.</span></span>
3.  <span data-ttu-id="1a401-112">Compilare il codice con l'utilità [mofcomp](mofcomp.md) o l'interfaccia [**IMOFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="1a401-112">Compile your code with the [mofcomp](mofcomp.md) utility or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span>

    <span data-ttu-id="1a401-113">Per ulteriori informazioni, vedere [compilazione di file MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="1a401-113">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="1a401-114">Nell'esempio di codice MOF seguente viene descritto come creare uno spazio dei nomi come elemento di pari livello per lo \\ spazio dei nomi "root CIMv2".</span><span class="sxs-lookup"><span data-stu-id="1a401-114">The following MOF code example describes how to create a namespace as a sibling to the "Root\\CIMv2" namespace.</span></span>

``` syntax
#pragma namespace("\\\\.\\Root")

instance of __Namespace 
{
    Name = "MyNamespace";
};
```

 

 



