---
description: È possibile che si verifichi una situazione in cui un'istanza creata come figlio di una classe padre deve modificare le classi padre e diventare l'elemento figlio di un'altra classe padre.
ms.assetid: 6d0fd456-81ab-4665-bb88-f9fb29fbbd39
ms.tgt_platform: multiple
title: Modifica dell'ereditarietà di un'istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a35de3dcc37d91b318ab60fb5a520cb4da10e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882321"
---
# <a name="changing-the-inheritance-of-an-instance"></a><span data-ttu-id="37240-103">Modifica dell'ereditarietà di un'istanza</span><span class="sxs-lookup"><span data-stu-id="37240-103">Changing the Inheritance of an Instance</span></span>

<span data-ttu-id="37240-104">È possibile che si verifichi una situazione in cui un'istanza creata come figlio di una classe padre deve modificare le classi padre e diventare l'elemento figlio di un'altra classe padre.</span><span class="sxs-lookup"><span data-stu-id="37240-104">You may find a situation where an instance that was created as a child of one parent class must change parent classes and become the child of a different parent class.</span></span> <span data-ttu-id="37240-105">Ad esempio, è possibile avere una classe derivata, **ManualService**, che descrive un servizio manuale e una classe derivata, **autoservice**, che descrive un servizio automatico.</span><span class="sxs-lookup"><span data-stu-id="37240-105">For example, you may have a derived class, **ManualService**, describing a manual service, and a derived class, **AutoService**, describing an automatic service.</span></span> <span data-ttu-id="37240-106">Entrambe le classi hanno un numero elevato di proprietà.</span><span class="sxs-lookup"><span data-stu-id="37240-106">Both classes have a large number of properties.</span></span> <span data-ttu-id="37240-107">Non tutte le proprietà sono identiche.</span><span class="sxs-lookup"><span data-stu-id="37240-107">Not all properties are identical.</span></span> <span data-ttu-id="37240-108">Per modificare un servizio da manuale a automatico, è necessario modificare anche l'istanza che rappresenta il servizio da **ManualService** a **autoservice**.</span><span class="sxs-lookup"><span data-stu-id="37240-108">To change a service from manual to automatic, you must also change the instance representing the service from **ManualService** to **AutoService**.</span></span> <span data-ttu-id="37240-109">Nella versione corrente di WMI non è possibile chiamare il metodo [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) con il parametro *Pint* che punta a un'istanza di **autoservice** e le proprietà chiave che descrivono l'istanza di **ManualService** .</span><span class="sxs-lookup"><span data-stu-id="37240-109">In the current version of WMI, you cannot call the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) method with the *pInst* parameter pointing to an instance of **AutoService** and the key properties describing the **ManualService** instance.</span></span> <span data-ttu-id="37240-110">In caso contrario, viene eliminata in modo implicito l'istanza di **ManualService** originale.</span><span class="sxs-lookup"><span data-stu-id="37240-110">If you do, you implicitly delete the original **ManualService** instance.</span></span> <span data-ttu-id="37240-111">In sostanza, dopo aver stabilito la classe di un'istanza, è possibile modificare solo la classe padre di un'istanza eliminando l'istanza e ricreando l'istanza come istanza della nuova classe padre.</span><span class="sxs-lookup"><span data-stu-id="37240-111">In essence, after you establish the class of an instance, you can only change the parent class of an instance by deleting the instance and recreating the instance as an instance of the new parent class.</span></span>

<span data-ttu-id="37240-112">Nella procedura seguente viene descritto come spostare un'istanza di da una classe a un'altra classe.</span><span class="sxs-lookup"><span data-stu-id="37240-112">The following procedure describes how to move an instance from one class to another class.</span></span>

<span data-ttu-id="37240-113">**Per spostare un'istanza da una classe a un'altra classe**</span><span class="sxs-lookup"><span data-stu-id="37240-113">**To move an instance from one class to another class**</span></span>

1.  <span data-ttu-id="37240-114">Eliminare l'istanza dalla classe originale.</span><span class="sxs-lookup"><span data-stu-id="37240-114">Delete the instance from the original class.</span></span>
2.  <span data-ttu-id="37240-115">Creare l'istanza sotto la nuova classe.</span><span class="sxs-lookup"><span data-stu-id="37240-115">Create the instance under the new class.</span></span>

    <span data-ttu-id="37240-116">WMI non consente alle applicazioni di spostare un'istanza creandola nella nuova classe e quindi aggiornarla con la chiave dell'istanza originale.</span><span class="sxs-lookup"><span data-stu-id="37240-116">WMI does not allow applications to move an instance by creating it in the new class and then updating it with the key of the original instance.</span></span>

<span data-ttu-id="37240-117">Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="37240-117">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 



