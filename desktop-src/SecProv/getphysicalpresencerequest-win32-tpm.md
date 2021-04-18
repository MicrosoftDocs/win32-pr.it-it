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
# <a name="getphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Metodo GetPhysicalPresenceRequest della \_ classe TPM Win32

Il metodo **GetPhysicalPresenceRequest** della classe [**\_ TPM Win32**](win32-tpm.md) restituisce l'operazione di presenza fisica del TPM in sospeso. Usare il metodo [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) per richiedere un'operazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetPhysicalPresenceRequest(
  [out] uint32 Request
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Richiesta* \[ out\]
</dt> <dd>

Tipo: **UInt32**

Valore che specifica l'operazione di presenza fisica del TPM in sospeso.



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
<td>Nessuna richiesta.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>1</dt> </dl></td>
<td>Abilitare il TPM.<br/> Questa operazione è invertita dall'operazione 2. <br/> Per ulteriori informazioni, vedere questi metodi correlati che non coinvolgono la presenza fisica:
<ul>
<li><a href="enable-win32-tpm.md"><strong>Abilitare</strong></a></li>
<li><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>2</dt> </dl></td>
<td>Disabilitare il TPM.<br/> Questa operazione è stata annullata dall'operazione 1. <br/> Per ulteriori informazioni, vedere questo metodo correlato che non implica la presenza fisica: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>3</dt> </dl></td>
<td>Attivare il TPM.<br/> Questa operazione è invertita dall'operazione 4.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>4</dt> </dl></td>
<td>Disattivare il TPM.<br/> Questa operazione è invertita dall'operazione 3.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>5</dt> </dl></td>
<td>Cancellare il TPM.<br/> Questa operazione non può essere annullata.<br/> Per ulteriori informazioni, vedere questo metodo correlato che non implica la presenza fisica: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>6</dt> </dl></td>
<td>Abilitare e attivare il TPM. <br/> Questa operazione è invertita dall'operazione 7.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>7</dt> </dl></td>
<td>Disattivare e disabilitare il TPM.<br/> Questa operazione è invertita dall'operazione 6. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>8</dt> </dl></td>
<td>Consente l'installazione di un proprietario del TPM. <br/> Questa operazione è invertita dall'operazione 9.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>9</dt> </dl></td>
<td>Impedire l'installazione di un proprietario del TPM.<br/> Questa operazione è invertita dall'operazione 8. <br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>10</dt> </dl></td>
<td>Abilitare, attivare e consentire l'installazione di un proprietario del TPM.<br/> Questa operazione è stata annullata dall'operazione 11.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>11</dt> </dl></td>
<td>Disattiva, Disabilita e impedisce l'installazione di un proprietario del TPM.<br/> Questa operazione è invertita dall'operazione 10.<br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <dt><strong></strong></dt><dt>12</dt> </dl></td>
<td>PresenceunownedFieldUpgrade fisico posticipato<br/> L'impostazione di presenza fisica è stata aggiornata.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>14</dt> </dl></td>
<td>Deselezionare, abilitare e attivare il TPM.<br/> Questa operazione non può essere annullata.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>15</dt> </dl></td>
<td>SetNoPPIProvision_False<br/> Imposta il provisioning che deve essere fisicamente presente per impostare il TPM.<br/> Questa operazione è invertita dall'operazione 16.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>16</dt> </dl></td>
<td>SetNoPPIProvision_True<br/> Imposta il provisioning che non è necessario essere fisicamente presente per impostare il TPM.<br/> Questa operazione è invertita dall'operazione 15.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>17</dt> </dl></td>
<td>SetNoPPIClear_False<br/> Imposta il provisioning che deve essere fisicamente presente per cancellare il TPM.<br/> Questa operazione è invertita dall'operazione 18.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>18</dt> </dl></td>
<td>SetNoPPIClear_True<br/> Imposta il provisioning che non è necessario essere fisicamente presente per cancellare il TPM.<br/> Questa operazione è invertita dall'operazione 17.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>19</dt> </dl></td>
<td>SetNoPPIMaintenance_False<br/> Imposta il provisioning che deve essere fisicamente presente per gestire il TPM.<br/> Questa operazione è invertita dall'operazione 20.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>20</dt> </dl></td>
<td>SetNoPPIMaintenance_True<br/> Imposta il provisioning che deve essere fisicamente presente per gestire il TPM.<br/> Questa operazione è invertita dall'operazione 19.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt>21</dt> </dl></td>
<td>Abilita + attiva + Cancella<br/> Abilitare, attivare e cancellare il TPM.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt>22</dt> </dl></td>
<td>Abilita + attiva + Cancella + Abilita + attiva<br/> Abilitare, attivare e cancellare il TPM, quindi abilitare e riattivare il TPM.<br/> <strong>Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:</strong> Questo valore non è supportato.<br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.

Nella tabella seguente sono elencati i codici restituiti comuni.



| Codice/valore restituito                                                                                                                                                                      | Descrizione                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                      | Il metodo è stato eseguito correttamente.<br/>                                                            |
| <dl> <dt>**TPM \_ \_ \_ \_ Errore ACPI di E PPI**</dt> <dt>2150171392 (0x80290300)</dt> </dl> | Si è verificato un errore hardware. Per ulteriori informazioni, consultare il produttore del computer.<br/> |



 

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM Win32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> <dt>

[**Deselezionare**](clear-win32-tpm.md)
</dt> <dt>

[**Disabilita**](disable-win32-tpm.md)
</dt> <dt>

[**Abilitare**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
