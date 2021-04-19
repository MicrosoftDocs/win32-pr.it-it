---
description: "Altre informazioni su: l'esempio completo del servizio"
ms.assetid: a3aeea9b-09c0-4834-892a-c378b67402f4
title: Esempio di servizio completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb87ebfef3f964eacee66be94a4b5291c335d0d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316086"
---
# <a name="the-complete-service-sample"></a><span data-ttu-id="a5c77-103">Esempio di servizio completo</span><span class="sxs-lookup"><span data-stu-id="a5c77-103">The Complete Service Sample</span></span>

<span data-ttu-id="a5c77-104">Gli argomenti di questa sezione costituiscono un esempio di servizio completo:</span><span class="sxs-lookup"><span data-stu-id="a5c77-104">The topics in this section form a complete service sample:</span></span>

-   <span data-ttu-id="a5c77-105">[Sample.MC](sample-mc.md) (contiene messaggi di errore)</span><span class="sxs-lookup"><span data-stu-id="a5c77-105">[Sample.mc](sample-mc.md) (contains error messages)</span></span>
-   <span data-ttu-id="a5c77-106">[Svc. cpp](svc-cpp.md) (contiene il codice del servizio)</span><span class="sxs-lookup"><span data-stu-id="a5c77-106">[Svc.cpp](svc-cpp.md) (contains the service code)</span></span>
-   <span data-ttu-id="a5c77-107">[SvcConfig. cpp](svcconfig-cpp.md) (contiene il codice di configurazione del servizio)</span><span class="sxs-lookup"><span data-stu-id="a5c77-107">[SvcConfig.cpp](svcconfig-cpp.md) (contains service configuration code)</span></span>
-   <span data-ttu-id="a5c77-108">[SvcControl. cpp](svccontrol-cpp.md) (contiene il codice di controllo del servizio)</span><span class="sxs-lookup"><span data-stu-id="a5c77-108">[SvcControl.cpp](svccontrol-cpp.md) (contains service control code)</span></span>

## <a name="building-the-service"></a><span data-ttu-id="a5c77-109">Compilazione del servizio</span><span class="sxs-lookup"><span data-stu-id="a5c77-109">Building the Service</span></span>

<span data-ttu-id="a5c77-110">Nella procedura seguente viene descritto come compilare il servizio e registrare la DLL del messaggio di evento.</span><span class="sxs-lookup"><span data-stu-id="a5c77-110">The following procedure describes how to build the service and register the event message DLL.</span></span>

<span data-ttu-id="a5c77-111">**Per compilare il servizio e registrare la DLL del messaggio di evento**</span><span class="sxs-lookup"><span data-stu-id="a5c77-111">**To build the service and register the event message DLL**</span></span>

1.  <span data-ttu-id="a5c77-112">Compilare la DLL del messaggio da Sample.mc attenendosi alla procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="a5c77-112">Build the message DLL from Sample.mc using the following steps:</span></span>
    1.  <span data-ttu-id="a5c77-113">**MC-U sample.mc**</span><span class="sxs-lookup"><span data-stu-id="a5c77-113">**mc -U sample.mc**</span></span>
    2.  <span data-ttu-id="a5c77-114">**esempio RC-r. RC**</span><span class="sxs-lookup"><span data-stu-id="a5c77-114">**rc -r sample.rc**</span></span>
    3.  <span data-ttu-id="a5c77-115">**link-DLL-NOENTRY -out:sample.dll Sample. res**</span><span class="sxs-lookup"><span data-stu-id="a5c77-115">**link -dll -noentry -out:sample.dll sample.res**</span></span>
