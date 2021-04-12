---
description: Questo argomento descrive cosa è necessario fare per iniziare a creare programmi che usano l'API del sensore.
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: Requisiti generali per lo sviluppo di applicazioni (API dei sensori)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ec328f659bb51eddf93cc69beb2fe6236113ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347646"
---
# <a name="general-requirements-for-application-development-sensor-api"></a><span data-ttu-id="5888e-103">Requisiti generali per lo sviluppo di applicazioni (API dei sensori)</span><span class="sxs-lookup"><span data-stu-id="5888e-103">General Requirements for Application Development (Sensor API)</span></span>

<span data-ttu-id="5888e-104">Questo argomento descrive cosa è necessario fare per iniziare a creare programmi che usano l'API del sensore.</span><span class="sxs-lookup"><span data-stu-id="5888e-104">This topic describes what you must do to start to create programs that use the Sensor API.</span></span>

<span data-ttu-id="5888e-105">Per creare un'applicazione API per i sensori, è necessario installare Windows 7 e il Software Development Kit (SDK) di Windows 7 nel computer.</span><span class="sxs-lookup"><span data-stu-id="5888e-105">To create a Sensor API application, you must install Windows 7 and the Windows 7 Software Development Kit (SDK) on your computer.</span></span> <span data-ttu-id="5888e-106">Nella tabella seguente vengono descritti i file specifici necessari.</span><span class="sxs-lookup"><span data-stu-id="5888e-106">The following table describes the specific files that you will need.</span></span>



| <span data-ttu-id="5888e-107">Nome file</span><span class="sxs-lookup"><span data-stu-id="5888e-107">File name</span></span>               | <span data-ttu-id="5888e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5888e-108">Description</span></span>                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5888e-109">Sensorsapi. h</span><span class="sxs-lookup"><span data-stu-id="5888e-109">Sensorsapi.h</span></span>            | <span data-ttu-id="5888e-110">Il file di intestazione principale per l'API del sensore.</span><span class="sxs-lookup"><span data-stu-id="5888e-110">The main header file for the Sensor API.</span></span> <span data-ttu-id="5888e-111">Questo file di intestazione contiene le definizioni dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="5888e-111">This header file contains the interface definitions.</span></span>               |
| <span data-ttu-id="5888e-112">Sensori. h</span><span class="sxs-lookup"><span data-stu-id="5888e-112">Sensors.h</span></span>               | <span data-ttu-id="5888e-113">Il file di intestazione che contiene le definizioni delle costanti definite dalla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="5888e-113">The header file that contains definitions of platform-defined constants.</span></span>                                    |
| <span data-ttu-id="5888e-114">Initguid. h</span><span class="sxs-lookup"><span data-stu-id="5888e-114">Initguid.h</span></span>              | <span data-ttu-id="5888e-115">Il file di intestazione che contiene le definizioni per il controllo dell'inizializzazione del **GUID** .</span><span class="sxs-lookup"><span data-stu-id="5888e-115">The header file that contains definitions for controlling **GUID** initialization.</span></span>                          |
| <span data-ttu-id="5888e-116">FunctionDiscoveryKeys. h</span><span class="sxs-lookup"><span data-stu-id="5888e-116">FunctionDiscoveryKeys.h</span></span> | <span data-ttu-id="5888e-117">Il file di intestazione che definisce le chiavi della proprietà ID dispositivo necessarie quando ci si connette ai sensori logici.</span><span class="sxs-lookup"><span data-stu-id="5888e-117">The header file that defines device ID property keys that are required when you connect to logical sensors.</span></span> |
| <span data-ttu-id="5888e-118">Sensorsapi. lib</span><span class="sxs-lookup"><span data-stu-id="5888e-118">Sensorsapi.lib</span></span>          | <span data-ttu-id="5888e-119">Libreria statica che contiene le definizioni **GUID** per l'API del sensore.</span><span class="sxs-lookup"><span data-stu-id="5888e-119">A static library that contains **GUID** definitions for the Sensor API.</span></span>                                     |
| <span data-ttu-id="5888e-120">PortableDeviceGuids. lib</span><span class="sxs-lookup"><span data-stu-id="5888e-120">PortableDeviceGuids.lib</span></span> | <span data-ttu-id="5888e-121">Libreria statica che contiene le definizioni **GUID** per gli oggetti dispositivi portatili Windows.</span><span class="sxs-lookup"><span data-stu-id="5888e-121">A static library that contains **GUID** definitions for Windows Portable Devices objects.</span></span>                   |



 

