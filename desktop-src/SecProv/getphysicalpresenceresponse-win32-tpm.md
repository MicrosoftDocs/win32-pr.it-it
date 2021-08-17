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
ms.openlocfilehash: 5f32379c9e0f538c2f9be4466b55158d0abcdd51a4d2612634b2b03ff869ed41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891861"
---
# <a name="getphysicalpresenceresponse-method-of-the-win32_tpm-class"></a>Metodo GetPhysicalPresenceResponse della classe Tpm Win32 \_

Il **metodo GetPhysicalPresenceResponse** della classe [**\_ Win32 Tpm**](win32-tpm.md) restituisce i risultati di un'operazione di presenza fisica TPM eseguita. Usare il [**metodo SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) per richiedere un'operazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetPhysicalPresenceResponse(
  [out] uint32 Request,
  [out] uint32 Response
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Richiesta* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Valore intero che specifica l'operazione di presenza fisica TPM eseguita.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valore</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt>0</dt> </dl></td>
<td>Nessuna richiesta.<br/> Non è stata eseguita alcuna operazione di presenza fisica.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>1</dt> </dl></td>
<td>Abilitare il TPM.<br/> Questa operazione viene inversata dall'operazione 2. <br/> Per altre informazioni, vedere questi metodi correlati che non comportano la presenza fisica:
<ul>
<li><a href="enable-win32-tpm.md"><strong>Abilita</strong></a></li>
<li><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>2</dt> </dl></td>
<td>Disabilitare il TPM.<br/> Questa operazione viene inversata dall'operazione 1. <br/> Per altre informazioni, vedere questo metodo correlato che non comporta la presenza fisica: <a href="disable-win32-tpm.md"><strong>Disabilitare</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>3</dt> </dl></td>
<td>Attivare il TPM.<br/> Questa operazione viene inversata dall'operazione 4.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>4</dt> </dl></td>
<td>Disattivare il TPM.<br/> Questa operazione viene inversata dall'operazione 3.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>5</dt> </dl></td>
<td>Cancellare il TPM.<br/> Questa operazione non può essere annullata. <br/> Per altre informazioni, vedere questo metodo correlato che non implica la presenza fisica: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>6</dt> </dl></td>
<td>Abilitare e attivare il TPM.<br/> Questa operazione viene inversata dall'operazione 7.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>7</dt> </dl></td>
<td>Disattivare e disabilitare il TPM.<br/> Questa operazione viene inversata dall'operazione 6. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>8</dt> </dl></td>
<td>Consentire l'installazione di un proprietario TPM.<br/> Questa operazione viene inversata dall'operazione 9.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>9</dt> </dl></td>
<td>Impedire l'installazione di un proprietario TPM.<br/> Questa operazione viene inversata dall'operazione 8. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>10</dt> </dl></td>
<td>Abilitare, attivare e consentire l'installazione di un proprietario TPM.<br/> Questa operazione viene inversata dall'operazione 11.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>11</dt> </dl></td>
<td>Disattivare, disabilitare ed impedire l'installazione di un proprietario TPM.<br/> Questa operazione viene inversata dall'operazione 10.<br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <dt><strong></strong></dt><dt>12</dt> </dl></td>
<td>Presenza fisica posticipataunownedFieldUpgrade<br/> L'impostazione presenza fisica è stata aggiornata.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>14</dt> </dl></td>
<td>Cancellare, abilitare e attivare il TPM.<br/> Questa operazione non può essere annullata.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>15</dt> </dl></td>
<td>SetNoPPIProvision_False<br/> Imposta il provisioning che deve essere fisicamente presente per impostare il TPM.<br/> Questa operazione viene inversata dall'operazione 16.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>16</dt> </dl></td>
<td>SetNoPPIProvision_True<br/> Imposta il provisioning che non è necessario essere fisicamente presenti per impostare il TPM.<br/> Questa operazione viene inversata dall'operazione 15.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>17</dt> </dl></td>
<td>SetNoPPIClear_False<br/> Imposta il provisioning che deve essere fisicamente presente per cancellare il TPM.<br/> Questa operazione viene inversata dall'operazione 18.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>18</dt> </dl></td>
<td>SetNoPPIClear_True<br/> Imposta il provisioning che non è necessario essere fisicamente presenti per cancellare il TPM.<br/> Questa operazione viene inversata dall'operazione 17.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>19</dt> </dl></td>
<td>SetNoPPIMaintenance_False<br/> Imposta il provisioning che deve essere fisicamente presente per mantenere il TPM.<br/> Questa operazione viene inversata dall'operazione 20.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>20</dt> </dl></td>
<td>SetNoPPIMaintenance_True<br/> Imposta il provisioning che deve essere fisicamente presente per mantenere il TPM.<br/> Questa operazione viene inversata dall'operazione 19.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>21</dt> </dl></td>
<td>Abilita + Attiva + Cancella<br/> Abilitare, attivare e cancellare il TPM.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>22</dt> </dl></td>
<td>Abilita + Attiva + Cancella + Abilita + Attiva<br/> Abilitare, attivare e cancellare il TPM, quindi abilitare e riattivare il TPM.<br/> <strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*Risposta* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Valore intero che specifica i risultati dell'esecuzione dell'operazione di presenza fisica TPM.

Un'operazione di presenza fisica ha esito positivo se un utente fisicamente presente conferma l'operazione e se l'operazione viene eseguita senza errori.

Questo valore può contenere qualsiasi errore TPM. Nella tabella seguente sono elencate alcune delle risposte di errore comuni.



| Valore                                                                                                                                                                                                                                                                    | Significato                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                                                                                                                                                                                             | L'operazione TPM richiesta è stata completata.<br/>              |
| <span id="TPM_E_PPI_USER_ABORT"></span><span id="tpm_e_ppi_user_abort"></span><dl> <dt>**TPM \_ E \_ PPI \_ USER \_ ABORT**</dt> <dt>2150171393 (0x80290301)</dt> </dl>       | L'utente ha rifiutato l'operazione TPM richiesta.<br/>           |
| <span id="TPM_E_PPI_BIOS_FAILURE"></span><span id="tpm_e_ppi_bios_failure"></span><dl> <dt>**TPM \_ Errore \_ del \_ BIOS \_ E PPI**</dt> 2150171394 <dt>(0x80290302)</dt> </dl> | Si è verificato un errore del BIOS durante l'esecuzione dell'operazione TPM.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi di base TPM.

Nella tabella seguente sono elencati alcuni dei codici restituiti comuni.



| Codice/valore restituito                                                                                                                                                                      | Descrizione                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                      | Il metodo è stato eseguito correttamente.<br/>                                                            |
| <dl> <dt>**TPM \_ Errore \_ E PPI \_ ACPI \_**</dt> 2150171392 <dt>(0x80290300)</dt> </dl> | Si è verificato un errore hardware. Per altre informazioni, vedere il produttore del computer.<br/> |



 

## <a name="remarks"></a>Commenti

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                      |
| Spazio dei nomi<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> <dt>

[**Cancella**](clear-win32-tpm.md)
</dt> <dt>

[**Disabilita**](disable-win32-tpm.md)
</dt> <dt>

[**Abilita**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> </dl>

 

 
