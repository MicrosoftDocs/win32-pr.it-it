---
description: Si tratta della proprietà Mode dell'oggetto Session. Questa proprietà è un valore che rappresenta il flag della modalità designata per la sessione di installazione corrente. La maggior parte dei flag della modalità è di sola lettura esternamente, ma è possibile impostare anche alcuni flag specificati.
ms.assetid: 9aca413d-d653-4ec1-a39b-af956f6c95e7
title: Proprietà Session. Mode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Mode
api_type:
- COM
api_location: ''
ms.openlocfilehash: f081859db789601f2c41bf95d65c377fba8d51f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333048"
---
# <a name="sessionmode-property"></a><span data-ttu-id="9004e-105">Proprietà Session. Mode</span><span class="sxs-lookup"><span data-stu-id="9004e-105">Session.Mode property</span></span>

<span data-ttu-id="9004e-106">Si tratta della proprietà **mode** dell'oggetto [**Session**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="9004e-106">This is the **Mode** property of the [**Session**](session-object.md) object.</span></span> <span data-ttu-id="9004e-107">Questa proprietà è un valore che rappresenta il flag della modalità designata per la sessione di installazione corrente.</span><span class="sxs-lookup"><span data-stu-id="9004e-107">This property is a value representing the designated mode flag for the current install session.</span></span> <span data-ttu-id="9004e-108">La maggior parte dei flag della modalità è di sola lettura esternamente, ma è possibile impostare anche alcuni flag specificati.</span><span class="sxs-lookup"><span data-stu-id="9004e-108">Most of the mode flags are read-only externally, but a few specified flags may be set as well.</span></span>

<span data-ttu-id="9004e-109">La funzione [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) restituisce un valore booleano true o false, che indica se la proprietà specifica passata nella funzione è attualmente impostata (true) o non impostata (false).</span><span class="sxs-lookup"><span data-stu-id="9004e-109">The [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) function returns a Boolean TRUE or FALSE, indicating whether the specific property passed into the function is currently set (TRUE) or not set (FALSE).</span></span>

<span data-ttu-id="9004e-110">Si noti che non tutti i valori della modalità di esecuzione del *flag* sono disponibili quando si chiama la proprietà **mode** da un'azione personalizzata posticipata.</span><span class="sxs-lookup"><span data-stu-id="9004e-110">Note that not all the run mode values of *flag* are available when calling the **Mode** property from a deferred custom action.</span></span> <span data-ttu-id="9004e-111">Per altre informazioni, vedere [ottenere informazioni sul contesto per le azioni personalizzate di esecuzione posticipata](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="9004e-111">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="9004e-112">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9004e-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9004e-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9004e-113">Syntax</span></span>


```JScript
propVal = Session.Mode
```



## <a name="property-value"></a><span data-ttu-id="9004e-114">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9004e-114">Property value</span></span>

<span data-ttu-id="9004e-115">Valore intero obbligatorio per il flag.</span><span class="sxs-lookup"><span data-stu-id="9004e-115">Required integer value for the flag.</span></span> <span data-ttu-id="9004e-116">I possibili valori sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9004e-116">Must be one of the following:</span></span>