2.  <span data-ttu-id="a5c77-116">Compilare rispettivamente Svc.exe, SvcConfig.exe e SvcControl.exe da svc. cpp, SvcConfig. cpp e SvcControl. cpp.</span><span class="sxs-lookup"><span data-stu-id="a5c77-116">Build Svc.exe, SvcConfig.exe, and SvcControl.exe from Svc.cpp, SvcConfig.cpp, and SvcControl.cpp, respectively.</span></span>
3.  <span data-ttu-id="a5c77-117">Creare la chiave del registro di **\_ sistema HKEY LOCAL \_ Machine \\ System \\ CurrentControlSet \\ Services \\ EventLog \\ Application \\ SvcName** e aggiungere i valori del registro di sistema seguenti a questa chiave.</span><span class="sxs-lookup"><span data-stu-id="a5c77-117">Create the registry key **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Services\\EventLog\\Application\\SvcName** and add the following registry values to this key.</span></span>

    | <span data-ttu-id="a5c77-118">Valore</span><span class="sxs-lookup"><span data-stu-id="a5c77-118">Value</span></span>                              | <span data-ttu-id="a5c77-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5c77-119">Type</span></span>       | <span data-ttu-id="a5c77-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5c77-120">Description</span></span>                                                                                                        |
    |------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="a5c77-121">**EventMessageFile**  =  *\_ percorso dll*</span><span class="sxs-lookup"><span data-stu-id="a5c77-121">**EventMessageFile** = *dll\_path*</span></span> | <span data-ttu-id="a5c77-122">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="a5c77-122">REG\_SZ</span></span>    | <span data-ttu-id="a5c77-123">Percorso della DLL di sole risorse contenente le stringhe che il servizio è in grado di scrivere nel log eventi.</span><span class="sxs-lookup"><span data-stu-id="a5c77-123">The path to the resource-only DLL that contains strings that the service can write to the event log.</span></span>               |
    | <span data-ttu-id="a5c77-124">**TypesSupported** = 0x00000007</span><span class="sxs-lookup"><span data-stu-id="a5c77-124">**TypesSupported** = 0x00000007</span></span>    | <span data-ttu-id="a5c77-125">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="a5c77-125">REG\_DWORD</span></span> | <span data-ttu-id="a5c77-126">Maschera di bit che specifica i tipi di evento supportati.</span><span class="sxs-lookup"><span data-stu-id="a5c77-126">A bit mask that specifies the supported event types.</span></span> <span data-ttu-id="a5c77-127">Il valore 0x000000007 indica che sono supportati tutti i tipi.</span><span class="sxs-lookup"><span data-stu-id="a5c77-127">The value 0x000000007 indicates that all types are supported.</span></span> |

    

     

## <a name="testing-the-service"></a><span data-ttu-id="a5c77-128">Test del servizio</span><span class="sxs-lookup"><span data-stu-id="a5c77-128">Testing the Service</span></span>

<span data-ttu-id="a5c77-129">Nella procedura seguente viene descritto come eseguire il test del servizio.</span><span class="sxs-lookup"><span data-stu-id="a5c77-129">The following procedure describes how to test the service.</span></span>

<span data-ttu-id="a5c77-130">**Per eseguire il test del servizio**</span><span class="sxs-lookup"><span data-stu-id="a5c77-130">**To test the service**</span></span>

1.  <span data-ttu-id="a5c77-131">Nel pannello di controllo avviare l'applicazione dei **Servizi** .</span><span class="sxs-lookup"><span data-stu-id="a5c77-131">In Control Panel, start the **Services** application.</span></span> <span data-ttu-id="a5c77-132">Nei passaggi seguenti usare il tasto F5 per aggiornare la visualizzazione dopo l'esecuzione di un comando che modifica le informazioni nell'applicazione dei **Servizi** .</span><span class="sxs-lookup"><span data-stu-id="a5c77-132">(In the following steps, use the F5 key to refresh the display after executing a command that modifies the information in the **Services** application.)</span></span>
2.  <span data-ttu-id="a5c77-133">Eseguire il comando seguente per installare il servizio:</span><span class="sxs-lookup"><span data-stu-id="a5c77-133">Run the following command to install the service:</span></span>

    <span data-ttu-id="a5c77-134">**installazione SVC**</span><span class="sxs-lookup"><span data-stu-id="a5c77-134">**svc install**</span></span>

    <span data-ttu-id="a5c77-135">Il servizio scrive "servizio installato correttamente" nella console di se l'operazione ha esito positivo o un messaggio di errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a5c77-135">The service writes "Service installed successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="a5c77-136">Se l'installazione del servizio ha esito positivo, il servizio viene visualizzato nell'applicazione dei **Servizi** .</span><span class="sxs-lookup"><span data-stu-id="a5c77-136">If the service installation succeeds, the service is displayed in the **Services** application.</span></span> <span data-ttu-id="a5c77-137">Si noti che il **nome** è impostato su "SvcName", la **Descrizione** e **lo stato** sono vuoti e il **tipo di avvio** è impostato su "Manual".</span><span class="sxs-lookup"><span data-stu-id="a5c77-137">Note that **Name** is set to "SvcName", **Description** and **Status** are blank, and **Startup Type** is set to "Manual".</span></span>

