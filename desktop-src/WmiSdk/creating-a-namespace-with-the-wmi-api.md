---
description: Un altro modo per creare uno spazio dei nomi consiste nell'usare l'API WMI per creare lo spazio dei nomi a livello di codice.
ms.assetid: 27a65eb0-4312-4df6-8c74-f30fe61dfec9
ms.tgt_platform: multiple
title: Creazione di uno spazio dei nomi con l'API WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53054837157df5edea90657f8b68c87b394b6d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310394"
---
# <a name="creating-a-namespace-with-the-wmi-api"></a><span data-ttu-id="73f38-103">Creazione di uno spazio dei nomi con l'API WMI</span><span class="sxs-lookup"><span data-stu-id="73f38-103">Creating a Namespace with the WMI API</span></span>

<span data-ttu-id="73f38-104">Un altro modo per creare uno spazio dei nomi consiste nell'usare l'API WMI per creare lo spazio dei nomi a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="73f38-104">Another way of creating a namespace is to use the WMI API to create the namespace programmatically.</span></span> <span data-ttu-id="73f38-105">Il vantaggio della creazione di uno spazio dei nomi a livello di codice è che è possibile creare lo spazio dei nomi dall'interno di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73f38-105">The advantage to creating a namespace programmatically is that you can create the namespace from within an application.</span></span> <span data-ttu-id="73f38-106">Tuttavia, l'utilizzo dell'API WMI è più complesso rispetto all'utilizzo del codice Managed Object Format (MOF) e non è possibile condividere facilmente gli spazi dei nomi con altri sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="73f38-106">However, using the WMI API is more complex than using Managed Object Format (MOF) code, and you cannot as easily share your namespaces with other developers.</span></span>

<span data-ttu-id="73f38-107">Nella procedura riportata di seguito viene descritto come creare uno spazio dei nomi utilizzando l'API WMI.</span><span class="sxs-lookup"><span data-stu-id="73f38-107">The following procedure describes how to create a namespace using the WMI API.</span></span>

<span data-ttu-id="73f38-108">**Per creare uno spazio dei nomi tramite l'API WMI**</span><span class="sxs-lookup"><span data-stu-id="73f38-108">**To create a namespace using the WMI API**</span></span>

1.  <span data-ttu-id="73f38-109">Usare [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) per recuperare un puntatore a un oggetto [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) che punta alla classe di sistema [**\_ \_ dello spazio dei nomi**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="73f38-109">Use [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve a pointer to an [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) object that points to the [**\_\_Namespace**](--namespace.md) system class.</span></span>
2.  <span data-ttu-id="73f38-110">Definire un'istanza della classe di sistema [**\_ \_ namespace**](--namespace.md) con una chiamata a [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).</span><span class="sxs-lookup"><span data-stu-id="73f38-110">Define an instance of the [**\_\_Namespace**](--namespace.md) system class with a call to [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance).</span></span>
3.  <span data-ttu-id="73f38-111">Impostare la proprietà **Name** dell'istanza [**\_ \_ dello spazio dei nomi**](--namespace.md) con una chiamata a [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span><span class="sxs-lookup"><span data-stu-id="73f38-111">Set the **Name** property of the [**\_\_Namespace**](--namespace.md) instance with a call to [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put).</span></span>
4.  <span data-ttu-id="73f38-112">Creare lo spazio dei nomi con una chiamata a [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).</span><span class="sxs-lookup"><span data-stu-id="73f38-112">Create the namespace with a call to [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance).</span></span>

    <span data-ttu-id="73f38-113">Il parametro *Pint* di [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) deve puntare alla nuova istanza.</span><span class="sxs-lookup"><span data-stu-id="73f38-113">The *pInst* parameter of [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) should point to the new instance.</span></span>

 

 



