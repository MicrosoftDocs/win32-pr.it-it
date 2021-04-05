---
title: LocalService
description: Installa un oggetto come applicazione di servizio.
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- Valore LocalService del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f630c7c0a6f5e3bbf4b9c26ad82e5a104be238
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103873022"
---
# <a name="localservice"></a><span data-ttu-id="5d960-104">LocalService</span><span class="sxs-lookup"><span data-stu-id="5d960-104">LocalService</span></span>

<span data-ttu-id="5d960-105">Installa un oggetto come applicazione di servizio.</span><span class="sxs-lookup"><span data-stu-id="5d960-105">Installs an object as a service application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="5d960-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="5d960-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LocalService = name
```

## <a name="remarks"></a><span data-ttu-id="5d960-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d960-107">Remarks</span></span>

<span data-ttu-id="5d960-108">Oltre a essere eseguito come file eseguibile del server locale (EXE), un oggetto COM può anche scegliere di creare un pacchetto per l'esecuzione come applicazione di servizio quando viene attivato da un client locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="5d960-108">In addition to running as a local server executable (EXE), a COM object may also choose to package itself to run as a service application when activated by a local or remote client.</span></span> <span data-ttu-id="5d960-109">I servizi supportano numerose funzionalità amministrative utili e integrate nell'interfaccia utente, tra cui l'avvio, l'arresto, la sospensione e il riavvio locali e remoti, nonché la possibilità di stabilire il server per l'esecuzione con un account utente e una stazione di finestra specifici.</span><span class="sxs-lookup"><span data-stu-id="5d960-109">Services support numerous useful and UI-integrated administrative features, including local and remote starting, stopping, pausing, and restarting, as well as the ability to establish the server to run under a specific user account and window station.</span></span>

<span data-ttu-id="5d960-110">Un oggetto scritto come servizio viene installato per l'uso da COM mediante la definizione di un valore **LocalService** e l'esecuzione di un'installazione del servizio standard.</span><span class="sxs-lookup"><span data-stu-id="5d960-110">An object written as a service is installed for use by COM by establishing a **LocalService** value and performing a standard service installation.</span></span> <span data-ttu-id="5d960-111">Il valore **LocalService** deve essere impostato sul nome del servizio, come configurato in **HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Services**, come valore predefinito di **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="5d960-111">The **LocalService** value must be set to the service name, as configured in **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services**, as the default **REG\_SZ** value.</span></span>

<span data-ttu-id="5d960-112">Quando **LocalService** è impostato, qualsiasi stringa assegnata a [**ServiceParameters**](serviceparameters.md) viene passata come argomento della riga di comando al servizio mentre viene avviata.</span><span class="sxs-lookup"><span data-stu-id="5d960-112">When **LocalService** is set, any string assigned to [**ServiceParameters**](serviceparameters.md) is passed as a command-line argument to the service as it is being launched.</span></span>

<span data-ttu-id="5d960-113">La configurazione del servizio è preferibile in molte situazioni in cui le funzionalità delle API di gestione dei servizi locali e remote e dell'interfaccia utente possono essere utili per i servizi forniti dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5d960-113">The service configuration is preferred in many situations where the capabilities of the local and remote service management APIs and user interface might be useful for the services that the object provides.</span></span> <span data-ttu-id="5d960-114">Ad esempio, l'utilizzo del Framework di amministrazione esistente dell'architettura del servizio deve essere una scelta ovvia se l'oggetto è di lunga durata o supporta facilmente concetti quali l'avvio, l'arresto, la reimpostazione o la sospensione.</span><span class="sxs-lookup"><span data-stu-id="5d960-114">For example, leveraging the existing administrative framework of the service architecture should be an obvious choice if the object is long-lived or readily supports concepts such as starting, stopping, resetting, or pausing.</span></span>

<span data-ttu-id="5d960-115">I servizi possono essere configurati dinamicamente e possono essere configurati per l'esecuzione automatica all'avvio del computer o per essere avviati quando richiesto da un'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="5d960-115">Services can be dynamically configured and can be configured to run automatically when the machine boots, or to be launched when requested by a client application.</span></span>

<span data-ttu-id="5d960-116">Se si implementano classi come servizi, è necessario tenere presenti i punti seguenti:</span><span class="sxs-lookup"><span data-stu-id="5d960-116">If you are implementing classes as services, you should be aware of the following points:</span></span>

-   <span data-ttu-id="5d960-117">Questo valore viene usato in preferenza con la chiave [**LocalServer32**](localserver32.md) per l'attivazione locale e remota requestsâ € "Se **LocalService** esiste e fa riferimento a un servizio valido, la chiave **LocalServer32** viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="5d960-117">This value is used in preference to the [**LocalServer32**](localserver32.md) key for local and remote activation requestsâ€”if **LocalService** exists and refers to a valid service, the **LocalServer32** key is ignored.</span></span>
-   <span data-ttu-id="5d960-118">Attualmente, solo una singola istanza di un'applicazione di servizio potrebbe essere in esecuzione in un determinato momento in un computer.</span><span class="sxs-lookup"><span data-stu-id="5d960-118">Currently, only a single instance of a service application may be running at a given time on a computer.</span></span> <span data-ttu-id="5d960-119">I servizi COM devono quindi registrare gli oggetti classe all'avvio usando REGCLS \_ MULTIPLEUSE per supportare più client.</span><span class="sxs-lookup"><span data-stu-id="5d960-119">COM services must therefore register their class objects on launch using REGCLS\_MULTIPLEUSE to support multiple clients.</span></span>
-   <span data-ttu-id="5d960-120">Per avviare e inizializzare correttamente, i servizi COM configurati per l'esecuzione automatica quando un computer viene avviato devono includere RPCSS nell'elenco di servizi dipendenti.</span><span class="sxs-lookup"><span data-stu-id="5d960-120">To launch and initialize properly, COM services configured to run automatically when a machine boots must include RPCSS in their list of dependent services.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d960-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5d960-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d960-122">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="5d960-122">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="5d960-123">**ServiceParameters**</span><span class="sxs-lookup"><span data-stu-id="5d960-123">**ServiceParameters**</span></span>](serviceparameters.md)
</dt> <dt>

[<span data-ttu-id="5d960-124">Services</span><span class="sxs-lookup"><span data-stu-id="5d960-124">Services</span></span>](/windows/desktop/Services/services)
</dt> </dl>

 

 