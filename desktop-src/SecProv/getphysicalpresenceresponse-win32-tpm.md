---
description: Restituisce i risultati di un'operazione di presenza fisica TPM eseguita.
ms.assetid: 28d76149-3905-45db-a41e-32fac1603582
title: Metodo GetPhysicalPresenceResponse della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceResponse
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 47dfad1491b398b035e40867d10d2d3e46327dd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306393"
---
# <a name="getphysicalpresenceresponse-method-of-the-win32_tpm-class"></a><span data-ttu-id="67782-103">Metodo GetPhysicalPresenceResponse della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="67782-103">GetPhysicalPresenceResponse method of the Win32\_Tpm class</span></span>

<span data-ttu-id="67782-104">Il metodo **GetPhysicalPresenceResponse** della classe [**\_ TPM Win32**](win32-tpm.md) restituisce i risultati di un'operazione di presenza fisica TPM eseguita.</span><span class="sxs-lookup"><span data-stu-id="67782-104">The **GetPhysicalPresenceResponse** method of the [**Win32\_Tpm**](win32-tpm.md) class returns the results from a TPM physical presence operation that was performed.</span></span> <span data-ttu-id="67782-105">Usare il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) per richiedere un'operazione.</span><span class="sxs-lookup"><span data-stu-id="67782-105">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="67782-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="67782-106">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceResponse(
  [out] uint32 Request,
  [out] uint32 Response
);
```



## <a name="parameters"></a><span data-ttu-id="67782-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="67782-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67782-108">*Richiesta* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="67782-108">*Request* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67782-109">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67782-109">Type: **uint32**</span></span>

<span data-ttu-id="67782-110">Valore intero che specifica l'operazione di presenza fisica TPM eseguita.</span><span class="sxs-lookup"><span data-stu-id="67782-110">An integer value that specifies the TPM physical presence operation that was performed.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="67782-111">Valore</span><span class="sxs-lookup"><span data-stu-id="67782-111">Value</span></span></th>
<th><span data-ttu-id="67782-112">Significato</span><span class="sxs-lookup"><span data-stu-id="67782-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="67782-113"><dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-113"><dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-114">Nessuna richiesta.</span><span class="sxs-lookup"><span data-stu-id="67782-114">No request.</span></span><br/> <span data-ttu-id="67782-115">Non è stata eseguita alcuna operazione di presenza fisica.</span><span class="sxs-lookup"><span data-stu-id="67782-115">No physical presence operation was performed.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="67782-116"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-116"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-117">Abilitare il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-117">Enable the TPM.</span></span><br/> <span data-ttu-id="67782-118">Questa operazione è invertita dall'operazione 2.</span><span class="sxs-lookup"><span data-stu-id="67782-118">This operation is reversed by operation 2.</span></span> <br/> <span data-ttu-id="67782-119">Per ulteriori informazioni, vedere questi metodi correlati che non coinvolgono la presenza fisica:</span><span class="sxs-lookup"><span data-stu-id="67782-119">For more information, see these related methods that do not involve physical presence:</span></span>
<ul>
<li><span data-ttu-id="67782-120"><a href="enable-win32-tpm.md"><strong>Abilitare</strong></a></span><span class="sxs-lookup"><span data-stu-id="67782-120"><a href="enable-win32-tpm.md"><strong>Enable</strong></a></span></span></li>
<li><span data-ttu-id="67782-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="67782-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="67782-122"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-122"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-123">Disabilitare il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-123">Disable the TPM.</span></span><br/> <span data-ttu-id="67782-124">Questa operazione è stata annullata dall'operazione 1.</span><span class="sxs-lookup"><span data-stu-id="67782-124">This operation is reversed by operation 1.</span></span> <br/> <span data-ttu-id="67782-125">Per ulteriori informazioni, vedere questo metodo correlato che non implica la presenza fisica: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="67782-125">For more information, see this related method that does not involve physical presence: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="67782-126"><dt>3</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-126"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-127">Attivare il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-127">Activate the TPM.</span></span><br/> <span data-ttu-id="67782-128">Questa operazione è invertita dall'operazione 4.</span><span class="sxs-lookup"><span data-stu-id="67782-128">This operation is reversed by operation 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="67782-129"><dt>4</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-129"><dt>4</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-130">Disattivare il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-130">Deactivate the TPM.</span></span><br/> <span data-ttu-id="67782-131">Questa operazione è invertita dall'operazione 3.</span><span class="sxs-lookup"><span data-stu-id="67782-131">This operation is reversed by operation 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="67782-132"><dt>5</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-132"><dt>5</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-133">Cancellare il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-133">Clear the TPM.</span></span><br/> <span data-ttu-id="67782-134">Questa operazione non può essere annullata.</span><span class="sxs-lookup"><span data-stu-id="67782-134">This operation cannot be reversed.</span></span> <br/> <span data-ttu-id="67782-135">Per ulteriori informazioni, vedere questo metodo correlato che non implica la presenza fisica: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="67782-135">For more information, see this related method that does not involve physical presence: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="67782-136"><dt>6</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-136"><dt>6</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-137">Abilitare e attivare il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-137">Enable and activate the TPM.</span></span><br/> <span data-ttu-id="67782-138">Questa operazione è invertita dall'operazione 7.</span><span class="sxs-lookup"><span data-stu-id="67782-138">This operation is reversed by operation 7.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="67782-139"><dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-139"><dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-140">Disattivare e disabilitare il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-140">Deactivate and disable the TPM.</span></span><br/> <span data-ttu-id="67782-141">Questa operazione è invertita dall'operazione 6.</span><span class="sxs-lookup"><span data-stu-id="67782-141">This operation is reversed by operation 6.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="67782-142"><dt>8</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-142"><dt>8</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-143">Consente l'installazione di un proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-143">Allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="67782-144">Questa operazione è invertita dall'operazione 9.</span><span class="sxs-lookup"><span data-stu-id="67782-144">This operation is reversed by operation 9.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="67782-145"><dt>9</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-145"><dt>9</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-146">Impedire l'installazione di un proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-146">Prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="67782-147">Questa operazione è invertita dall'operazione 8.</span><span class="sxs-lookup"><span data-stu-id="67782-147">This operation is reversed by operation 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="67782-148"><dt>10</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-148"><dt>10</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-149">Abilitare, attivare e consentire l'installazione di un proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-149">Enable, activate, and allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="67782-150">Questa operazione è stata annullata dall'operazione 11.</span><span class="sxs-lookup"><span data-stu-id="67782-150">This operation is reversed by operation 11.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="67782-151"><dt>11</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-151"><dt>11</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-152">Disattiva, Disabilita e impedisce l'installazione di un proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-152">Deactivate, disable, and prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="67782-153">Questa operazione è invertita dall'operazione 10.</span><span class="sxs-lookup"><span data-stu-id="67782-153">This operation is reversed by operation 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <span data-ttu-id="67782-154"><dt><strong></strong></dt><dt>12</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-154"><dt><strong></strong></dt> <dt>12</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-155">PresenceunownedFieldUpgrade fisico posticipato</span><span class="sxs-lookup"><span data-stu-id="67782-155">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> <span data-ttu-id="67782-156">L'impostazione di presenza fisica è stata aggiornata.</span><span class="sxs-lookup"><span data-stu-id="67782-156">Physical presence setting has been updated.</span></span><br/> <span data-ttu-id="67782-157"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="67782-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="67782-158"><dt>14</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-158"><dt>14</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-159">Deselezionare, abilitare e attivare il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-159">Clear, enable, and activate the TPM.</span></span><br/> <span data-ttu-id="67782-160">Questa operazione non può essere annullata.</span><span class="sxs-lookup"><span data-stu-id="67782-160">This operation cannot be reversed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="67782-161"><dt>15</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-161"><dt>15</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-162">SetNoPPIProvision_False</span><span class="sxs-lookup"><span data-stu-id="67782-162">SetNoPPIProvision_False</span></span><br/> <span data-ttu-id="67782-163">Imposta il provisioning che deve essere fisicamente presente per impostare il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-163">Sets the provision that you must be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="67782-164">Questa operazione è invertita dall'operazione 16.</span><span class="sxs-lookup"><span data-stu-id="67782-164">This operation is reversed by operation 16.</span></span><br/> <span data-ttu-id="67782-165"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="67782-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="67782-166"><dt>16</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-166"><dt>16</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-167">SetNoPPIProvision_True</span><span class="sxs-lookup"><span data-stu-id="67782-167">SetNoPPIProvision_True</span></span><br/> <span data-ttu-id="67782-168">Imposta il provisioning che non è necessario essere fisicamente presente per impostare il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-168">Sets the provision that you don't need to be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="67782-169">Questa operazione è invertita dall'operazione 15.</span><span class="sxs-lookup"><span data-stu-id="67782-169">This operation is reversed by operation 15.</span></span><br/> <span data-ttu-id="67782-170"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="67782-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="67782-171"><dt>17</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-171"><dt>17</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-172">SetNoPPIClear_False</span><span class="sxs-lookup"><span data-stu-id="67782-172">SetNoPPIClear_False</span></span><br/> <span data-ttu-id="67782-173">Imposta il provisioning che deve essere fisicamente presente per cancellare il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-173">Sets the provision that you must be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="67782-174">Questa operazione è invertita dall'operazione 18.</span><span class="sxs-lookup"><span data-stu-id="67782-174">This operation is reversed by operation 18.</span></span><br/> <span data-ttu-id="67782-175"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="67782-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="67782-176"><dt>18</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-176"><dt>18</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-177">SetNoPPIClear_True</span><span class="sxs-lookup"><span data-stu-id="67782-177">SetNoPPIClear_True</span></span><br/> <span data-ttu-id="67782-178">Imposta il provisioning che non è necessario essere fisicamente presente per cancellare il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-178">Sets the provision that you don't need to be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="67782-179">Questa operazione è invertita dall'operazione 17.</span><span class="sxs-lookup"><span data-stu-id="67782-179">This operation is reversed by operation 17.</span></span><br/> <span data-ttu-id="67782-180"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="67782-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="67782-181"><dt>19</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-181"><dt>19</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-182">SetNoPPIMaintenance_False</span><span class="sxs-lookup"><span data-stu-id="67782-182">SetNoPPIMaintenance_False</span></span><br/> <span data-ttu-id="67782-183">Imposta il provisioning che deve essere fisicamente presente per gestire il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-183">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="67782-184">Questa operazione è invertita dall'operazione 20.</span><span class="sxs-lookup"><span data-stu-id="67782-184">This operation is reversed by operation 20.</span></span><br/> <span data-ttu-id="67782-185"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="67782-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="67782-186"><dt>20</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-186"><dt>20</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-187">SetNoPPIMaintenance_True</span><span class="sxs-lookup"><span data-stu-id="67782-187">SetNoPPIMaintenance_True</span></span><br/> <span data-ttu-id="67782-188">Imposta il provisioning che deve essere fisicamente presente per gestire il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-188">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="67782-189">Questa operazione è invertita dall'operazione 19.</span><span class="sxs-lookup"><span data-stu-id="67782-189">This operation is reversed by operation 19.</span></span><br/> <span data-ttu-id="67782-190"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="67782-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="67782-191"><dt>21</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-191"><dt>21</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-192">Abilita + attiva + Cancella</span><span class="sxs-lookup"><span data-stu-id="67782-192">Enable + Activate + Clear</span></span><br/> <span data-ttu-id="67782-193">Abilitare, attivare e cancellare il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-193">Enable, activate, and clear the TPM.</span></span><br/> <span data-ttu-id="67782-194"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="67782-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="67782-195"><dt>22</dt> </span><span class="sxs-lookup"><span data-stu-id="67782-195"><dt>22</dt> </span></span></dl></td>
<td><span data-ttu-id="67782-196">Abilita + attiva + Cancella + Abilita + attiva</span><span class="sxs-lookup"><span data-stu-id="67782-196">Enable + Activate + Clear + Enable + Activate</span></span><br/> <span data-ttu-id="67782-197">Abilitare, attivare e cancellare il TPM, quindi abilitare e riattivare il TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-197">Enable, activate, and clear the TPM, and then enable and reactivate the TPM.</span></span><br/> <span data-ttu-id="67782-198"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="67782-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="67782-199">*Risposta* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="67782-199">*Response* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67782-200">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67782-200">Type: **uint32**</span></span>

<span data-ttu-id="67782-201">Valore intero che specifica i risultati dell'esecuzione dell'operazione di presenza fisica del TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-201">An integer value that specifies the results of performing the TPM physical presence operation.</span></span>

<span data-ttu-id="67782-202">Un'operazione di presenza fisica ha esito positivo se un utente fisicamente presente conferma l'operazione e se l'operazione viene eseguita senza errori.</span><span class="sxs-lookup"><span data-stu-id="67782-202">A physical presence operation is successful if a physically present user confirms the operation and if the operation runs without errors.</span></span>

<span data-ttu-id="67782-203">Questo valore può contenere qualsiasi errore TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-203">This value may contain any TPM error.</span></span> <span data-ttu-id="67782-204">Nella tabella seguente sono elencate alcune delle risposte di errore comuni.</span><span class="sxs-lookup"><span data-stu-id="67782-204">The following table lists some of the common error responses.</span></span>



| <span data-ttu-id="67782-205">Valore</span><span class="sxs-lookup"><span data-stu-id="67782-205">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="67782-206">Significato</span><span class="sxs-lookup"><span data-stu-id="67782-206">Meaning</span></span>                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="67782-207"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="67782-207"><dt>0</dt></span></span> </dl>                                                                                                                                                                                             | <span data-ttu-id="67782-208">L'operazione TPM richiesta è stata completata.</span><span class="sxs-lookup"><span data-stu-id="67782-208">The requested TPM operation was successful.</span></span><br/>              |
| <span id="TPM_E_PPI_USER_ABORT"></span><span id="tpm_e_ppi_user_abort"></span><dl> <span data-ttu-id="67782-209"><dt>**TPM \_ E l'utente di E- \_ PPI \_ \_ interrompe**</dt> <dt>2150171393 (0x80290301)</dt></span><span class="sxs-lookup"><span data-stu-id="67782-209"><dt>**TPM\_E\_PPI\_USER\_ABORT**</dt> <dt>2150171393 (0x80290301)</dt></span></span> </dl>       | <span data-ttu-id="67782-210">L'utente ha rifiutato l'operazione TPM richiesta.</span><span class="sxs-lookup"><span data-stu-id="67782-210">The user rejected the requested TPM operation.</span></span><br/>           |
| <span id="TPM_E_PPI_BIOS_FAILURE"></span><span id="tpm_e_ppi_bios_failure"></span><dl> <span data-ttu-id="67782-211"><dt>**TPM \_ \_Errore del \_ BIOS \_ di E PPI**</dt> <dt>2150171394 (0x80290302)</dt></span><span class="sxs-lookup"><span data-stu-id="67782-211"><dt>**TPM\_E\_PPI\_BIOS\_FAILURE**</dt> <dt>2150171394 (0x80290302)</dt></span></span> </dl> | <span data-ttu-id="67782-212">Si è verificato un errore del BIOS durante l'esecuzione dell'operazione TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-212">A BIOS failure occurred while running the TPM operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67782-213">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="67782-213">Return value</span></span>

<span data-ttu-id="67782-214">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="67782-214">Type: **uint32**</span></span>

<span data-ttu-id="67782-215">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="67782-215">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="67782-216">Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.</span><span class="sxs-lookup"><span data-stu-id="67782-216">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="67782-217">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="67782-217">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="67782-218">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67782-218">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="67782-219"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="67782-219"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="67782-220">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="67782-220">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="67782-221"><dt>**TPM \_ \_ \_ \_ Errore ACPI di E PPI**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="67782-221"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="67782-222">Si è verificato un errore hardware.</span><span class="sxs-lookup"><span data-stu-id="67782-222">A hardware failure occurred.</span></span> <span data-ttu-id="67782-223">Per ulteriori informazioni, consultare il produttore del computer.</span><span class="sxs-lookup"><span data-stu-id="67782-223">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="67782-224">Commenti</span><span class="sxs-lookup"><span data-stu-id="67782-224">Remarks</span></span>

<span data-ttu-id="67782-225">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="67782-225">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="67782-226">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="67782-226">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="67782-227">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="67782-227">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="67782-228">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="67782-228">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67782-229">Requisiti</span><span class="sxs-lookup"><span data-stu-id="67782-229">Requirements</span></span>



| <span data-ttu-id="67782-230">Requisito</span><span class="sxs-lookup"><span data-stu-id="67782-230">Requirement</span></span> | <span data-ttu-id="67782-231">Valore</span><span class="sxs-lookup"><span data-stu-id="67782-231">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="67782-232">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67782-232">Minimum supported client</span></span><br/> | <span data-ttu-id="67782-233">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="67782-233">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="67782-234">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="67782-234">Minimum supported server</span></span><br/> | <span data-ttu-id="67782-235">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="67782-235">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="67782-236">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="67782-236">Namespace</span></span><br/>                | <span data-ttu-id="67782-237">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="67782-237">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="67782-238">MOF</span><span class="sxs-lookup"><span data-stu-id="67782-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67782-239"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67782-239"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="67782-240">DLL</span><span class="sxs-lookup"><span data-stu-id="67782-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67782-241"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="67782-241"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67782-242">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="67782-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67782-243">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="67782-243">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="67782-244">**Deselezionare**</span><span class="sxs-lookup"><span data-stu-id="67782-244">**Clear**</span></span>](clear-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="67782-245">**Disabilita**</span><span class="sxs-lookup"><span data-stu-id="67782-245">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="67782-246">**Abilitare**</span><span class="sxs-lookup"><span data-stu-id="67782-246">**Enable**</span></span>](enable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="67782-247">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="67782-247">**IsEnabled**</span></span>](isenabled-win32-tpm.md)
</dt> </dl>

 

 