3.  <span data-ttu-id="a5c77-138">Eseguire il comando seguente per avviare il servizio:</span><span class="sxs-lookup"><span data-stu-id="a5c77-138">Run the following command to start the service:</span></span>

    <span data-ttu-id="a5c77-139">**SvcControl avviare SvcName**</span><span class="sxs-lookup"><span data-stu-id="a5c77-139">**svccontrol start SvcName**</span></span>

    <span data-ttu-id="a5c77-140">Se l'operazione ha esito positivo, il programma di controllo del servizio scrive "avvio del servizio in sospeso..." e "il servizio è stato avviato correttamente" nella console.</span><span class="sxs-lookup"><span data-stu-id="a5c77-140">If the operation succeeds, the service control program writes "Service start pending..." and then "Service started successfully" to the console.</span></span> <span data-ttu-id="a5c77-141">In caso contrario, il programma scrive un messaggio di errore nella console.</span><span class="sxs-lookup"><span data-stu-id="a5c77-141">Otherwise, the program writes an error message to the console.</span></span>

    <span data-ttu-id="a5c77-142">Se il servizio viene avviato correttamente, **lo stato** è impostato su "avviato".</span><span class="sxs-lookup"><span data-stu-id="a5c77-142">If the service starts successfully, **Status** is set to "Started".</span></span> <span data-ttu-id="a5c77-143">Il codice nella funzione [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) viene eseguito dal gestore SCM.</span><span class="sxs-lookup"><span data-stu-id="a5c77-143">The code in the [*ServiceMain*](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) function is executed by the SCM.</span></span> <span data-ttu-id="a5c77-144">Se si verifica un errore, il servizio scriverà un messaggio di errore nel registro eventi.</span><span class="sxs-lookup"><span data-stu-id="a5c77-144">If an error occurs, the service will write an error message to the event log.</span></span> <span data-ttu-id="a5c77-145">Questo messaggio include il nome della funzione che ha avuto esito negativo e il codice di errore restituito in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="a5c77-145">This message includes the name of the function that failed and the error code that was returned on failure.</span></span>

4.  <span data-ttu-id="a5c77-146">Eseguire il comando seguente per aggiornare la descrizione del servizio:</span><span class="sxs-lookup"><span data-stu-id="a5c77-146">Run the following command to update the service description:</span></span>

    <span data-ttu-id="a5c77-147">**svcconfig descrivere SvcName**</span><span class="sxs-lookup"><span data-stu-id="a5c77-147">**svcconfig describe SvcName**</span></span>

    <span data-ttu-id="a5c77-148">Il programma di configurazione del servizio scrive "Descrizione servizio aggiornata" nella console di se l'operazione ha esito positivo o un messaggio di errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a5c77-148">The service configuration program writes "Service description updated successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="a5c77-149">Se l'aggiornamento ha esito positivo, la **Descrizione** è impostata su "Questa è una descrizione del test".</span><span class="sxs-lookup"><span data-stu-id="a5c77-149">If the update succeeds, **Description** is set to "This is a test description".</span></span>

5.  <span data-ttu-id="a5c77-150">Eseguire il comando seguente per eseguire una query sulla configurazione del servizio:</span><span class="sxs-lookup"><span data-stu-id="a5c77-150">Run the following command to query the service configuration:</span></span>

    <span data-ttu-id="a5c77-151">**SvcName query svcconfig**</span><span class="sxs-lookup"><span data-stu-id="a5c77-151">**svcconfig query SvcName**</span></span>

    <span data-ttu-id="a5c77-152">Il programma di configurazione del servizio scrive le informazioni di configurazione del servizio nella console di se l'operazione ha esito positivo o un messaggio di errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a5c77-152">The service configuration program writes the service configuration information to the console if the operation succeeds or an error message otherwise.</span></span>

6.  <span data-ttu-id="a5c77-153">Eseguire il comando seguente per modificare il DACL del servizio:</span><span class="sxs-lookup"><span data-stu-id="a5c77-153">Run the following command to change the service DACL:</span></span>

    <span data-ttu-id="a5c77-154">**SvcName DACL SvcControl**</span><span class="sxs-lookup"><span data-stu-id="a5c77-154">**svccontrol dacl SvcName**</span></span>

    <span data-ttu-id="a5c77-155">Il programma di configurazione del servizio scrive "DACL servizio aggiornato" alla console se l'operazione ha esito positivo o un messaggio di errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a5c77-155">The service configuration program writes "Service DACL updated successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

7.  <span data-ttu-id="a5c77-156">Eseguire il comando seguente per disabilitare il servizio:</span><span class="sxs-lookup"><span data-stu-id="a5c77-156">Run the following command to disable the service:</span></span>

    <span data-ttu-id="a5c77-157">**svcconfig Disabilita SvcName**</span><span class="sxs-lookup"><span data-stu-id="a5c77-157">**svcconfig disable SvcName**</span></span>

    <span data-ttu-id="a5c77-158">Il programma di configurazione del servizio scrive "servizio disabilitato correttamente" nella console di se l'operazione ha esito positivo o un messaggio di errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a5c77-158">The service configuration program writes "Service disabled successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="a5c77-159">Se il servizio è stato disabilitato correttamente, il **tipo di avvio** è impostato su "disabilitato".</span><span class="sxs-lookup"><span data-stu-id="a5c77-159">If the service is disabled successfully, **Startup Type** is set to "Disabled".</span></span>

