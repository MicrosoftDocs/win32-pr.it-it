---
description: Richiede un'operazione TPM che richiede la presenza fisica.
ms.assetid: e71eb6ab-b6ab-4586-8999-0a464f11047a
title: Metodo SetPhysicalPresenceRequest della Win32_Tpm classe
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
ms.openlocfilehash: 9c1b1e2760ed5015b6b682b94bd364e469edb4ed519adc371e2c348a0bf8c607
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891356"
---
# <a name="setphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Metodo SetPhysicalPresenceRequest della classe \_ Win32 Tpm

Il **metodo SetPhysicalPresenceRequest** della classe [**\_ Win32 Tpm**](win32-tpm.md) richiede un'operazione TPM che richiede la presenza fisica. Dopo aver usato questo metodo per inviare una richiesta, applicare il passaggio successivo indicato nel [**metodo GetPhysicalPresenceTransition.**](getphysicalpresencetransition-win32-tpm.md) Usare infine il metodo [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) per verificare se l'operazione è stata eseguita correttamente. Questo metodo sospende BitLocker se la chiamata di potrebbe causare la necessità del ripristino di BitLocker. BitLocker riprenderà automaticamente dopo il provisioning del TPM.

Questi passaggi sono necessari perché le operazioni di presenza fisica possono essere eseguite solo dopo che il computer ha rilevato l'utente fisicamente presente.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetPhysicalPresenceRequest(
  [in] uint32 Request
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Richiesta* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Valore intero che specifica l'operazione TPM richiesta che richiede la presenza fisica.



| Valore                                                                                                                               | Significato                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                                                        | Nessuna richiesta.<br/> Usare questo valore per cancellare una richiesta in sospeso.<br/>                                                                                                                                                                                                                                |
| <dl> <dt>1</dt> </dl>                                                        | Abilitare il TPM.<br/> Questa operazione viene inversa dall'operazione 2.<br/> Per altre informazioni, vedere i metodi correlati seguenti che non implicano la presenza fisica: [**Enable**](enable-win32-tpm.md) e [**IsEnabled.**](isenabled-win32-tpm.md)<br/>                                 |
| <dl> <dt>2</dt> </dl>                                                        | Disabilitare il TPM.<br/> Questa operazione viene inversa dall'operazione 1.<br/> Per altre informazioni, vedere il metodo correlato seguente che non implica la presenza fisica: [**Disabilitare**](disable-win32-tpm.md).<br/>                                                                          |
| <dl> <dt>3</dt> </dl>                                                        | Attivare il TPM.<br/> Questa operazione viene inversa dall'operazione 4.<br/>                                                                                                                                                                                                                          |
| <dl> <dt>4</dt> </dl>                                                        | Disattivare il TPM.<br/> Questa operazione viene inversa dall'operazione 3.<br/>                                                                                                                                                                                                                        |
| <dl> <dt>5</dt> </dl>                                                        | Cancellare il TPM.<br/> Questa operazione non può essere annullata.<br/> Per altre informazioni, vedere il metodo correlato seguente che non implica la presenza fisica: [**Clear**](clear-win32-tpm.md).<br/>                                                                                        |
| <dl> <dt>6</dt> </dl>                                                        | Abilitare e attivare il TPM.<br/> Questa operazione viene inversa dall'operazione 7.<br/>                                                                                                                                                                                                               |
| <dl> <dt>7</dt> </dl>                                                        | Disattivare e disabilitare il TPM.<br/> Questa operazione viene inversa dall'operazione 6.<br/>                                                                                                                                                                                                            |
| <dl> <dt>8</dt> </dl>                                                        | Consente l'installazione di un proprietario del TPM.<br/> Questa operazione viene inversa dall'operazione 9.<br/>                                                                                                                                                                                                     |
| <dl> <dt>9</dt> </dl>                                                        | Impedire l'installazione di un proprietario del TPM.<br/> Questa operazione viene inversa dall'operazione 8. <br/>                                                                                                                                                                                                  |
| <dl> <dt>10</dt> </dl>                                                       | Abilitare, attivare e consentire l'installazione di un proprietario del TPM.<br/> Questa operazione viene inversa dall'operazione 11.<br/>                                                                                                                                                                              |
| <dl> <dt>11</dt> </dl>                                                       | Disattivare, disabilitare e impedire l'installazione di un proprietario del TPM.<br/> Questa operazione viene inversa dall'operazione 10.<br/>                                                                                                                                                                         |
| <dl> <dt></dt><dt>12</dt> </dl> | Presenza fisica posticipataunownedFieldUpgrade<br/> L'impostazione della presenza fisica è stata aggiornata.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Questo valore non è supportato.<br/>                                                                       |
| <dl> <dt>14</dt> </dl>                                                       | Cancellare, abilitare e attivare il TPM.<br/> Questa operazione non può essere annullata.<br/>                                                                                                                                                                                                               |
| <dl> <dt>15</dt> </dl>                                                       | SetNoPPIProvision \_ False<br/> Imposta il provisioning che deve essere fisicamente presente per impostare il TPM.<br/> Questa operazione viene inversa dall'operazione 16.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Questo valore non è supportato.<br/>         |
| <dl> <dt>16</dt> </dl>                                                       | SetNoPPIProvision \_ True<br/> Imposta il provisioning che non è necessario avere fisicamente per impostare il TPM.<br/> Questa operazione viene inversa dall'operazione 15.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Questo valore non è supportato.<br/> |
| <dl> <dt>17</dt> </dl>                                                       | SetNoPPIClear \_ False<br/> Imposta il provisioning che deve essere fisicamente presente per cancellare il TPM.<br/> Questa operazione viene inversa dall'operazione 18.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Questo valore non è supportato.<br/>           |
| <dl> <dt>18</dt> </dl>                                                       | SetNoPPIClear \_ True<br/> Imposta il provisioning che non è necessario presenza fisica per cancellare il TPM.<br/> Questa operazione viene inversa dall'operazione 17.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Questo valore non è supportato.<br/>   |
| <dl> <dt>19</dt> </dl>                                                       | SetNoPPIMaintenance \_ False<br/> Imposta il provisioning che è necessario essere fisicamente presenti per mantenere il TPM.<br/> Questa operazione viene inversa dall'operazione 20.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Questo valore non è supportato.<br/>  |
| <dl> <dt>20</dt> </dl>                                                       | SetNoPPIMaintenance \_ True<br/> Imposta il provisioning che non è necessario avere fisicamente per mantenere il TPM.<br/> Questa operazione viene inversa dall'operazione 19.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Questo valore non è supportato.<br/>   |
| <dl> <dt>21</dt> </dl>                                                       | Abilita + Attiva + Cancella<br/> Abilitare, attivare e cancellare il TPM.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Questo valore non è supportato.<br/>                                                                                                  |
| <dl> <dt>22</dt> </dl>                                                       | Enable + Activate + Clear + Enable + Activate<br/> Abilitare, attivare e cancellare il TPM, quindi abilitare e riattivare il TPM.<br/> **Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:** Questo valore non è supportato.<br/>                                      |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi di base TPM.