<span data-ttu-id="5888e-122">Il programma potrebbe richiedere file aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="5888e-122">Your program may require additional files.</span></span>

## <a name="supported-operating-systems"></a><span data-ttu-id="5888e-123">Sistemi operativi supportati</span><span class="sxs-lookup"><span data-stu-id="5888e-123">Supported Operating Systems</span></span>

<span data-ttu-id="5888e-124">Le applicazioni dell'API del sensore vengono eseguite in tutte le edizioni di Windows 7, ad eccezione di Windows 7 Starter Edition.</span><span class="sxs-lookup"><span data-stu-id="5888e-124">Sensor API applications will run on all editions of Windows 7, except for Windows 7 Starter edition.</span></span>

## <a name="windows-portable-devices-interfaces"></a><span data-ttu-id="5888e-125">Interfacce dei dispositivi portatili Windows</span><span class="sxs-lookup"><span data-stu-id="5888e-125">Windows Portable Devices Interfaces</span></span>

<span data-ttu-id="5888e-126">L'API dei sensori USA determinati oggetti dispositivi portatili Windows (WPD) per incapsulare le chiavi e i valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="5888e-126">The Sensor API uses certain Windows Portable Devices (WPD) objects to encapsulate property keys and values.</span></span> <span data-ttu-id="5888e-127">Nella tabella seguente vengono descritte le interfacce per questi oggetti.</span><span class="sxs-lookup"><span data-stu-id="5888e-127">The following table describes the interfaces for these objects.</span></span>



| <span data-ttu-id="5888e-128">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="5888e-128">Interface</span></span>                                                                       | <span data-ttu-id="5888e-129">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5888e-129">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5888e-130">[IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5888e-130">[IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))</span></span>        | <span data-ttu-id="5888e-131">Questa interfaccia fornisce un modo pratico per creare un contenitore di proprietà di coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="5888e-131">This interface provides a convenient way to create a property bag of name/value pairs.</span></span> <span data-ttu-id="5888e-132">I nomi sono rappresentati da **PropertyKey** e i valori sono rappresentati da **PROPVARIANT** s.</span><span class="sxs-lookup"><span data-stu-id="5888e-132">Names are represented by **PROPERTYKEY** s and values are represented by **PROPVARIANT** s.</span></span> <br/> <span data-ttu-id="5888e-133">L'API usa questa interfaccia per l'impostazione e il recupero di valori singoli e set di valori.</span><span class="sxs-lookup"><span data-stu-id="5888e-133">The API uses this interface for setting and retrieving both single values and sets of values.</span></span> <span data-ttu-id="5888e-134">Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamando **CoCreateInstance** con CLSID \_ PortableDeviceValues.</span><span class="sxs-lookup"><span data-stu-id="5888e-134">This interface can be retrieved from a method or, if a new object is required, by calling **CoCreateInstance** with CLSID\_PortableDeviceValues.</span></span><br/> |
| <span data-ttu-id="5888e-135">[IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5888e-135">[IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85))</span></span> | <span data-ttu-id="5888e-136">Questa interfaccia contiene una raccolta di **PropertyKey** s.</span><span class="sxs-lookup"><span data-stu-id="5888e-136">This interface contains a collection of **PROPERTYKEY** s.</span></span> <span data-ttu-id="5888e-137">Queste chiavi rappresentano i nomi di proprietà che possono essere archiviati da **IPortableDeviceValues**.</span><span class="sxs-lookup"><span data-stu-id="5888e-137">These keys represent property names that can be stored by **IPortableDeviceValues**.</span></span> <span data-ttu-id="5888e-138">L'API usa questo oggetto raccolta per impostare e recuperare sia i nomi di proprietà singoli che i set di nomi di proprietà.</span><span class="sxs-lookup"><span data-stu-id="5888e-138">The API uses this collection object for setting and retrieving both single property names and sets of property names.</span></span><br/> <span data-ttu-id="5888e-139">Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamando **CoCreateInstance** con CLSID \_ PortableDeviceKeyCollection.</span><span class="sxs-lookup"><span data-stu-id="5888e-139">This interface can be retrieved from a method or, if a new object is required, by calling **CoCreateInstance** with CLSID\_PortableDeviceKeyCollection.</span></span> <br/>    |



 

 

