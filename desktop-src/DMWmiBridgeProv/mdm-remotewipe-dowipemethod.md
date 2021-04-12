---
title: Metodo doWipeMethod della classe MDM_RemoteWipe
description: Attiva il dispositivo per avviare la cancellazione remota.
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- Metodo doWipeMethod
- Metodo doWipeMethod, classe MDM_RemoteWipe
- Classe MDM_RemoteWipe, metodo doWipeMethod
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f31dcc9dde2fe51ca0d8677df8b27637edd06c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475286"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a>Metodo doWipeMethod della classe MDM \_ RemoteWipe

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Attiva il dispositivo per avviare la cancellazione remota. Vedere anche [contrassegno dowipe](/windows/client-management/mdm/remotewipe-csp).

## <a name="syntax"></a>Sintassi


```mof
uint32 doWipeMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*param* \[ in\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | \\ \\ DMMap MDM CIMv2 \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_REMOTEWIPE MDM**](mdm-remotewipe.md)
</dt> <dt>

[Utilizzo di script di PowerShell con il provider del Bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

