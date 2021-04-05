---
description: Un'applicazione di gestione che utilizza il provider del registro di sistema può definire classi con proprietà che rappresentano i dati del registro di sistema per chiavi specifiche e quindi archivia le classi nel repository WMI.
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: Definizione delle classi per il provider del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebce4867559398722182b7b77ae02bc31c070b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968054"
---
# <a name="defining-classes-for-the-system-registry-provider"></a><span data-ttu-id="1295f-103">Definizione delle classi per il provider del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="1295f-103">Defining Classes for the System Registry Provider</span></span>

<span data-ttu-id="1295f-104">Un'applicazione di gestione che utilizza il provider del registro di sistema può definire classi con proprietà che rappresentano i dati del registro di sistema per chiavi specifiche e quindi archivia le classi nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="1295f-104">A management application using the System Registry provider can define classes with properties that represent registry data for particular keys and then stores the classes in the WMI repository.</span></span> <span data-ttu-id="1295f-105">La maggior parte dei processi per la definizione di una classe per il registro di sistema è identica alla definizione di qualsiasi altra classe.</span><span class="sxs-lookup"><span data-stu-id="1295f-105">Most of the processes for defining a class for the system registry is identical to defining any other class.</span></span> <span data-ttu-id="1295f-106">Tuttavia, il provider del registro di sistema richiede l'utilizzo di tipi di dati e qualificatori specifici.</span><span class="sxs-lookup"><span data-stu-id="1295f-106">However, the System Registry provider requires that you use specific data types and qualifiers.</span></span>

<span data-ttu-id="1295f-107">Nella procedura riportata di seguito viene descritto come definire una classe per il provider del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1295f-107">The following procedure describes how to define a class for the System Registry provider.</span></span>

<span data-ttu-id="1295f-108">**Per definire una classe per il provider del registro di sistema**</span><span class="sxs-lookup"><span data-stu-id="1295f-108">**To define a class for the System Registry provider**</span></span>

1.  <span data-ttu-id="1295f-109">Creare la classe come qualsiasi altra classe.</span><span class="sxs-lookup"><span data-stu-id="1295f-109">Create the class as you would any other class.</span></span>

    <span data-ttu-id="1295f-110">Per ulteriori informazioni, vedere [creazione di una classe](creating-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="1295f-110">For more information, see [Creating a Class](creating-a-class.md).</span></span>

2.  <span data-ttu-id="1295f-111">Eseguire il mapping dei tipi di dati del registro di sistema appropriati ai tipi WMI appropriati.</span><span class="sxs-lookup"><span data-stu-id="1295f-111">Map the appropriate registry data types to the appropriate WMI types.</span></span>

    <span data-ttu-id="1295f-112">Il provider registro di sistema esegue il mapping dei tipi di dati del registro di sistema a tipi di dati WMI specifici.</span><span class="sxs-lookup"><span data-stu-id="1295f-112">The System Registry provider maps the registry data types to specific WMI data types.</span></span> <span data-ttu-id="1295f-113">Per ulteriori informazioni, vedere [mapping di un tipo di dati del registro di sistema a un tipo di dati WMI](mapping-a-registry-data-type-to-a-wmi-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1295f-113">For more information, see [Mapping a Registry Data Type to a WMI Data Type](mapping-a-registry-data-type-to-a-wmi-data-type.md).</span></span>

3.  <span data-ttu-id="1295f-114">Utilizzare i qualificatori richiesti per definire il percorso del provider del registro di sistema e il percorso della chiave del registro di sistema appropriata.</span><span class="sxs-lookup"><span data-stu-id="1295f-114">Use the required qualifiers to define the location of the Registry provider and the location of the appropriate registry key.</span></span>

    <span data-ttu-id="1295f-115">Il provider del registro di sistema usa tre qualificatori per definire il percorso di varie classi, provider e voci del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1295f-115">The System Registry provider uses three qualifiers to define the location of various classes, providers, and registry entries.</span></span> <span data-ttu-id="1295f-116">Per ulteriori informazioni, vedere [definizione di una classe Registry con qualificatori](defining-a-registry-class-with-qualifiers.md).</span><span class="sxs-lookup"><span data-stu-id="1295f-116">For more information, see [Defining a Registry Class With Qualifiers](defining-a-registry-class-with-qualifiers.md).</span></span>

 

 



