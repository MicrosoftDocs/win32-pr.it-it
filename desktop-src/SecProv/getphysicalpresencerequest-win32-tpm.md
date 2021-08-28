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
ms.openlocfilehash: 7d88ec523e983e60cacab57b41307381b05e8de6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481867"
---
# <a name="getphysicalpresencerequest-method-of-the-win32_tpm-class"></a>Metodo GetPhysicalPresenceRequest della classe Tpm Win32 \_

Il **metodo GetPhysicalPresenceRequest** della [**classe \_ Tpm Win32**](win32-tpm.md) restituisce l'operazione di presenza fisica TPM in sospeso. Usare il [**metodo SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) per richiedere un'operazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetPhysicalPresenceRequest(
  [out] uint32 Request
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Richiesta* \[ Cambio\]
</dt> <dd>

Tipo: **uint32**

Valore che specifica l'operazione di presenza fisica TPM in sospeso.




| valore | Significato | 
|-------|---------|
| <dl><dt>0</dt></dl> | Nessuna richiesta.<br /> | 
| <dl><dt>1</dt></dl> | Abilitare il TPM.<br /> Questa operazione viene inversata dall'operazione 2. <br /> Per altre informazioni, vedere i metodi correlati che non comportano la presenza fisica:<ul><li><a href="enable-win32-tpm.md"><strong>Abilita</strong></a></li><li><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></li></ul><br /> | 
| <dl><dt>2</dt></dl> | Disabilitare il TPM.<br /> Questa operazione viene inversata dall'operazione 1. <br /> Per altre informazioni, vedere questo metodo correlato che non comporta la presenza fisica: <a href="disable-win32-tpm.md"><strong>Disabilitare</strong></a>.<br /> | 
| <dl><dt>3</dt></dl> | Attivare il TPM.<br /> Questa operazione viene inversata dall'operazione 4.<br /> | 
| <dl><dt>4</dt></dl> | Disattivare il TPM.<br /> Questa operazione viene inversata dall'operazione 3.<br /> | 
| <dl><dt>5</dt></dl> | Cancellare il TPM.<br /> Questa operazione non può essere annullata.<br /> Per altre informazioni, vedere questo metodo correlato che non comporta la presenza fisica: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.<br /> | 
| <dl><dt>6</dt></dl> | Abilitare e attivare il TPM. <br /> Questa operazione viene inversata dall'operazione 7.<br /> | 
| <dl><dt>7</dt></dl> | Disattivare e disabilitare il TPM.<br /> Questa operazione viene inversata dall'operazione 6. <br /> | 
| <dl><dt>8</dt></dl> | Consentire l'installazione di un proprietario TPM. <br /> Questa operazione viene inversata dall'operazione 9.<br /> | 
| <dl><dt>9</dt></dl> | Impedire l'installazione di un proprietario del TPM.<br /> Questa operazione viene inversata dall'operazione 8. <br /> | 
| <dl><dt>10</dt></dl> | Abilitare, attivare e consentire l'installazione di un proprietario TPM.<br /> Questa operazione viene inversata dall'operazione 11.<br /> | 
| <dl><dt>11</dt></dl> | Disattivare, disabilitare e impedire l'installazione di un proprietario TPM.<br /> Questa operazione viene inversata dall'operazione 10.<br /> | 
| <span></span><dl><dt><strong></strong></dt><dt>12</dt></dl> | Presenza fisica posticipataunownedFieldUpgrade<br /> L'impostazione presenza fisica è stata aggiornata.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br /> | 
| <dl><dt>14</dt></dl> | Deselezionare, abilitare e attivare il TPM.<br /> Questa operazione non può essere annullata.<br /> | 
| <dl><dt>15</dt></dl> | SetNoPPIProvision_False<br /> Imposta il provisioning che deve essere fisicamente presente per impostare il TPM.<br /> Questa operazione viene inversata dall'operazione 16.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br /> | 
| <dl><dt>16</dt></dl> | SetNoPPIProvision_True<br /> Imposta il provisioning che non è necessario essere fisicamente presenti per impostare il TPM.<br /> Questa operazione viene inversata dall'operazione 15.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br /> | 
| <dl><dt>17</dt></dl> | SetNoPPIClear_False<br /> Imposta il provisioning che deve essere fisicamente presente per cancellare il TPM.<br /> Questa operazione viene inversata dall'operazione 18.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br /> | 
| <dl><dt>18</dt></dl> | SetNoPPIClear_True<br /> Imposta il provisioning che non è necessario essere fisicamente presenti per cancellare il TPM.<br /> Questa operazione viene inversata dall'operazione 17.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br /> | 
| <dl><dt>19</dt></dl> | SetNoPPIMaintenance_False<br /> Imposta il provisioning che deve essere fisicamente presente per mantenere il TPM.<br /> Questa operazione viene inversata dall'operazione 20.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br /> | 
| <dl><dt>20</dt></dl> | SetNoPPIMaintenance_True<br /> Imposta il provisioning che deve essere fisicamente presente per mantenere il TPM.<br /> Questa operazione viene inversata dall'operazione 19.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br /> | 
| <dl><dt>21</dt></dl> | Abilita + Attiva + Cancella<br /> Abilitare, attivare e cancellare il TPM.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br /> | 
| <dl><dt>22</dt></dl> | Abilita + Attiva + Cancella + Abilita + Attiva<br /> Abilitare, attivare e cancellare il TPM, quindi abilitare e riattivare il TPM.<br /><strong>Windows 7, Windows Server 2008 R2, Windows Vista e Windows Server 2008:</strong> Questo valore non è supportato.<br /> | 




 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi di base TPM.

Nella tabella seguente sono elencati i codici restituiti comuni.



| Codice/valore restituito                                                                                                                                                                      | Descrizione                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                      | Il metodo è stato eseguito correttamente.<br/>                                                            |
| <dl> <dt>**TPM \_ Errore \_ E PPI \_ ACPI \_**</dt> 2150171392 <dt>(0x80290300)</dt> </dl> | Si è verificato un errore hardware. Per altre informazioni, vedere il produttore del computer.<br/> |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows wmi (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | valore |
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
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
