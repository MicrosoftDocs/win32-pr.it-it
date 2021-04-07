---
description: La tabella AppId o la tabella del registro di sistema specifica che il programma di installazione configura e registra i server DCOM per eseguire una delle operazioni seguenti durante un'installazione.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: Tabella AppId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fa202907c094d8c12f73d838f5ad1d6b942125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881134"
---
# <a name="appid-table"></a><span data-ttu-id="01833-103">Tabella AppId</span><span class="sxs-lookup"><span data-stu-id="01833-103">AppId Table</span></span>

<span data-ttu-id="01833-104">La tabella AppId o la [tabella del registro di sistema](registry-table.md) specifica che il programma di installazione configura e registra i server DCOM per eseguire una delle operazioni seguenti durante un'installazione.</span><span class="sxs-lookup"><span data-stu-id="01833-104">The AppId table or the [Registry table](registry-table.md) specifies that the installer configure and register DCOM servers to do one of the following during an installation.</span></span>

-   <span data-ttu-id="01833-105">Eseguire il server DCOM con un'identità diversa da quella dell'utente che attiva il server.</span><span class="sxs-lookup"><span data-stu-id="01833-105">Run the DCOM server under a different identity than the user activating the server.</span></span> <span data-ttu-id="01833-106">Ad esempio, per configurare un server DCOM per l'esecuzione sempre come utente interattivo o come utente predefinito.</span><span class="sxs-lookup"><span data-stu-id="01833-106">For example, to configure a DCOM server to always run as an interactive user or as a predefined user.</span></span>
-   <span data-ttu-id="01833-107">Eseguire il server DCOM come servizio.</span><span class="sxs-lookup"><span data-stu-id="01833-107">Run the DCOM server as a service.</span></span>
-   <span data-ttu-id="01833-108">Configurare l'accesso di sicurezza predefinito per il server DCOM.</span><span class="sxs-lookup"><span data-stu-id="01833-108">Configure the default security access for the DCOM server.</span></span>
-   <span data-ttu-id="01833-109">Registrare il server DCOM in modo che sia attivato in un computer diverso.</span><span class="sxs-lookup"><span data-stu-id="01833-109">Register the DCOM server such that it is activated on a different computer.</span></span>

<span data-ttu-id="01833-110">Questa tabella viene elaborata in fase di installazione del componente associato al server DCOM nella \_ colonna componente della tabella della [classe](class-table.md).</span><span class="sxs-lookup"><span data-stu-id="01833-110">This table is processed at the installation of the component associated with the DCOM server in the \_Component column of the [Class table](class-table.md).</span></span> <span data-ttu-id="01833-111">AppId non annunciato.</span><span class="sxs-lookup"><span data-stu-id="01833-111">An AppId is not advertised.</span></span>

<span data-ttu-id="01833-112">La tabella AppId contiene le colonne seguenti.</span><span class="sxs-lookup"><span data-stu-id="01833-112">The AppId table has the following columns.</span></span>



