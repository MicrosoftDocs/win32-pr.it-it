---
description: L'oggetto di gestione dei sensori consente di accedere ai sensori disponibili per l'utilizzo.
ms.assetid: dd39d533-9983-41b4-a9a3-d94dcadebaac
title: Oggetto di gestione dei sensori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715448a62c058c5e6825368003939e5ae2066847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128739"
---
# <a name="the-sensor-manager-object"></a><span data-ttu-id="31f90-103">Oggetto di gestione dei sensori</span><span class="sxs-lookup"><span data-stu-id="31f90-103">The Sensor Manager Object</span></span>

<span data-ttu-id="31f90-104">L'oggetto di gestione dei sensori consente di accedere ai sensori disponibili per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="31f90-104">The sensor manager object provides access to the sensors that are available for your use.</span></span>

<span data-ttu-id="31f90-105">Per usare l'API del sensore, è prima necessario chiamare il metodo COM **CoCreateInstance** per creare un'istanza dell'oggetto di gestione dei sensori e recuperare un puntatore alla relativa interfaccia, denominato [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager).</span><span class="sxs-lookup"><span data-stu-id="31f90-105">To use the Sensor API, you must first call the COM **CoCreateInstance** method to create an instance of the sensor manager object and retrieve a pointer to its interface, named [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager).</span></span> <span data-ttu-id="31f90-106">Gestione sensori mantiene l'elenco dei sensori disponibili.</span><span class="sxs-lookup"><span data-stu-id="31f90-106">The sensor manager maintains the list of available sensors.</span></span> <span data-ttu-id="31f90-107">È possibile usare **ISensorManager** per chiamare metodi che recuperano gruppi di sensori per categoria o per tipo oppure è possibile chiamare un metodo per recuperare un determinato sensore usando il relativo ID univoco.</span><span class="sxs-lookup"><span data-stu-id="31f90-107">You can use **ISensorManager** to call methods that retrieve groups of sensors by category or by type, or you can call a method to retrieve a particular sensor by using its unique ID.</span></span> <span data-ttu-id="31f90-108">Gestione sensori consente inoltre di effettuare la registrazione per ricevere un evento che informa l'utente quando un nuovo sensore è stato connesso alla piattaforma.</span><span class="sxs-lookup"><span data-stu-id="31f90-108">The sensor manager also enables you to register to receive an event that notifies you when a new sensor has been connected to the platform.</span></span>

<span data-ttu-id="31f90-109">In alcuni casi, il gestore dei sensori fornisce un puntatore a un sensore, ma l'utente non ha abilitato il sensore.</span><span class="sxs-lookup"><span data-stu-id="31f90-109">Sometimes, the sensor manager provides a pointer to a sensor, but the user has not enabled the sensor.</span></span> <span data-ttu-id="31f90-110">Ad esempio, è spesso possibile recuperare i valori per le proprietà dei sensori non privati, ad esempio il produttore o il modello del sensore, prima che l'utente Abilita il sensore.</span><span class="sxs-lookup"><span data-stu-id="31f90-110">For example, you can often retrieve values for non-private sensor properties, such as the sensor manufacturer or model, before the user enables the sensor.</span></span> <span data-ttu-id="31f90-111">Queste informazioni possono essere utili per decidere se richiedere all'utente l'autorizzazione per l'uso del sensore.</span><span class="sxs-lookup"><span data-stu-id="31f90-111">This information can help you to decide whether to ask the user for permission to use the sensor.</span></span> <span data-ttu-id="31f90-112">È possibile chiamare [**ISensorManager:: RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) per richiedere all'utente di abilitare un sensore o una raccolta di sensori particolare.</span><span class="sxs-lookup"><span data-stu-id="31f90-112">You can call [**ISensorManager::RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) to prompt the user to enable a particular sensor or collection of sensors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31f90-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="31f90-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31f90-114">Gestione delle autorizzazioni utente</span><span class="sxs-lookup"><span data-stu-id="31f90-114">Managing User Permissions</span></span>](managing-user-permissions.md)
</dt> <dt>

[<span data-ttu-id="31f90-115">Richiesta di autorizzazioni utente</span><span class="sxs-lookup"><span data-stu-id="31f90-115">Requesting User Permissions</span></span>](requesting-user-permissions.md)
</dt> </dl>

 

 