8.  <span data-ttu-id="a5c77-160">Eseguire il comando seguente per abilitare il servizio:</span><span class="sxs-lookup"><span data-stu-id="a5c77-160">Run the following command to enable the service:</span></span>

    <span data-ttu-id="a5c77-161">**svcconfig Abilita SvcName**</span><span class="sxs-lookup"><span data-stu-id="a5c77-161">**svcconfig enable SvcName**</span></span>

    <span data-ttu-id="a5c77-162">Il programma di configurazione del servizio scrive "servizio abilitato correttamente" nella console se l'operazione ha esito positivo o un messaggio di errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a5c77-162">The service configuration program writes "Service enabled successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="a5c77-163">Se il servizio è stato abilitato correttamente, il **tipo di avvio** è impostato su "manuale".</span><span class="sxs-lookup"><span data-stu-id="a5c77-163">If the service is enabled successfully, **Startup Type** is set to "Manual".</span></span>

9.  <span data-ttu-id="a5c77-164">Eseguire il comando seguente per arrestare il servizio:</span><span class="sxs-lookup"><span data-stu-id="a5c77-164">Run the following command to stop the service:</span></span>

    <span data-ttu-id="a5c77-165">**SvcControl arrestare SvcName**</span><span class="sxs-lookup"><span data-stu-id="a5c77-165">**svccontrol stop SvcName**</span></span>

    <span data-ttu-id="a5c77-166">Se l'operazione ha esito positivo, il programma di controllo del servizio scrive "arresto servizio in sospeso..." e quindi "il servizio è stato arrestato correttamente" nella console.</span><span class="sxs-lookup"><span data-stu-id="a5c77-166">If the operation succeeds, the service control program writes "Service stop pending..." and then "Service stopped successfully" to the console.</span></span> <span data-ttu-id="a5c77-167">In caso contrario, il programma scrive un messaggio di errore nella console.</span><span class="sxs-lookup"><span data-stu-id="a5c77-167">Otherwise, the program writes an error message to the console.</span></span>

    <span data-ttu-id="a5c77-168">Se il servizio viene arrestato correttamente, **lo stato** è vuoto.</span><span class="sxs-lookup"><span data-stu-id="a5c77-168">If the service stops successfully, **Status** is blank.</span></span>

    <span data-ttu-id="a5c77-169">Se il servizio non viene arrestato, il programma di controllo del servizio scrive un messaggio di errore nel registro eventi che include il nome della funzione che ha avuto esito negativo e il codice di errore restituito in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="a5c77-169">If the service fails to stop, the service control program writes an error message to the event log that includes the name of the function that failed and the error code that was returned on failure.</span></span>

10. <span data-ttu-id="a5c77-170">Eseguire il comando seguente per eliminare il servizio:</span><span class="sxs-lookup"><span data-stu-id="a5c77-170">Run the following command to delete the service:</span></span>

    <span data-ttu-id="a5c77-171">**svcconfig eliminare SvcName**</span><span class="sxs-lookup"><span data-stu-id="a5c77-171">**svcconfig delete SvcName**</span></span>

    <span data-ttu-id="a5c77-172">Il programma di configurazione del servizio scrive "Servizio eliminato correttamente" nella console di se l'operazione ha esito positivo o un messaggio di errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a5c77-172">The service configuration program writes "Service deleted successfully" to the console if the operation succeeds or an error message otherwise.</span></span>

    <span data-ttu-id="a5c77-173">Se il servizio viene eliminato correttamente, non viene più visualizzato nell'applicazione **dei servizi** .</span><span class="sxs-lookup"><span data-stu-id="a5c77-173">If the service is deleted successfully, it is no longer displayed in the **Services** application.</span></span> <span data-ttu-id="a5c77-174">Si noti che se si tenta di eliminare un servizio non arrestato, l'operazione ha esito positivo, ma il **tipo di avvio** è impostato su "disabilitato" e la voce del servizio verrà eliminata al riavvio del sistema o quando il servizio viene terminato tramite Gestione attività.</span><span class="sxs-lookup"><span data-stu-id="a5c77-174">(Note that if you attempt to delete a service that is not stopped, the operation succeeds but **Startup Type** is set to "Disabled" and the service entry will be deleted at system restart or when the service is terminated using Task Manager.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5c77-175">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a5c77-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5c77-176">Uso dei servizi</span><span class="sxs-lookup"><span data-stu-id="a5c77-176">Using Services</span></span>](using-services.md)
</dt> </dl>

 

 
