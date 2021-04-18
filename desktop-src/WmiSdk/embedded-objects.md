---
description: Un oggetto incorporato è un oggetto di una classe presente in una dichiarazione di classe o istanza di un'altra classe.
ms.assetid: 11a4556b-f682-4850-aedc-793602c5745b
ms.tgt_platform: multiple
title: Incorporamento di oggetti in una classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39b94296a6869dddca7fd3df08739615a4a0c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315996"
---
# <a name="embedding-objects-in-a-class"></a><span data-ttu-id="d5a2b-103">Incorporamento di oggetti in una classe</span><span class="sxs-lookup"><span data-stu-id="d5a2b-103">Embedding Objects in a Class</span></span>

<span data-ttu-id="d5a2b-104">Un oggetto incorporato è un oggetto di una classe presente in una dichiarazione di classe o istanza di un'altra classe.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-104">An embedded object is an object of a class that exists within a class or instance declaration of another class.</span></span> <span data-ttu-id="d5a2b-105">La classe [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) , ad esempio, contiene gli oggetti incorporati [**\_ trustee Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) .</span><span class="sxs-lookup"><span data-stu-id="d5a2b-105">For example, the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class contains [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) embedded objects.</span></span> <span data-ttu-id="d5a2b-106">Ognuno degli oggetti **\_ trustee Win32** contiene un oggetto [**\_ ACE Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="d5a2b-106">Each of the **Win32\_Trustee** objects contains a [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) object.</span></span> <span data-ttu-id="d5a2b-107">WMI non limita la profondità a cui una classe può disporre di oggetti incorporati.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-107">WMI does not limit the depth to which a class can have embedded objects.</span></span> <span data-ttu-id="d5a2b-108">Tuttavia, l'uso di un'altra progettazione, ad esempio la creazione di una classe di associazione, può creare uno schema più gestibile.</span><span class="sxs-lookup"><span data-stu-id="d5a2b-108">However, using another design, such as creating an association class, may make a more manageable schema.</span></span>

<span data-ttu-id="d5a2b-109">Per ulteriori informazioni sugli oggetti incorporati, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="d5a2b-109">For more information about embedded objects, see the following topics:</span></span>

-   [<span data-ttu-id="d5a2b-110">Creazione di oggetti incorporati</span><span class="sxs-lookup"><span data-stu-id="d5a2b-110">Creating Embedded Objects</span></span>](creating-embedded-objects.md)
-   [<span data-ttu-id="d5a2b-111">Esecuzione di query su oggetti incorporati</span><span class="sxs-lookup"><span data-stu-id="d5a2b-111">Querying Embedded Objects</span></span>](querying-embedded-objects.md)

## <a name="related-topics"></a><span data-ttu-id="d5a2b-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d5a2b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5a2b-113">Progettazione di classi Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="d5a2b-113">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
