---
description: In WMI, una classe è un oggetto che descrive alcuni aspetti di un'azienda, ad esempio un tipo speciale di unità disco.
ms.assetid: 06b75910-f126-48b6-8e43-4a9ed4661732
ms.tgt_platform: multiple
title: Creazione di una classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2274252715ce44b9d2b79e398c945ca723fe3f7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317571"
---
# <a name="creating-a-wmi-class"></a><span data-ttu-id="7cb60-103">Creazione di una classe WMI</span><span class="sxs-lookup"><span data-stu-id="7cb60-103">Creating a WMI Class</span></span>

<span data-ttu-id="7cb60-104">In WMI, una classe è un oggetto che descrive alcuni aspetti di un'azienda, ad esempio un tipo speciale di unità disco.</span><span class="sxs-lookup"><span data-stu-id="7cb60-104">In WMI, a class is an object that describes some aspect of an enterprise, such as a special type of disk drive.</span></span> <span data-ttu-id="7cb60-105">Dopo aver creato una definizione di classe, scrivere la DLL del provider per fornire le istanze della classe, i dati della proprietà e i metodi Execute definiti per la classe.</span><span class="sxs-lookup"><span data-stu-id="7cb60-105">After you have created a class definition, write your provider DLL to supply instances of the class, property data, and execute methods defined for the class.</span></span> <span data-ttu-id="7cb60-106">Gli script e le applicazioni possono quindi ottenere i dati o controllare il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7cb60-106">Scripts and applications can then obtain data or control the device.</span></span> <span data-ttu-id="7cb60-107">Per ulteriori informazioni, vedere [sviluppo di un provider WMI](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7cb60-107">For more information, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="7cb60-108">Per assicurarsi che tutte le definizioni di classe WMI per gli oggetti gestiti vengano ripristinate nel [*repository WMI*](gloss-w.md) in caso di errore e riavvio di WMI, utilizzare l'istruzione per il preprocessore dell'istruzione [**\# pragma autocover**](pragma-autorecover.md) nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="7cb60-108">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) statement preprocessor instruction in your MOF file.</span></span>

 

## <a name="base-class"></a><span data-ttu-id="7cb60-109">Classe di base</span><span class="sxs-lookup"><span data-stu-id="7cb60-109">Base Class</span></span>

<span data-ttu-id="7cb60-110">Una classe di base rappresenta un concetto generale.</span><span class="sxs-lookup"><span data-stu-id="7cb60-110">A base class represents some general concept.</span></span> <span data-ttu-id="7cb60-111">Ad esempio, la classe [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) rappresenta tutti i tipi di unità CD-ROM in WMI e contiene le proprietà generali che descrivono tutti i tipi di unità CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="7cb60-111">For example, the [**CIM\_CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) class represents all types of CD-ROM drives in WMI, and contains general properties that describe all kinds of CD-ROM drives.</span></span> <span data-ttu-id="7cb60-112">Per ulteriori informazioni, vedere [creazione di una classe di base](creating-a-base-class.md).</span><span class="sxs-lookup"><span data-stu-id="7cb60-112">For more information, see [Creating a Base Class](creating-a-base-class.md).</span></span>

<span data-ttu-id="7cb60-113">Una classe derivata eredita proprietà e metodi da un'altra classe.</span><span class="sxs-lookup"><span data-stu-id="7cb60-113">A derived class inherits properties and methods from another class.</span></span> <span data-ttu-id="7cb60-114">Una classe derivata rappresenta in genere un caso specifico di una classe base.</span><span class="sxs-lookup"><span data-stu-id="7cb60-114">A derived class usually represents a specific case of a base class.</span></span> <span data-ttu-id="7cb60-115">Ad esempio, la classe [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) rappresenta un'unità CD-ROM in un sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="7cb60-115">For example, the [**Win32\_CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) class represents a CD-ROM drive on a Windows system.</span></span> <span data-ttu-id="7cb60-116">La classe **Win32 \_ CDROMDrive** è basata su e eredita molte proprietà da [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive).</span><span class="sxs-lookup"><span data-stu-id="7cb60-116">The **Win32\_CDROMDrive** class is based on and inherits many of properties from [**CIM\_CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive).</span></span> <span data-ttu-id="7cb60-117">Tuttavia, **\_ CDROMDrive Win32**, come altre classi derivate, possono avere proprietà aggiuntive che rendono univoca la classe derivata.</span><span class="sxs-lookup"><span data-stu-id="7cb60-117">However, **Win32\_CDROMDrive**, like other derived classes, can have additional properties that make the derived class unique.</span></span> <span data-ttu-id="7cb60-118">Per ulteriori informazioni, vedere [creazione di una classe derivata](creating-a-derived-class.md).</span><span class="sxs-lookup"><span data-stu-id="7cb60-118">For more information, see [Creating a Derived Class](creating-a-derived-class.md).</span></span>

## <a name="properties-and-methods"></a><span data-ttu-id="7cb60-119">Proprietà e metodi</span><span class="sxs-lookup"><span data-stu-id="7cb60-119">Properties and Methods</span></span>

<span data-ttu-id="7cb60-120">La creazione di una classe significa definire le proprietà che descrivono tale classe.</span><span class="sxs-lookup"><span data-stu-id="7cb60-120">Creating a class means defining the properties that describe that class.</span></span> <span data-ttu-id="7cb60-121">È anche possibile definire metodi che modificano l'oggetto rappresentato dalla classe.</span><span class="sxs-lookup"><span data-stu-id="7cb60-121">You can also define methods that manipulate the object represented by the class.</span></span>

<span data-ttu-id="7cb60-122">In genere, una proprietà rappresenta un aspetto dell'oggetto, ad esempio un numero di serie per un dispositivo o una dimensione in byte per un processo, mentre un metodo rappresenta un'azione che modifica lo stato o il comportamento del dispositivo o dell'entità logica.</span><span class="sxs-lookup"><span data-stu-id="7cb60-122">Generally, a property represents an aspect of the object, such as a serial number for a device or a size in bytes for a process, while a method represents an action that changes the state or behavior of the device or logical entity.</span></span>

<span data-ttu-id="7cb60-123">Ogni classe deve avere almeno una proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="7cb60-123">Each class must have at least one key property.</span></span> <span data-ttu-id="7cb60-124">Mentre una classe può avere più chiavi, non è possibile creare un'istanza di una classe con più di 256 di chiavi.</span><span class="sxs-lookup"><span data-stu-id="7cb60-124">While a class may have multiple keys, you cannot create an instance of a class with more than 256 keys.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cb60-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7cb60-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cb60-126">Progettazione di classi Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="7cb60-126">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
