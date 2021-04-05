---
title: Uso dell'interfaccia IDirectoryObject
description: Quando si crea un client ADSI in C o C++ che usa l'associazione anticipata, sarà disponibile una varietà più ampia di tipi di dati ADSI da usare per il client se chiama l'interfaccia IDirectoryObject invece dell'interfaccia IADs.
ms.assetid: d2c706ed-a341-4c49-91da-70230192f055
ms.tgt_platform: multiple
keywords:
- IDirectoryObject ADSI, utilizzo
- ADSI ADSI, utilizzo di, utilizzo dell'interfaccia IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3174402a629bc02df2b1fffe07cc8fba1d73193c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707357"
---
# <a name="using-the-idirectoryobject-interface"></a><span data-ttu-id="30ad5-105">Uso dell'interfaccia IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="30ad5-105">Using the IDirectoryObject Interface</span></span>

<span data-ttu-id="30ad5-106">Quando si crea un client ADSI in C o C++ che usa l'associazione anticipata, sarà disponibile una varietà più ampia di tipi di dati ADSI da usare per il client se chiama l'interfaccia [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) invece dell'interfaccia [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) .</span><span class="sxs-lookup"><span data-stu-id="30ad5-106">When you create an ADSI client in C or C++ that uses early binding, you will have a wider variety of ADSI data types available to use for your client if it calls the [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) interface instead of the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="30ad5-107">L'interfaccia **IDirectoryObject** fornisce metodi per supportare un subset delle proprietà di manutenzione di un oggetto e per accedere ai relativi attributi.</span><span class="sxs-lookup"><span data-stu-id="30ad5-107">The **IDirectoryObject** interface provides methods to support a subset of an object's maintenance properties and to access its attributes.</span></span> <span data-ttu-id="30ad5-108">Nella figura seguente sono illustrate le relazioni tra le strutture di dati.</span><span class="sxs-lookup"><span data-stu-id="30ad5-108">The following figure shows the relationships among the data structures.</span></span>

![strutture di dati dell'interfaccia IDirectoryObject](images/ds2dso.png)

<span data-ttu-id="30ad5-110">Nella figura precedente, le [**\_ \_ informazioni sull'oggetto di ADS**](/windows/desktop/api/Iads/ns-iads-ads_object_info) della struttura definiscono le proprietà che identificano l'oggetto in base al nome distinto, al nome distinto relativo, al contenitore (DNPadre), al tipo di oggetto (ClassDN) e alla definizione dello schema (SchemaDN).</span><span class="sxs-lookup"><span data-stu-id="30ad5-110">In the preceding figure, the structure [**ADS\_OBJECT\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_object_info) defines properties that identify the object by distinguished name, relative distinguished name, by container (ParentDN), by object type (ClassDN), and by schema definition (SchemaDN).</span></span> <span data-ttu-id="30ad5-111">Il descrittore di attributi [**Ads \_ attr \_ info**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) è costituito da un nome, un tipo di dati, una matrice di valori di dati mostrati in [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)e un flag che indica al servizio directory sottostante di eseguire determinate operazioni sugli attributi descritti in dettaglio nelle [ \_ \_ \* costanti di ADS attr](adsi-constants.md).</span><span class="sxs-lookup"><span data-stu-id="30ad5-111">The attribute descriptor [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) consists of a name, data type, an array of data values shown in [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue), and a flag that directs the underlying directory service to perform certain operations on the attributes detailed in [ADS\_ATTR\_\* constants](adsi-constants.md).</span></span> <span data-ttu-id="30ad5-112">I tipi di dati per questi attributi includono i tipi di sintassi estesi ADSI, descritti in dettaglio in [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum).</span><span class="sxs-lookup"><span data-stu-id="30ad5-112">The data types for these attributes include the ADSI extended syntax types, detailed in [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum).</span></span>

 

 