| Codice/valore restituito                                                                                                                                                                       | Descrizione                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                       | Il metodo è stato eseguito correttamente.<br/> Usare [**il metodo GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md) per determinare il passaggio successivo necessario.<br/>                                                  |
| <dl> <dt>**TPM \_ E \_ PPI \_ NOT \_ SUPPORTED**</dt> <dt>2150171395 (0x80290303)</dt> </dl> | Il computer non supporta le operazioni di presenza fisica TPM tramite questo metodo.<br/> Per altre informazioni, vedere il produttore del computer. Il BIOS del computer potrebbe avere un supporto alternativo per la configurazione del TPM.<br/> |
| <dl> <dt>**TPM \_ Errore \_ E PPI \_ ACPI \_**</dt> 2150171392 <dt>(0x80290300)</dt> </dl>  | Si è verificato un errore hardware.<br/> Per altre informazioni, vedere il produttore del computer.<br/>                                                                                                                                  |



 

## <a name="remarks"></a>Commenti

Le operazioni di presenza fisica TPM non richiedono l'autorizzazione del proprietario TPM. Tuttavia, richiedono passaggi aggiuntivi per proteggere da modifiche non autorizzate al TPM.

I computer che supportano le operazioni di presenza fisica TPM tenteranno di rilevare l'utente fisicamente presente prima di eseguire l'operazione. Anche se i computer possono differire per il modo in cui viene eseguito questo rilevamento, l'idea è quella di fare in modo che un utente o un amministratore presenti fisicamente autorizzi l'operazione.

Ad esempio, il computer potrebbe richiedere all'utente di riavviare il computer. Dopo il riavvio del computer, il computer può visualizzare una finestra di dialogo di conferma del BIOS che consente all'utente di confermare l'operazione usando la tastiera.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

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

[**Abilita**](enable-win32-tpm.md)
</dt> <dt>

[**IsEnabled**](isenabled-win32-tpm.md)
</dt> <dt>

[**Disabilita**](disable-win32-tpm.md)
</dt> <dt>

[**Cancella**](clear-win32-tpm.md)
</dt> </dl>

 

 
