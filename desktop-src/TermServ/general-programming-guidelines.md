---
title: Linee guida generali per la programmazione
description: Linee guida per lo sviluppo di applicazioni in un ambiente Servizi Desktop remoto.
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465c658e64959eb1bfd61cf3c43f6ffd2cc6b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300024"
---
# <a name="general-programming-guidelines"></a><span data-ttu-id="b6bbc-103">Linee guida generali per la programmazione</span><span class="sxs-lookup"><span data-stu-id="b6bbc-103">General programming guidelines</span></span>

<span data-ttu-id="b6bbc-104">Nelle sezioni seguenti vengono fornite linee guida generali per lo sviluppo di applicazioni in un ambiente Servizi Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="b6bbc-104">The following sections provide general guidelines for developing applications in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b6bbc-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="b6bbc-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="b6bbc-106">Livello di compatibilità delle applicazioni</span><span class="sxs-lookup"><span data-stu-id="b6bbc-106">Application compatibility layer</span></span>](application-compatibility-layer.md)
</dt> <dd>

<span data-ttu-id="b6bbc-107">Per eseguire applicazioni legacy in un ambiente Servizi Desktop remoto è possibile usare il Servizi Desktop remoto livello di compatibilità delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="b6bbc-107">To run legacy applications in a Remote Desktop Services environment you can use the Remote Desktop Services Application Compatibility layer.</span></span>

</dd> <dt>

[<span data-ttu-id="b6bbc-108">Linee guida per applicazioni client/server</span><span class="sxs-lookup"><span data-stu-id="b6bbc-108">Client/Server application guidelines</span></span>](client-server-application-guidelines.md)
</dt> <dd>

<span data-ttu-id="b6bbc-109">Le applicazioni client/server non devono presupporre che una connessione a computer singolo sia equivalente a una singola sessione utente.</span><span class="sxs-lookup"><span data-stu-id="b6bbc-109">Client/server applications must not assume that a single computer connection is equivalent to a single user session.</span></span>

</dd> <dt>

[<span data-ttu-id="b6bbc-110">Monitoraggio di connessioni e disconnessioni di sessione</span><span class="sxs-lookup"><span data-stu-id="b6bbc-110">Monitoring session connections and disconnections</span></span>](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

<span data-ttu-id="b6bbc-111">Per registrare un'applicazione con Servizi Desktop remoto, archiviare il nome dell'applicazione Virtual Channel Server nel registro di sistema aggiungendo una sottochiave.</span><span class="sxs-lookup"><span data-stu-id="b6bbc-111">To register an application with Remote Desktop Services, store the name of the virtual channel server application in the registry by adding a subkey.</span></span>

</dd> <dt>

[<span data-ttu-id="b6bbc-112">Linee guida hardware periferiche</span><span class="sxs-lookup"><span data-stu-id="b6bbc-112">Peripheral hardware guidelines</span></span>](peripheral-hardware-guidelines.md)
</dt> <dd>

<span data-ttu-id="b6bbc-113">Se il dispositivo hardware non è progettato per funzionare in una sessione remota, i fornitori devono garantire che il software dei driver di dispositivo forzi la disabilitazione del reindirizzamento del dispositivo usando criteri di sistema o criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="b6bbc-113">If their hardware device is not designed to work over a remote session, vendors must ensure that the device driver software forces disabling the redirection of the device by using a system policy or group policy.</span></span>

</dd> <dt>

[<span data-ttu-id="b6bbc-114">Collegamento di run-time a Wtsapi32.dll</span><span class="sxs-lookup"><span data-stu-id="b6bbc-114">Run-Time linking to Wtsapi32.dll</span></span>](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

<span data-ttu-id="b6bbc-115">L'applicazione può usare l'API Servizi Desktop remoto per collegare in modo dinamico al Wtsapi32.dll in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b6bbc-115">Your application can use the Remote Desktop Services API to dynamically link to the Wtsapi32.dll at run time.</span></span> <span data-ttu-id="b6bbc-116">A tale scopo, l'applicazione deve chiamare la funzione [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) per caricare Wtsapi32.dll.</span><span class="sxs-lookup"><span data-stu-id="b6bbc-116">To do this, your application should call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Wtsapi32.dll.</span></span>

</dd> </dl>

 

 