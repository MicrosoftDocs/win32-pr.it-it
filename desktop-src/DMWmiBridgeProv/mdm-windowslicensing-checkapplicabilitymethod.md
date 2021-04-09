---
title: Metodo CheckApplicabilityMethod della classe MDM_WindowsLicensing
description: Verifica se il codice Product Key immesso può essere usato per l'aggiornamento di un'edizione, l'attivazione o la modifica di un codice Product Key di Windows 10 per i dispositivi desktop. Vedere anche CheckApplicability.
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- Metodo CheckApplicabilityMethod
- Metodo CheckApplicabilityMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, metodo CheckApplicabilityMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.CheckApplicabilityMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae08c4a13d036a7d1185a3d53dee846ea460e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120611"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a>Metodo CheckApplicabilityMethod della classe MDM \_ WindowsLicensing

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Verifica se il codice Product Key immesso può essere usato per l'aggiornamento di un'edizione, l'attivazione o la modifica di un codice Product Key di Windows 10 per i dispositivi desktop. Vedere anche [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).

## <a name="syntax"></a>Sintassi


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*param* \[ in\]
</dt> <dd>

Codice Product Key.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

TRUE o FALSE

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | \\ \\ Dmmap MDM CIMV2 \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_WINDOWSLICENSING MDM**](mdm-windowslicensing.md)
</dt> <dt>

[Utilizzo di script di PowerShell con il provider del Bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

