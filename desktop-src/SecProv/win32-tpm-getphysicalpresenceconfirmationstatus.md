---
description: Indica se è necessaria la conferma da parte di un utente fisicamente presente per una determinata operazione di presenza fisica.
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: Win32_Tpm::GetPhysicalPresenceConfirmationStatus
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
ms.openlocfilehash: 8e48fc7506b6b8ba8218d23bdeba75e960f2e3beca68c3d0a95b2aa4ea3c05e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118890866"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a>Metodo \_ Win32 Tpm::GetPhysicalPresenceConfirmationStatus

Indica se è necessaria la conferma da parte di un utente fisicamente presente per una determinata operazione di presenza fisica.

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

*Operazione* \[ Pollici\]
</dt> <dd>

Valore intero che specifica l'operazione TPM richiesta che richiede la presenza fisica. Sono supportati anche i comandi specifici del fornitore.

Il *parametro Operation* può essere costituito da valori seguenti.



| Valore                                                                                                                               | Significato                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <dt>1</dt> </dl>                                                        | Abilita<br/>                                        |
| <dl> <dt>2</dt> </dl>                                                        | Disabilita<br/>                                       |
| <dl> <dt>3</dt> </dl>                                                        | Activate<br/>                                      |
| <dl> <dt>4</dt> </dl>                                                        | Disattivare<br/>                                    |
| <dl> <dt>5</dt> </dl>                                                        | Cancella<br/>                                         |
| <dl> <dt>6</dt> </dl>                                                        | Abilita + Attiva<br/>                             |
| <dl> <dt>7</dt> </dl>                                                        | Disattiva + Disabilita<br/>                          |
| <dl> <dt>8</dt> </dl>                                                        | SetOwnerInstall \_ True<br/>                         |
| <dl> <dt>9</dt> </dl>                                                        | SetOwnerInstall \_ False<br/>                        |
| <dl> <dt>10</dt> </dl>                                                       | Enable + Activate + SetOwnerInstall \_ True<br/>     |
| <dl> <dt>11</dt> </dl>                                                       | SetOwnerInstall \_ False + Disattiva + Disabilita<br/> |
| <dl> <dt></dt><dt>12</dt> </dl> | Presenza fisica posticipataunownedFieldUpgrade<br/> |
| <dl> <dt></dt><dt>14</dt> </dl> | Cancella + Abilita + Attiva<br/>                     |
| <dl> <dt>15</dt> </dl>                                                       | SetNoPPIProvision \_ False<br/>                      |
| <dl> <dt>16</dt> </dl>                                                       | SetNoPPIProvision \_ True<br/>                       |
| <dl> <dt>17</dt> </dl>                                                       | SetNoPPIClear \_ False<br/>                          |
| <dl> <dt>18</dt> </dl>                                                       | SetNoPPIClear \_ True<br/>                           |
| <dl> <dt>19</dt> </dl>                                                       | SetNoPPIMaintenance \_ False<br/>                    |
| <dl> <dt>20</dt> </dl>                                                       | SetNoPPIMaintenance \_ True<br/>                     |
| <dl> <dt>21</dt> </dl>                                                       | Abilita + Attiva + Cancella<br/>                     |
| <dl> <dt>22</dt> </dl>                                                       | Enable + Activate + Clear + Enable + Activate<br/> |



 

</dd> <dt>

*Stato di conferma* \[ Cambio\]
</dt> <dd>

Restituisce lo stato di conferma per il comando di presenza fisica.

Il *parametro ConfirmationStatus* può essere costituito da valori seguenti.



| Valore                                                                        | Significato                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Non implementato<br/>                                             |
| <dl> <dt>1</dt> </dl> | Solo BIOS.<br/>                                                  |
| <dl> <dt>2</dt> </dl> | Bloccato per il sistema operativo dalla configurazione del BIOS.<br/> |
| <dl> <dt>3</dt> </dl> | Utente consentito e fisicamente presente richiesto.<br/>               |
| <dl> <dt>4</dt> </dl> | Utente consentito e fisicamente presente non obbligatorio<br/>            |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile restituire tutti gli errori TPM e gli errori specifici dei servizi [di base TPM.](../tbs/tbs-return-codes.md)

I codici restituiti comuni sono elencati di seguito.



| Codice/valore restituito                                                                                                                                 | Descrizione                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | Il metodo è stato eseguito correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Windows SDK. Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                      |
| Spazio dei nomi<br/>                | \\\\.\\ Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                     |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> </dl>

 

 
