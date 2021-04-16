---
title: Metodo ChangeProductKeyMethod della classe MDM_WindowsLicensing
description: Questo metodo installa un codice Product Key per i dispositivi Windows 10 desktop. Il punto non viene riavviato. Vedere anche ChangeProductKey.
ms.assetid: 1d9e3243-2ca4-427b-bda2-d33e1e70c80d
keywords:
- Metodo ChangeProductKeyMethod
- Metodo ChangeProductKeyMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, metodo ChangeProductKeyMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.ChangeProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e00345fb0e23655b457e0540c70289a169c54ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478046"
---
# <a name="changeproductkeymethod-method-of-the-mdm_windowslicensing-class"></a>Metodo ChangeProductKeyMethod della classe MDM \_ WindowsLicensing

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Questo metodo installa un codice Product Key per i dispositivi Windows 10 desktop. Il punto non viene riavviato. Vedere anche [ChangeProductKey](/windows/client-management/mdm/windowslicensing-csp)

## <a name="syntax"></a>Sintassi


```mof
uint32 ChangeProductKeyMethod(
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
| Spazio dei nomi<br/>                | \\ \\ Dmmap MDM CIMV2 \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_WINDOWSLICENSING MDM**](mdm-windowslicensing.md)
</dt> </dl>

 

