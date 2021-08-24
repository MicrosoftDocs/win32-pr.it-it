---
title: Metodo ChangeProductKeyMethod della classe MDM_WindowsLicensing
description: Questo metodo installa un codice Product Key per i Windows 10 desktop. Punto non riavvio. Vedere anche ChangeProductKey.
ms.assetid: 1d9e3243-2ca4-427b-bda2-d33e1e70c80d
keywords:
- Metodo ChangeProductKeyMethod
- Metodo ChangeProductKeyMethod, MDM_WindowsLicensing classe
- MDM_WindowsLicensing classe, metodo ChangeProductKeyMethod
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
ms.openlocfilehash: 0c164a97061b5e558a199a7d7e19a6bf26d7efc5d2a82c0a00e3831985c1a1cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693351"
---
# <a name="changeproductkeymethod-method-of-the-mdm_windowslicensing-class"></a>Metodo ChangeProductKeyMethod della classe \_ MDM WindowsLicensing

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

Questo metodo installa un codice Product Key per i Windows 10 desktop. Punto non riavvio. Vedere anche [ChangeProductKey](/windows/client-management/mdm/windowslicensing-csp)

## <a name="syntax"></a>Sintassi


```mof
uint32 ChangeProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*param* \[ Pollici\]
</dt> <dd></dd> </dl>

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
</dt> </dl>

 

