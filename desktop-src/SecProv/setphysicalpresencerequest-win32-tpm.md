---
description: Richiede un'operazione TPM che richiede la presenza fisica.
ms.assetid: e71eb6ab-b6ab-4586-8999-0a464f11047a
title: Metodo SetPhysicalPresenceRequest della classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 55a0f8c5fc0a8573192f25e3901b63f24e05f7c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306373"
---
# <a name="setphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Metodo SetPhysicalPresenceRequest della \_ classe TPM Win32

Il metodo **SetPhysicalPresenceRequest** della classe [**\_ TPM Win32**](win32-tpm.md) richiede un'operazione TPM che richiede la presenza fisica. Dopo aver usato questo metodo per inviare una richiesta, applicare il passaggio successivo indicato nel metodo [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md) . Infine, utilizzare il metodo [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) per verificare se l'operazione è stata eseguita correttamente. Questo metodo sospende BitLocker se la chiamata a può causare la richiesta del ripristino BitLocker. BitLocker verrà ripreso automaticamente dopo il provisioning del TPM.

Questi passaggi sono necessari perché le operazioni di presenza fisica possono essere eseguite solo dopo che il computer ha rilevato l'utente fisicamente presente.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetPhysicalPresenceRequest(
  [in] uint32 Request
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Richiesta* \[ in\]
</dt> <dd>

Tipo: **UInt32**

Valore intero che specifica l'operazione TPM richiesta che richiede la presenza fisica.



| Valore                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                                                        | Nessuna richiesta.<br/> Utilizzare questo valore per cancellare una richiesta in sospeso.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>1</dt> </dl>                                                        | Abilitare il TPM.<br/> Questa operazione è invertita dall'operazione 2.<br/> Per ulteriori informazioni, vedere i metodi correlati seguenti che non coinvolgono la presenza fisica: [**Enable**](enable-win32-tpm.md) e [**IsEnabled**](isenabled-win32-tpm.md).<br/>                                 |
| <dl> <dt>2</dt> </dl>                                                        | Disabilitare il TPM.<br/> Questa operazione è stata annullata dall'operazione 1.<br/> Per ulteriori informazioni, vedere il metodo correlato seguente che non implica la presenza fisica: [**Disable**](disable-win32-tpm.md).<br/>                                                                          |
| <dl> <dt>3</dt> </dl>                                                        | Attivare il TPM.<br/> Questa operazione è invertita dall'operazione 4.<br/>                                                                                                                                                                                                                          |
| <dl> <dt>4</dt> </dl>                                                        | Disattivare il TPM.<br/> Questa operazione è invertita dall'operazione 3.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>5</dt> </dl>                                                        | Cancellare il TPM.<br/> Questa operazione non può essere annullata.<br/> Per ulteriori informazioni, vedere il metodo correlato seguente che non implica la presenza fisica: [**Clear**](clear-win32-tpm.md).<br/>                                                                                        |
| <dl> <dt>6</dt> </dl>                                                        | Abilitare e attivare il TPM.<br/> Questa operazione è invertita dall'operazione 7.<br/>                                                                                                                                                                                                               |
| <dl> <dt>7</dt> </dl>                                                        | Disattivare e disabilitare il TPM.<br/> Questa operazione è invertita dall'operazione 6.<br/>                                                                                                                                                                                                            |
| <dl> <dt>8</dt> </dl>                                                        | Consente l'installazione di un proprietario del TPM.<br/> Questa operazione è invertita dall'operazione 9.<br/>                                                                                                                                                                                                     |
| <dl> <dt>9</dt> </dl>                                                        | Impedire l'installazione di un proprietario del TPM.<br/> Questa operazione è invertita dall'operazione 8. <br/>                                                                                                                                                                                                  |
| <dl> <dt>10</dt> </dl>                                                       | Abilitare, attivare e consentire l'installazione di un proprietario del TPM.<br/> Questa operazione è stata annullata dall'operazione 11.<br/>                                                                                                                                                                              |
| <dl> <dt>11</dt> </dl>                                                       | Disattiva, Disabilita e impedisce l'installazione di un proprietario del TPM.<br/> Questa operazione è invertita dall'operazione 10.<br/>                                                                                                                                                                         |
| <dl> <dt></dt><dt>12</dt> </dl> | PresenceunownedFieldUpgrade fisico posticipato<br/> L'impostazione di presenza fisica è stata aggiornata.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questo valore non è supportato.<br/>                                                                       |
| <dl> <dt>14</dt> </dl>                                                       | Deselezionare, abilitare e attivare il TPM.<br/> Questa operazione non può essere annullata.<br/>                                                                                                                                                                                                               |
| <dl> <dt>15</dt> </dl>                                                       | SetNoPPIProvision \_ false<br/> Imposta il provisioning che deve essere fisicamente presente per impostare il TPM.<br/> Questa operazione è invertita dall'operazione 16.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questo valore non è supportato.<br/>         |
| <dl> <dt>16</dt> </dl>                                                       | SetNoPPIProvision \_ true<br/> Imposta il provisioning che non è necessario essere fisicamente presente per impostare il TPM.<br/> Questa operazione è invertita dall'operazione 15.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questo valore non è supportato.<br/> |
| <dl> <dt>17</dt> </dl>                                                       | SetNoPPIClear \_ false<br/> Imposta il provisioning che deve essere fisicamente presente per cancellare il TPM.<br/> Questa operazione è invertita dall'operazione 18.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questo valore non è supportato.<br/>           |
| <dl> <dt>18</dt> </dl>                                                       | SetNoPPIClear \_ true<br/> Imposta il provisioning che non è necessario essere fisicamente presente per cancellare il TPM.<br/> Questa operazione è invertita dall'operazione 17.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questo valore non è supportato.<br/>   |
| <dl> <dt>19</dt> </dl>                                                       | SetNoPPIMaintenance \_ false<br/> Imposta il provisioning che deve essere fisicamente presente per gestire il TPM.<br/> Questa operazione è invertita dall'operazione 20.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questo valore non è supportato.<br/>  |
| <dl> <dt>20</dt> </dl>                                                       | SetNoPPIMaintenance \_ true<br/> Imposta il provisioning che non è necessario essere fisicamente presente per gestire il TPM.<br/> Questa operazione è invertita dall'operazione 19.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questo valore non è supportato.<br/>   |
| <dl> <dt>21</dt> </dl>                                                       | Abilita + attiva + Cancella<br/> Abilitare, attivare e cancellare il TPM.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questo valore non è supportato.<br/>                                                                                                  |
| <dl> <dt>22</dt> </dl>                                                       | Abilita + attiva + Cancella + Abilita + attiva<br/> Abilitare, attivare e cancellare il TPM, quindi abilitare e riattivare il TPM.<br/> **Windows 7, Windows server 2008 R2, Windows Vista e Windows server 2008:** Questo valore non è supportato.<br/>                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici dei servizi di base TPM.



