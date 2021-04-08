---
description: Indica se è richiesta la conferma da un utente fisicamente presente per una determinata operazione di presenza fisica.
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: 'Metodo Win32_Tpm:: GetPhysicalPresenceConfirmationStatus'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceConfirmationStatus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 61dc2798973a82cfc75c803f2bf8307c8a43b3c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967874"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a>\_Metodo Win32 TPM:: GetPhysicalPresenceConfirmationStatus

Indica se è richiesta la conferma da un utente fisicamente presente per una determinata operazione di presenza fisica.

Questo metodo è accessibile solo agli amministratori locali.

## <a name="syntax"></a>Sintassi


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Operazione* \[ di in\]
</dt> <dd>

Valore intero che specifica l'operazione TPM richiesta che richiede la presenza fisica. Sono supportati anche i comandi specifici del fornitore.

Il parametro *Operation* può essere costituito dai valori seguenti.



| Valore                                                                                                                               | Significato                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>1</dt> </dl>                                                        | Abilitare<br/>                                        |
| <dl> <dt>2</dt> </dl>                                                        | Disabilita<br/>                                       |
| <dl> <dt>3</dt> </dl>                                                        | Activate<br/>                                      |
| <dl> <dt>4</dt> </dl>                                                        | Disattivare<br/>                                    |
| <dl> <dt>5</dt> </dl>                                                        | Cancella<br/>                                         |
| <dl> <dt>6</dt> </dl>                                                        | Abilita + attiva<br/>                             |
| <dl> <dt>7</dt> </dl>                                                        | Disattiva + Disabilita<br/>                          |
| <dl> <dt>8</dt> </dl>                                                        | SetOwnerInstall \_ true<br/>                         |
| <dl> <dt>9</dt> </dl>                                                        | SetOwnerInstall \_ false<br/>                        |
| <dl> <dt>10</dt> </dl>                                                       | Enable + Activate + SetOwnerInstall \_ true<br/>     |
| <dl> <dt>11</dt> </dl>                                                       | SetOwnerInstall \_ false + disattiva + Disabilita<br/> |
| <dl> <dt></dt><dt>12</dt> </dl> | PresenceunownedFieldUpgrade fisico posticipato<br/> |
| <dl> <dt></dt><dt>14</dt> </dl> | Deselezionare + Abilita + attiva<br/>                     |
| <dl> <dt>15</dt> </dl>                                                       | SetNoPPIProvision \_ false<br/>                      |
| <dl> <dt>16</dt> </dl>                                                       | SetNoPPIProvision \_ true<br/>                       |
| <dl> <dt>17</dt> </dl>                                                       | SetNoPPIClear \_ false<br/>                          |
| <dl> <dt>18</dt> </dl>                                                       | SetNoPPIClear \_ true<br/>                           |
| <dl> <dt>19</dt> </dl>                                                       | SetNoPPIMaintenance \_ false<br/>                    |
| <dl> <dt>20</dt> </dl>                                                       | SetNoPPIMaintenance \_ true<br/>                     |
| <dl> <dt>21</dt> </dl>                                                       | Abilita + attiva + Cancella<br/>                     |
| <dl> <dt>22</dt> </dl>                                                       | Abilita + attiva + Cancella + Abilita + attiva<br/> |



 

</dd> <dt>

*ConfirmationStatus* \[ out\]
</dt> <dd>

Restituisce lo stato di conferma per il comando presenza fisica.

Il parametro *ConfirmationStatus* può essere costituito dai valori seguenti.



| Valore                                                                        | Significato                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Non implementato<br/>                                             |
| <dl> <dt>1</dt> </dl> | Solo BIOS.<br/>                                                  |
| <dl> <dt>2</dt> </dl> | Bloccato per il sistema operativo dalla configurazione del BIOS.<br/> |
| <dl> <dt>3</dt> </dl> | È necessario che l'utente sia consentito e fisicamente presente.<br/>               |
| <dl> <dt>4</dt> </dl> | Utenti consentiti e fisicamente presenti non necessari<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile restituire tutti gli errori del TPM, nonché gli errori specifici [dei servizi di base TPM](../tbs/tbs-return-codes.md) .

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non sono installati come parte del Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                      |
| Spazio dei nomi<br/>                | \\\\.\\ radice \\ CIMV2 \\ sicurezza \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>\_TPM Win32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TPM Win32**](win32-tpm.md)
</dt> </dl>

 

 
