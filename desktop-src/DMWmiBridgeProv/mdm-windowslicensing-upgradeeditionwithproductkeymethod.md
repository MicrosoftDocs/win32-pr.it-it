---
title: Metodo UpgradeEditionWithProductKeyMethod della MDM_WindowsLicensing
description: Immette un codice Product Key per un aggiornamento dell'edizione Windows 10 dispositivi desktop. Vedere anche UpgradeEditionWithProductKey.
ms.assetid: 6576fb5c-210c-4979-8c01-ed8f78e72c2c
keywords:
- Metodo UpgradeEditionWithProductKeyMethod
- Metodo UpgradeEditionWithProductKeyMethod, MDM_WindowsLicensing classe
- MDM_WindowsLicensing classe, metodo UpgradeEditionWithProductKeyMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a44293701c5a18f20b7e286530446c662778999f3ffa5ed8edffb5819dda8a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913241"
---
# <a name="upgradeeditionwithproductkeymethod-method-of-the-mdm_windowslicensing-class"></a>Metodo UpgradeEditionWithProductKeyMethod della classe \_ MDM WindowsLicensing

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Immette un codice Product Key per un aggiornamento dell'edizione Windows 10 dispositivi desktop. Vedere anche [UpgradeEditionWithProductKey](/windows/client-management/mdm/windowslicensing-csp).

## <a name="syntax"></a>Sintassi


```mof
uint32 UpgradeEditionWithProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*param* \[ Pollici\]
</dt> <dd>

Codice Product Key.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Windows \_ MDMLicensing**](mdm-windowslicensing.md)
</dt> <dt>

[Uso di script di PowerShell con il provider bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