| Codice/valore restituito                                                                                                                                                                       | Descrizione                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | Il metodo è stato eseguito correttamente.<br/> Usare il metodo [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md) per determinare il passaggio successivo necessario.<br/>                                                  |
| <dl> <dt>**TPM \_ E \_ PPI \_ non \_ supportati**</dt> <dt>2150171395 (0x80290303)</dt> </dl> | Il computer non supporta le operazioni di presenza fisica TPM utilizzando questo metodo.<br/> Per ulteriori informazioni, consultare il produttore del computer. Il BIOS del computer potrebbe avere supporto alternativo per la configurazione del TPM.<br/> |
| <dl> <dt>**TPM \_ \_ \_ \_ Errore ACPI di E PPI**</dt> <dt>2150171392 (0x80290300)</dt> </dl>  | Si è verificato un errore hardware.<br/> Per ulteriori informazioni, consultare il produttore del computer.<br/>                                                                                                                                  |



 

## <a name="remarks"></a>Commenti

Le operazioni di presenza fisica TPM non richiedono l'autorizzazione del proprietario del TPM. Tuttavia, sono necessari passaggi aggiuntivi per facilitare la protezione da modifiche non autorizzate al TPM.

I computer che supportano le operazioni di presenza fisica TPM tenterà di rilevare l'utente fisicamente presente prima di eseguire l'operazione. Sebbene sia possibile che i computer differiscano dal modo in cui viene eseguito questo rilevamento, l'idea è avere un utente o un amministratore fisicamente presente per autorizzare l'operazione.

Ad esempio, il computer potrebbe richiedere all'utente di riavviare il computer. Al riavvio del computer, il computer può visualizzare una finestra di dialogo di conferma del BIOS che consente all'utente di confermare l'operazione utilizzando la tastiera.

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

[**Abilitare**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**Disabilita**](disable-win32-tpm.md)
</dt> <dt>

[**Deselezionare**](clear-win32-tpm.md)
</dt> </dl>

 

 
