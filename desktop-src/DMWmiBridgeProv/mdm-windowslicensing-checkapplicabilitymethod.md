---
title: Metodo CheckApplicabilityMethod della MDM_WindowsLicensing classe
description: Controlla se il codice Product Key immesso può essere usato per un aggiornamento dell'edizione, l'attivazione o la modifica di un codice Product Key Windows 10 per dispositivi desktop. Vedere anche CheckApplicability.
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- Metodo CheckApplicabilityMethod
- Metodo CheckApplicabilityMethod, MDM_WindowsLicensing classe
- MDM_WindowsLicensing classe, metodo CheckApplicabilityMethod
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
ms.openlocfilehash: db236e05ffe7b5b6273e7cba594266c31720932b43a7df2de751a0fa66cced5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750151"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a>Metodo CheckApplicabilityMethod della classe \_ MDM WindowsLicensing

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Controlla se il codice Product Key immesso può essere usato per un aggiornamento dell'edizione, l'attivazione o la modifica di un codice Product Key Windows 10 per dispositivi desktop. Vedere anche [CheckApplicability.](/windows/client-management/mdm/windowslicensing-csp)

## <a name="syntax"></a>Sintassi


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*param* \[ Pollici\]
</dt> <dd>

Codice Product Key.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

TRUE o FALSE

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Windows MDMLicensing**](mdm-windowslicensing.md)
</dt> <dt>

[Uso di script di PowerShell con il provider Bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