| <span data-ttu-id="9004e-117">Nome del flag</span><span class="sxs-lookup"><span data-stu-id="9004e-117">Flag name</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="9004e-118">Significato</span><span class="sxs-lookup"><span data-stu-id="9004e-118">Meaning</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiRunModeAdmin"></span><span id="msirunmodeadmin"></span><span id="MSIRUNMODEADMIN"></span><dl> <span data-ttu-id="9004e-119"><dt>**msiRunModeAdmin**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-119"><dt>**msiRunModeAdmin**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="9004e-120">Installazione in modalità amministrativa, altrimenti installazione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="9004e-120">Administrative mode install, else product install.</span></span><br/>                                  |
| <span id="msiRunModeAdvertise"></span><span id="msirunmodeadvertise"></span><span id="MSIRUNMODEADVERTISE"></span><dl> <span data-ttu-id="9004e-121"><dt>**msiRunModeAdvertise**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-121"><dt>**msiRunModeAdvertise**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="9004e-122">Annunciare la modalità di installazione.</span><span class="sxs-lookup"><span data-stu-id="9004e-122">Advertise mode of install.</span></span><br/>                                                          |
| <span id="msiRunModeMaintenance"></span><span id="msirunmodemaintenance"></span><span id="MSIRUNMODEMAINTENANCE"></span><dl> <span data-ttu-id="9004e-123"><dt>**msiRunModeMaintenance**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-123"><dt>**msiRunModeMaintenance**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="9004e-124">Database in modalità manutenzione caricato.</span><span class="sxs-lookup"><span data-stu-id="9004e-124">Maintenance mode database loaded.</span></span><br/>                                                   |
| <span id="msiRunModeRollbackEnabled"></span><span id="msirunmoderollbackenabled"></span><span id="MSIRUNMODEROLLBACKENABLED"></span><dl> <span data-ttu-id="9004e-125"><dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-125"><dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt></span></span> </dl>      | <span data-ttu-id="9004e-126">Il rollback è abilitato.</span><span class="sxs-lookup"><span data-stu-id="9004e-126">Rollback is enabled.</span></span><br/>                                                                |
| <span id="msiRunModeLogEnabled"></span><span id="msirunmodelogenabled"></span><span id="MSIRUNMODELOGENABLED"></span><dl> <span data-ttu-id="9004e-127"><dt>**msiRunModeLogEnabled**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-127"><dt>**msiRunModeLogEnabled**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="9004e-128">Il file di log è attivo.</span><span class="sxs-lookup"><span data-stu-id="9004e-128">Log file is active.</span></span><br/>                                                                 |
| <span id="msiRunModeOperations"></span><span id="msirunmodeoperations"></span><span id="MSIRUNMODEOPERATIONS"></span><dl> <span data-ttu-id="9004e-129"><dt>**msiRunModeOperations**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-129"><dt>**msiRunModeOperations**</dt> <dt>5</dt></span></span> </dl>                          | <span data-ttu-id="9004e-130">Esecuzione o spooling delle operazioni.</span><span class="sxs-lookup"><span data-stu-id="9004e-130">Executing or spooling operations.</span></span><br/>                                                   |
| <span id="msiRunModeRebootAtEnd"></span><span id="msirunmoderebootatend"></span><span id="MSIRUNMODEREBOOTATEND"></span><dl> <span data-ttu-id="9004e-131"><dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-131"><dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt></span></span> </dl>                      | <span data-ttu-id="9004e-132">È necessario riavviare il computer (impostabile).</span><span class="sxs-lookup"><span data-stu-id="9004e-132">Reboot is needed (settable).</span></span><br/>                                                        |
| <span id="msiRunModeRebootNow"></span><span id="msirunmoderebootnow"></span><span id="MSIRUNMODEREBOOTNOW"></span><dl> <span data-ttu-id="9004e-133"><dt>**msiRunModeRebootNow**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-133"><dt>**msiRunModeRebootNow**</dt> <dt>7</dt></span></span> </dl>                              | <span data-ttu-id="9004e-134">Per continuare l'installazione è necessario riavviare il computer (impostabile).</span><span class="sxs-lookup"><span data-stu-id="9004e-134">Reboot is needed to continue installation (settable).</span></span><br/>                               |
| <span id="msiRunModeCabinet"></span><span id="msirunmodecabinet"></span><span id="MSIRUNMODECABINET"></span><dl> <span data-ttu-id="9004e-135"><dt>**msiRunModeCabinet**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-135"><dt>**msiRunModeCabinet**</dt> <dt>8</dt></span></span> </dl>                                      | <span data-ttu-id="9004e-136">Installazione di file da file CAB e file con la tabella media.</span><span class="sxs-lookup"><span data-stu-id="9004e-136">Installing files from cabinets and files using Media table.</span></span><br/>                         |
| <span id="msiRunModeSourceShortNames"></span><span id="msirunmodesourceshortnames"></span><span id="MSIRUNMODESOURCESHORTNAMES"></span><dl> <span data-ttu-id="9004e-137"><dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-137"><dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt></span></span> </dl>  | <span data-ttu-id="9004e-138">I file di origine utilizzano solo nomi di file brevi.</span><span class="sxs-lookup"><span data-stu-id="9004e-138">Source files use only short file names.</span></span><br/>                                             |
| <span id="msiRunModeTargetShortNames"></span><span id="msirunmodetargetshortnames"></span><span id="MSIRUNMODETARGETSHORTNAMES"></span><dl> <span data-ttu-id="9004e-139"><dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-139"><dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="9004e-140">I file di destinazione devono usare solo nomi di file brevi.</span><span class="sxs-lookup"><span data-stu-id="9004e-140">Target files are to use only short file names.</span></span><br/>                                      |
| <span id="msiRunModeWindows9x"></span><span id="msirunmodewindows9x"></span><span id="MSIRUNMODEWINDOWS9X"></span><dl> <span data-ttu-id="9004e-141"><dt>**msiRunModeWindows9x**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-141"><dt>**msiRunModeWindows9x**</dt> <dt>12</dt></span></span> </dl>                             | <span data-ttu-id="9004e-142">Il sistema operativo è Windows 98/95.</span><span class="sxs-lookup"><span data-stu-id="9004e-142">Operating system is Windows 98/95.</span></span><br/>                                                  |
| <span id="msiRunModeZawEnabled"></span><span id="msirunmodezawenabled"></span><span id="MSIRUNMODEZAWENABLED"></span><dl> <span data-ttu-id="9004e-143"><dt>**msiRunModeZawEnabled**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-143"><dt>**msiRunModeZawEnabled**</dt> <dt>13</dt></span></span> </dl>                         | <span data-ttu-id="9004e-144">Il sistema operativo supporta la pubblicità di prodotti.</span><span class="sxs-lookup"><span data-stu-id="9004e-144">Operating system supports advertising of products.</span></span><br/>                                  |
| <span id="msiRunModeScheduled"></span><span id="msirunmodescheduled"></span><span id="MSIRUNMODESCHEDULED"></span><dl> <span data-ttu-id="9004e-145"><dt>**msiRunModeScheduled**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-145"><dt>**msiRunModeScheduled**</dt> <dt>16</dt></span></span> </dl>                             | <span data-ttu-id="9004e-146">[Azione personalizzata](custom-actions.md) posticipata chiamata dall'esecuzione dello script di installazione.</span><span class="sxs-lookup"><span data-stu-id="9004e-146">Deferred [custom action](custom-actions.md) called from install script execution.</span></span><br/>  |
| <span id="msiRunModeRollback"></span><span id="msirunmoderollback"></span><span id="MSIRUNMODEROLLBACK"></span><dl> <span data-ttu-id="9004e-147"><dt>**msiRunModeRollback**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-147"><dt>**msiRunModeRollback**</dt> <dt>17</dt></span></span> </dl>                                 | <span data-ttu-id="9004e-148">[Azione personalizzata](custom-actions.md) posticipata chiamata dallo script di esecuzione del rollback.</span><span class="sxs-lookup"><span data-stu-id="9004e-148">Deferred [custom action](custom-actions.md) called from rollback execution script.</span></span><br/> |
| <span id="msiRunModeCommit"></span><span id="msirunmodecommit"></span><span id="MSIRUNMODECOMMIT"></span><dl> <span data-ttu-id="9004e-149"><dt>**msiRunModeCommit**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="9004e-149"><dt>**msiRunModeCommit**</dt> <dt>18</dt></span></span> </dl>                                         | <span data-ttu-id="9004e-150">[Azione personalizzata](custom-actions.md) posticipata chiamata dallo script di esecuzione del commit.</span><span class="sxs-lookup"><span data-stu-id="9004e-150">Deferred [custom action](custom-actions.md) called from commit execution script.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="9004e-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9004e-151">Requirements</span></span>



| <span data-ttu-id="9004e-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="9004e-152">Requirement</span></span> | <span data-ttu-id="9004e-153">Valore</span><span class="sxs-lookup"><span data-stu-id="9004e-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9004e-154">Versione</span><span class="sxs-lookup"><span data-stu-id="9004e-154">Version</span></span><br/> | <span data-ttu-id="9004e-155">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9004e-155">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9004e-156">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9004e-156">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9004e-157">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="9004e-157">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



 

 




