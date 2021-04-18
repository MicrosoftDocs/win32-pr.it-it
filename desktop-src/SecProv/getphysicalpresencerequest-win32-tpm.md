---
description: Restituisce l'operazione di presenza fisica TPM in sospeso. Usare il metodo SetPhysicalPresenceRequest per richiedere un'operazione.
ms.assetid: c50378ae-b465-4c82-beb9-8ecb7939dae2
title: Metodo GetPhysicalPresenceRequest della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8d631aabfc1e2df15aa4182b8332091fe503f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316105"
---
# <a name="getphysicalpresencerequest-method-of-the-win32_tpm-class"></a><span data-ttu-id="5ba5d-104">Metodo GetPhysicalPresenceRequest della \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="5ba5d-104">GetPhysicalPresenceRequest method of the Win32\_Tpm class</span></span>

<span data-ttu-id="5ba5d-105">Il metodo **GetPhysicalPresenceRequest** della classe [**\_ TPM Win32**](win32-tpm.md) restituisce l'operazione di presenza fisica del TPM in sospeso.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-105">The **GetPhysicalPresenceRequest** method of the [**Win32\_Tpm**](win32-tpm.md) class returns the pending TPM physical presence operation.</span></span> <span data-ttu-id="5ba5d-106">Usare il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) per richiedere un'operazione.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-106">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ba5d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ba5d-107">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceRequest(
  [out] uint32 Request
);
```



## <a name="parameters"></a><span data-ttu-id="5ba5d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5ba5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ba5d-109">*Richiesta* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5ba5d-109">*Request* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ba5d-110">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5ba5d-110">Type: **uint32**</span></span>

<span data-ttu-id="5ba5d-111">Valore che specifica l'operazione di presenza fisica del TPM in sospeso.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-111">A value that specifies the pending TPM physical presence operation.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ba5d-112">Valore</span><span class="sxs-lookup"><span data-stu-id="5ba5d-112">Value</span></span></th>
<th><span data-ttu-id="5ba5d-113">Significato</span><span class="sxs-lookup"><span data-stu-id="5ba5d-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="5ba5d-114"><dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-114"><dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-115">Nessuna richiesta.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-115">No request.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="5ba5d-116"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-116"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-117">Abilitare il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-117">Enable the TPM.</span></span><br/> <span data-ttu-id="5ba5d-118">Questa operazione è invertita dall'operazione 2.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-118">This operation is reversed by operation 2.</span></span> <br/> <span data-ttu-id="5ba5d-119">Per ulteriori informazioni, vedere questi metodi correlati che non coinvolgono la presenza fisica:</span><span class="sxs-lookup"><span data-stu-id="5ba5d-119">For more information, see these related methods that do not involve physical presence:</span></span>
<ul>
<li><span data-ttu-id="5ba5d-120"><a href="enable-win32-tpm.md"><strong>Abilitare</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ba5d-120"><a href="enable-win32-tpm.md"><strong>Enable</strong></a></span></span></li>
<li><span data-ttu-id="5ba5d-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="5ba5d-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="5ba5d-122"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-122"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-123">Disabilitare il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-123">Disable the TPM.</span></span><br/> <span data-ttu-id="5ba5d-124">Questa operazione è stata annullata dall'operazione 1.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-124">This operation is reversed by operation 1.</span></span> <br/> <span data-ttu-id="5ba5d-125">Per ulteriori informazioni, vedere questo metodo correlato che non implica la presenza fisica: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-125">For more information, see this related method that does not involve physical presence: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="5ba5d-126"><dt>3</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-126"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-127">Attivare il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-127">Activate the TPM.</span></span><br/> <span data-ttu-id="5ba5d-128">Questa operazione è invertita dall'operazione 4.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-128">This operation is reversed by operation 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="5ba5d-129"><dt>4</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-129"><dt>4</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-130">Disattivare il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-130">Deactivate the TPM.</span></span><br/> <span data-ttu-id="5ba5d-131">Questa operazione è invertita dall'operazione 3.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-131">This operation is reversed by operation 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="5ba5d-132"><dt>5</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-132"><dt>5</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-133">Cancellare il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-133">Clear the TPM.</span></span><br/> <span data-ttu-id="5ba5d-134">Questa operazione non può essere annullata.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-134">This operation cannot be reversed.</span></span><br/> <span data-ttu-id="5ba5d-135">Per ulteriori informazioni, vedere questo metodo correlato che non implica la presenza fisica: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-135">For more information, see this related method that does not involve physical presence: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="5ba5d-136"><dt>6</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-136"><dt>6</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-137">Abilitare e attivare il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-137">Enable and activate the TPM.</span></span> <br/> <span data-ttu-id="5ba5d-138">Questa operazione è invertita dall'operazione 7.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-138">This operation is reversed by operation 7.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="5ba5d-139"><dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-139"><dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-140">Disattivare e disabilitare il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-140">Deactivate and disable the TPM.</span></span><br/> <span data-ttu-id="5ba5d-141">Questa operazione è invertita dall'operazione 6.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-141">This operation is reversed by operation 6.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="5ba5d-142"><dt>8</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-142"><dt>8</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-143">Consente l'installazione di un proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-143">Allow the installation of a TPM owner.</span></span> <br/> <span data-ttu-id="5ba5d-144">Questa operazione è invertita dall'operazione 9.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-144">This operation is reversed by operation 9.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="5ba5d-145"><dt>9</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-145"><dt>9</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-146">Impedire l'installazione di un proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-146">Prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="5ba5d-147">Questa operazione è invertita dall'operazione 8.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-147">This operation is reversed by operation 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="5ba5d-148"><dt>10</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-148"><dt>10</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-149">Abilitare, attivare e consentire l'installazione di un proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-149">Enable, activate, and allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="5ba5d-150">Questa operazione è stata annullata dall'operazione 11.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-150">This operation is reversed by operation 11.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="5ba5d-151"><dt>11</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-151"><dt>11</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-152">Disattiva, Disabilita e impedisce l'installazione di un proprietario del TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-152">Deactivate, disable, and prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="5ba5d-153">Questa operazione è invertita dall'operazione 10.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-153">This operation is reversed by operation 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <span data-ttu-id="5ba5d-154"><dt><strong></strong></dt><dt>12</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-154"><dt><strong></strong></dt> <dt>12</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-155">PresenceunownedFieldUpgrade fisico posticipato</span><span class="sxs-lookup"><span data-stu-id="5ba5d-155">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> <span data-ttu-id="5ba5d-156">L'impostazione di presenza fisica è stata aggiornata.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-156">Physical presence setting has been updated.</span></span><br/> <span data-ttu-id="5ba5d-157"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="5ba5d-158"><dt>14</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-158"><dt>14</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-159">Deselezionare, abilitare e attivare il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-159">Clear, enable, and activate the TPM.</span></span><br/> <span data-ttu-id="5ba5d-160">Questa operazione non può essere annullata.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-160">This operation cannot be reversed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="5ba5d-161"><dt>15</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-161"><dt>15</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-162">SetNoPPIProvision_False</span><span class="sxs-lookup"><span data-stu-id="5ba5d-162">SetNoPPIProvision_False</span></span><br/> <span data-ttu-id="5ba5d-163">Imposta il provisioning che deve essere fisicamente presente per impostare il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-163">Sets the provision that you must be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="5ba5d-164">Questa operazione è invertita dall'operazione 16.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-164">This operation is reversed by operation 16.</span></span><br/> <span data-ttu-id="5ba5d-165"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="5ba5d-166"><dt>16</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-166"><dt>16</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-167">SetNoPPIProvision_True</span><span class="sxs-lookup"><span data-stu-id="5ba5d-167">SetNoPPIProvision_True</span></span><br/> <span data-ttu-id="5ba5d-168">Imposta il provisioning che non è necessario essere fisicamente presente per impostare il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-168">Sets the provision that you don't need to be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="5ba5d-169">Questa operazione è invertita dall'operazione 15.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-169">This operation is reversed by operation 15.</span></span><br/> <span data-ttu-id="5ba5d-170"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="5ba5d-171"><dt>17</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-171"><dt>17</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-172">SetNoPPIClear_False</span><span class="sxs-lookup"><span data-stu-id="5ba5d-172">SetNoPPIClear_False</span></span><br/> <span data-ttu-id="5ba5d-173">Imposta il provisioning che deve essere fisicamente presente per cancellare il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-173">Sets the provision that you must be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="5ba5d-174">Questa operazione è invertita dall'operazione 18.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-174">This operation is reversed by operation 18.</span></span><br/> <span data-ttu-id="5ba5d-175"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="5ba5d-176"><dt>18</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-176"><dt>18</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-177">SetNoPPIClear_True</span><span class="sxs-lookup"><span data-stu-id="5ba5d-177">SetNoPPIClear_True</span></span><br/> <span data-ttu-id="5ba5d-178">Imposta il provisioning che non è necessario essere fisicamente presente per cancellare il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-178">Sets the provision that you don't need to be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="5ba5d-179">Questa operazione è invertita dall'operazione 17.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-179">This operation is reversed by operation 17.</span></span><br/> <span data-ttu-id="5ba5d-180"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="5ba5d-181"><dt>19</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-181"><dt>19</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-182">SetNoPPIMaintenance_False</span><span class="sxs-lookup"><span data-stu-id="5ba5d-182">SetNoPPIMaintenance_False</span></span><br/> <span data-ttu-id="5ba5d-183">Imposta il provisioning che deve essere fisicamente presente per gestire il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-183">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="5ba5d-184">Questa operazione è invertita dall'operazione 20.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-184">This operation is reversed by operation 20.</span></span><br/> <span data-ttu-id="5ba5d-185"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="5ba5d-186"><dt>20</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-186"><dt>20</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-187">SetNoPPIMaintenance_True</span><span class="sxs-lookup"><span data-stu-id="5ba5d-187">SetNoPPIMaintenance_True</span></span><br/> <span data-ttu-id="5ba5d-188">Imposta il provisioning che deve essere fisicamente presente per gestire il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-188">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="5ba5d-189">Questa operazione è invertita dall'operazione 19.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-189">This operation is reversed by operation 19.</span></span><br/> <span data-ttu-id="5ba5d-190"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="5ba5d-191"><dt>21</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-191"><dt>21</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-192">Abilita + attiva + Cancella</span><span class="sxs-lookup"><span data-stu-id="5ba5d-192">Enable + Activate + Clear</span></span><br/> <span data-ttu-id="5ba5d-193">Abilitare, attivare e cancellare il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-193">Enable, activate, and clear the TPM.</span></span><br/> <span data-ttu-id="5ba5d-194"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="5ba5d-195"><dt>22</dt> </span><span class="sxs-lookup"><span data-stu-id="5ba5d-195"><dt>22</dt> </span></span></dl></td>
<td><span data-ttu-id="5ba5d-196">Abilita + attiva + Cancella + Abilita + attiva</span><span class="sxs-lookup"><span data-stu-id="5ba5d-196">Enable + Activate + Clear + Enable + Activate</span></span><br/> <span data-ttu-id="5ba5d-197">Abilitare, attivare e cancellare il TPM, quindi abilitare e riattivare il TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-197">Enable, activate, and clear the TPM, and then enable and reactivate the TPM.</span></span><br/> <span data-ttu-id="5ba5d-198"><strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ba5d-199">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ba5d-199">Return value</span></span>

<span data-ttu-id="5ba5d-200">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5ba5d-200">Type: **uint32**</span></span>

<span data-ttu-id="5ba5d-201">È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-201">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="5ba5d-202">Nella tabella seguente sono elencati i codici restituiti comuni.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-202">The following table lists the common return codes.</span></span>



| <span data-ttu-id="5ba5d-203">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="5ba5d-203">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="5ba5d-204">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ba5d-204">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ba5d-205"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5ba5d-205"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="5ba5d-206">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-206">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="5ba5d-207"><dt>**TPM \_ \_ \_ \_ Errore ACPI di E PPI**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="5ba5d-207"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="5ba5d-208">Si è verificato un errore hardware.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-208">A hardware failure occurred.</span></span> <span data-ttu-id="5ba5d-209">Per ulteriori informazioni, consultare il produttore del computer.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-209">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5ba5d-210">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ba5d-210">Remarks</span></span>

<span data-ttu-id="5ba5d-211">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="5ba5d-211">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5ba5d-212">I file MOF non sono installati come parte del Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-212">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5ba5d-213">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="5ba5d-213">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5ba5d-214">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5ba5d-214">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ba5d-215">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ba5d-215">Requirements</span></span>



| <span data-ttu-id="5ba5d-216">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ba5d-216">Requirement</span></span> | <span data-ttu-id="5ba5d-217">Valore</span><span class="sxs-lookup"><span data-stu-id="5ba5d-217">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ba5d-218">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ba5d-218">Minimum supported client</span></span><br/> | <span data-ttu-id="5ba5d-219">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ba5d-219">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5ba5d-220">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ba5d-220">Minimum supported server</span></span><br/> | <span data-ttu-id="5ba5d-221">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5ba5d-221">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5ba5d-222">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5ba5d-222">Namespace</span></span><br/>                | <span data-ttu-id="5ba5d-223">Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="5ba5d-223">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="5ba5d-224">MOF</span><span class="sxs-lookup"><span data-stu-id="5ba5d-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ba5d-225"><dt>\_TPM Win32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ba5d-225"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ba5d-226">DLL</span><span class="sxs-lookup"><span data-stu-id="5ba5d-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ba5d-227"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="5ba5d-227"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ba5d-228">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ba5d-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ba5d-229">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="5ba5d-229">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="5ba5d-230">**Deselezionare**</span><span class="sxs-lookup"><span data-stu-id="5ba5d-230">**Clear**</span></span>](clear-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="5ba5d-231">**Disabilita**</span><span class="sxs-lookup"><span data-stu-id="5ba5d-231">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="5ba5d-232">**Abilitare**</span><span class="sxs-lookup"><span data-stu-id="5ba5d-232">**Enable**</span></span>](enable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="5ba5d-233">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5ba5d-233">**IsEnabled**</span></span>](isenabled-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="5ba5d-234">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="5ba5d-234">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