| <span data-ttu-id="01833-113">Colonna</span><span class="sxs-lookup"><span data-stu-id="01833-113">Column</span></span>               | <span data-ttu-id="01833-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="01833-114">Type</span></span>                       | <span data-ttu-id="01833-115">Chiave</span><span class="sxs-lookup"><span data-stu-id="01833-115">Key</span></span> | <span data-ttu-id="01833-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="01833-116">Nullable</span></span> |
|----------------------|----------------------------|-----|----------|
| <span data-ttu-id="01833-117">AppId</span><span class="sxs-lookup"><span data-stu-id="01833-117">AppId</span></span>                | [<span data-ttu-id="01833-118">GUID</span><span class="sxs-lookup"><span data-stu-id="01833-118">GUID</span></span>](guid.md)           | <span data-ttu-id="01833-119">S</span><span class="sxs-lookup"><span data-stu-id="01833-119">Y</span></span>   | <span data-ttu-id="01833-120">N</span><span class="sxs-lookup"><span data-stu-id="01833-120">N</span></span>        |
| <span data-ttu-id="01833-121">RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="01833-121">RemoteServerName</span></span>     | [<span data-ttu-id="01833-122">Formattato</span><span class="sxs-lookup"><span data-stu-id="01833-122">Formatted</span></span>](formatted.md) | <span data-ttu-id="01833-123">N</span><span class="sxs-lookup"><span data-stu-id="01833-123">N</span></span>   | <span data-ttu-id="01833-124">S</span><span class="sxs-lookup"><span data-stu-id="01833-124">Y</span></span>        |
| <span data-ttu-id="01833-125">LocalService</span><span class="sxs-lookup"><span data-stu-id="01833-125">LocalService</span></span>         | [<span data-ttu-id="01833-126">Text</span><span class="sxs-lookup"><span data-stu-id="01833-126">Text</span></span>](text.md)           | <span data-ttu-id="01833-127">N</span><span class="sxs-lookup"><span data-stu-id="01833-127">N</span></span>   | <span data-ttu-id="01833-128">S</span><span class="sxs-lookup"><span data-stu-id="01833-128">Y</span></span>        |
| <span data-ttu-id="01833-129">ServiceParameters</span><span class="sxs-lookup"><span data-stu-id="01833-129">ServiceParameters</span></span>    | [<span data-ttu-id="01833-130">Text</span><span class="sxs-lookup"><span data-stu-id="01833-130">Text</span></span>](text.md)           | <span data-ttu-id="01833-131">N</span><span class="sxs-lookup"><span data-stu-id="01833-131">N</span></span>   | <span data-ttu-id="01833-132">S</span><span class="sxs-lookup"><span data-stu-id="01833-132">Y</span></span>        |
| <span data-ttu-id="01833-133">DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="01833-133">DllSurrogate</span></span>         | [<span data-ttu-id="01833-134">Text</span><span class="sxs-lookup"><span data-stu-id="01833-134">Text</span></span>](text.md)           | <span data-ttu-id="01833-135">N</span><span class="sxs-lookup"><span data-stu-id="01833-135">N</span></span>   | <span data-ttu-id="01833-136">S</span><span class="sxs-lookup"><span data-stu-id="01833-136">Y</span></span>        |
| <span data-ttu-id="01833-137">ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="01833-137">ActivateAtStorage</span></span>    | [<span data-ttu-id="01833-138">Integer</span><span class="sxs-lookup"><span data-stu-id="01833-138">Integer</span></span>](integer.md)     | <span data-ttu-id="01833-139">N</span><span class="sxs-lookup"><span data-stu-id="01833-139">N</span></span>   | <span data-ttu-id="01833-140">S</span><span class="sxs-lookup"><span data-stu-id="01833-140">Y</span></span>        |
| <span data-ttu-id="01833-141">RunAsInteractiveUser</span><span class="sxs-lookup"><span data-stu-id="01833-141">RunAsInteractiveUser</span></span> | [<span data-ttu-id="01833-142">Integer</span><span class="sxs-lookup"><span data-stu-id="01833-142">Integer</span></span>](integer.md)     | <span data-ttu-id="01833-143">N</span><span class="sxs-lookup"><span data-stu-id="01833-143">N</span></span>   | <span data-ttu-id="01833-144">S</span><span class="sxs-lookup"><span data-stu-id="01833-144">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="01833-145">Colonne</span><span class="sxs-lookup"><span data-stu-id="01833-145">Columns</span></span>

<dl> <dt>

<span data-ttu-id="01833-146"><span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId</span><span class="sxs-lookup"><span data-stu-id="01833-146"><span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId</span></span>
</dt> <dd>

<span data-ttu-id="01833-147">La colonna AppId della [tabella della classe](class-table.md) è una chiave esterna in questa colonna della tabella AppID.</span><span class="sxs-lookup"><span data-stu-id="01833-147">The AppId column of the [Class table](class-table.md) is a foreign key into this column of the AppId table.</span></span> <span data-ttu-id="01833-148">Questa colonna contiene il valore AppId che verrà scritto sotto il CLSID e creerà la chiave del GUID AppId in HKCR \\ AppID.</span><span class="sxs-lookup"><span data-stu-id="01833-148">This column contains the AppId value that will be written under the CLSID and creates the AppId GUID key under HKCR\\AppId.</span></span>

</dd> <dt>

<span data-ttu-id="01833-149"><span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="01833-149"><span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName</span></span>
</dt> <dd>

<span data-ttu-id="01833-150">Questa colonna contiene il valore "RemoteServerName" = <xxxx> che verrà scritto in HKCR \\ AppID \\ {AppID} \\ .</span><span class="sxs-lookup"><span data-stu-id="01833-150">This column contains the value of "RemoteServerName"=<xxxx> that will be written under HKCR\\AppID\\{AppID}\\ .</span></span>

</dd> <dt>

<span data-ttu-id="01833-151"><span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService</span><span class="sxs-lookup"><span data-stu-id="01833-151"><span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService</span></span>
</dt> <dd>

<span data-ttu-id="01833-152">Questa colonna contiene il valore di LocalService che verrà scritto in HKCR \\ AppID \\ { <appid> } "LocalService" = <xxx> .</span><span class="sxs-lookup"><span data-stu-id="01833-152">This column contains the value of LocalService that will be written under HKCR\\AppID\\{<appid>} "LocalService"=<xxx>.</span></span>

</dd> <dt>

<span data-ttu-id="01833-153"><span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters</span><span class="sxs-lookup"><span data-stu-id="01833-153"><span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters</span></span>
</dt> <dd>

