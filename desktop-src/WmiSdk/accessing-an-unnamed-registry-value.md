---
description: Accesso a un valore del registro di sistema senza nome
ms.assetid: 1095da4c-8b9f-4674-9801-f2d25c4f372b
ms.tgt_platform: multiple
title: Accesso a un valore del registro di sistema senza nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92860d240598f0353d1f4c9f41a77306942d272b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317573"
---
# <a name="accessing-an-unnamed-registry-value"></a><span data-ttu-id="1bf93-103">Accesso a un valore del registro di sistema senza nome</span><span class="sxs-lookup"><span data-stu-id="1bf93-103">Accessing an Unnamed Registry Value</span></span>

<span data-ttu-id="1bf93-104">Il valore predefinito o senza nome di una chiave del registro di sistema viene visualizzato come (impostazione predefinita) o <No Name> nell'editor del registro di sistema Regedit.</span><span class="sxs-lookup"><span data-stu-id="1bf93-104">The default, or unnamed value of a registry key is shown as (Default) or <No Name> in the Regedit registry editor.</span></span> <span data-ttu-id="1bf93-105">Per accedere a una chiave del registro di sistema senza nome, è possibile utilizzare il provider del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1bf93-105">You can use the System Registry provider to access an unnamed registry key.</span></span> <span data-ttu-id="1bf93-106">Analogamente, è anche possibile usare il provider del registro di sistema per accedere alle descrizioni bitmap, definite come valori senza nome.</span><span class="sxs-lookup"><span data-stu-id="1bf93-106">Similarly, you can also use the System Registry provider to access bitmap descriptions, which are defined as unnamed values.</span></span>

<span data-ttu-id="1bf93-107">Nella procedura riportata di seguito viene descritto come recuperare un valore del registro di sistema senza nome.</span><span class="sxs-lookup"><span data-stu-id="1bf93-107">The following procedure describes how to retrieve an unnamed registry value.</span></span>

<span data-ttu-id="1bf93-108">**Per recuperare un valore del registro di sistema senza nome**</span><span class="sxs-lookup"><span data-stu-id="1bf93-108">**To retrieve an unnamed registry value**</span></span>

1.  <span data-ttu-id="1bf93-109">Definire una proprietà e impostare il qualificatore **PropertyContext** della proprietà su una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="1bf93-109">Define a property and set the **PropertyContext** qualifier of that property to an empty string.</span></span>

    <span data-ttu-id="1bf93-110">Nell'esempio di codice seguente viene illustrato come la classe definisce le proprietà per mantenere i valori per la chiave specificata dal qualificatore **ClassContext** .</span><span class="sxs-lookup"><span data-stu-id="1bf93-110">The following code example shows how the class defines properties to hold values for the key specified by the **ClassContext** qualifier.</span></span> <span data-ttu-id="1bf93-111">Il valore predefinito viene archiviato nella proprietà **predefinita** .</span><span class="sxs-lookup"><span data-stu-id="1bf93-111">The default value is stored in the **Default** property.</span></span>

    ``` syntax
    [dynamic, 
     provider("RegProv"), 
     ClassContext("local|hkey_local_machine\\software\\"
     "microsoft\\Active Setup\\Installed Components")]

    class RegTrans{
      [key] String Transports="";
      [PropertyContext("")] String Default;
      [PropertyContext("ComponentId")] String ComponentID;
      [PropertyContext("Locale")] String Locale;
    };
    ```

    <span data-ttu-id="1bf93-112">La chiave Transports non utilizza il valore senza nome, pertanto la compilazione di questo file MOF non produce alcun valore per la proprietà **predefinita** , a meno che non venga utilizzato uno strumento di modifica del registro di sistema per modificare il valore senza nome.</span><span class="sxs-lookup"><span data-stu-id="1bf93-112">The Transports key does not use the unnamed value, so compilation of this MOF file does not produce any value for the **Default** property unless a registry editing tool is used to change the unnamed value.</span></span>

2.  <span data-ttu-id="1bf93-113">Per un file bitmap, definire una proprietà e impostare il **PropertyContext** della proprietà.</span><span class="sxs-lookup"><span data-stu-id="1bf93-113">For a bitmap file, define a property and set the **PropertyContext** of that property.</span></span>

    <span data-ttu-id="1bf93-114">Nell'esempio di codice riportato di seguito viene illustrato come definire una proprietà.</span><span class="sxs-lookup"><span data-stu-id="1bf93-114">The following code example shows how to define a property.</span></span>

    ```mof
    Local|hkey_classes_root\\.bmp
    ```

    

 

 