<span data-ttu-id="01833-154">Questa colonna contiene il valore di ServiceParameters che verrà scritto in HKCR \\ AppID \\ {AppID>} "ServiceParameters".</span><span class="sxs-lookup"><span data-stu-id="01833-154">This column contains the value of ServiceParameters that will be written under HKCR\\AppID\\{appid>} "ServiceParameters".</span></span>

</dd> <dt>

<span data-ttu-id="01833-155"><span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate</span><span class="sxs-lookup"><span data-stu-id="01833-155"><span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate</span></span>
</dt> <dd>

<span data-ttu-id="01833-156">Questa colonna contiene il valore di DllSurrogate che verrà scritto in HKCR \\ AppID \\ { <appid> } "DllSurrogate" = <xxx> .</span><span class="sxs-lookup"><span data-stu-id="01833-156">This column contains the value of DllSurrogate that will be written under HKCR\\AppId\\{<appid>} "DllSurrogate"=<xxx>.</span></span> <span data-ttu-id="01833-157">Se questa colonna è presente, sarà in genere una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="01833-157">If this column is present it will typically be an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="01833-158"><span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage</span><span class="sxs-lookup"><span data-stu-id="01833-158"><span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage</span></span>
</dt> <dd>

<span data-ttu-id="01833-159">Un valore integer diverso da zero in questo campo fa in modo che Windows Installer scriva HKCR \\ AppID \\ { <appid> } "ActivateAtStorage" = "Y" nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="01833-159">A non-zero integer value in this field causes Windows Installer to write HKCR\\AppID\\{<appid>} "ActivateAtStorage"="Y" into the registry.</span></span> <span data-ttu-id="01833-160">Se il campo viene lasciato vuoto o ha un valore pari a zero, non verrà scritto alcun valore.</span><span class="sxs-lookup"><span data-stu-id="01833-160">If the field is left empty, or has a value of zero, no value will be written.</span></span>

</dd> <dt>

<span data-ttu-id="01833-161"><span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser</span><span class="sxs-lookup"><span data-stu-id="01833-161"><span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser</span></span>
</dt> <dd>

<span data-ttu-id="01833-162">Un valore integer diverso da zero in questo campo fa in modo che Windows Installer scriva HKCR \\ AppID \\ {AppID>} "RunAs" = "utente interattivo" nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="01833-162">A non-zero integer value in this field causes Windows Installer to write HKCR\\AppID\\{appid>} "RunAs"="Interactive User" into the registry.</span></span> <span data-ttu-id="01833-163">Se il campo viene lasciato vuoto o ha un valore pari a zero, non verrà scritto alcun valore.</span><span class="sxs-lookup"><span data-stu-id="01833-163">If the field is left empty, or has a value of zero, no value will be written.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01833-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="01833-164">Remarks</span></span>

<span data-ttu-id="01833-165">Questa tabella viene usata dall'azione [registerClassInfo](registerclassinfo-action.md) e dall' [azione UnregisterClassInfo](unregisterclassinfo-action.md).</span><span class="sxs-lookup"><span data-stu-id="01833-165">This table is used by the [RegisterClassInfo action](registerclassinfo-action.md) and [UnregisterClassInfo action](unregisterclassinfo-action.md).</span></span>

<span data-ttu-id="01833-166">Si noti che la tabella AppId non contiene una colonna per la registrazione di un nome predefinito.</span><span class="sxs-lookup"><span data-stu-id="01833-166">Note that the AppId table does not have a column for registering a Default name.</span></span> <span data-ttu-id="01833-167">Pertanto, nei casi in cui è necessario scrivere un nome descrittivo per l'utente come valore predefinito, è necessario registrarsi usando la [tabella del registro di sistema](registry-table.md).</span><span class="sxs-lookup"><span data-stu-id="01833-167">Therefore in cases where you need to write a user friendly name as the Default name value, you must register using the [Registry table](registry-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="01833-168">Convalida</span><span class="sxs-lookup"><span data-stu-id="01833-168">Validation</span></span>

<dl>

[<span data-ttu-id="01833-169">ICE03</span><span class="sxs-lookup"><span data-stu-id="01833-169">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="01833-170">ICE06</span><span class="sxs-lookup"><span data-stu-id="01833-170">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="01833-171">ICE32</span><span class="sxs-lookup"><span data-stu-id="01833-171">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="01833-172">ICE33</span><span class="sxs-lookup"><span data-stu-id="01833-172">ICE33</span></span>](ice33.md)  
[<span data-ttu-id="01833-173">ICE46</span><span class="sxs-lookup"><span data-stu-id="01833-173">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="01833-174">ICE69</span><span class="sxs-lookup"><span data-stu-id="01833-174">ICE69</span></span>](ice69.md)  
</dl>

 

 



